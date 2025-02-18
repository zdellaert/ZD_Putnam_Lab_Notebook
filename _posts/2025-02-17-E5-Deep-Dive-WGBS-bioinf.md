---
layout: post
title: Deep Dive WGBS Bioinformatics Test
date: '2025-02-17'
categories: Analysis
tags: [DNA, Bioinformatics, WGBS, E5]
---

## Deep Dive WGBS Bioinformatics Test

Doing this here as to not confuse results in the [deep-dive expression repo](https://github.com/urol-e5/deep-dive-expression.git).

1. Make unity scratch directory and clone github repo

```
ws_allocate -n deep_dive -G pi_hputnam_uri_edu
cd /scratch3/workspace/zdellaert_uri_edu-deep_dive
git clone https://github.com/urol-e5/deep-dive-expression.git
cd deep-dive-expression/
```

2. Download trimmed WGBS data (ACR)

```
cd D-Apul/output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/

wget -r -np -nH --cut-dirs=7 -A '*.gz' https://gannet.fish.washington.edu/gitrepos/urol-e5/deep-dive-expression/D-Apul/output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/
```

3. Download genome (ACR)

```
cd deep-dive-expression/
wget -r -np -nH --cut-dirs=3 https://gannet.fish.washington.edu/seashell/bu-github/deep-dive-expression/D-Apul/data/Apulcra-genome.fa
```

4. Prepare genome for bismark

```
cd deep-dive-expression/
cd D-Apul/code
nano scripts/bismark_genome.sh 
```

```
#!/usr/bin/env bash
#SBATCH --export=NONE
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --mem=200GB
#SBATCH -t 24:00:00
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --error=scripts/outs_errs/"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=scripts/outs_errs/"%x_output.%j" #once your job is completed, any final job report comments will be put in this file

# load modules needed
module load uri/main
module load Bismark/0.23.1-foss-2021b
module load bowtie2/2.5.2

cd ../data

bismark_genome_preparation --verbose --parallel 10 ./
```

5. Test alignment parameters

Testing score min parameters based on https://sr320.github.io/tumbling-oysters/posts/33-bismark-array/

```
cd deep-dive-expression/
cd D-Apul/code
nano scripts/bismark_align_paramtest.sh 
```

```
#!/usr/bin/env bash
#SBATCH --ntasks=1 --cpus-per-task=30 #split one task over multiple CPU
#SBATCH --array=0-4 #for 5 samples
#SBATCH --mem=100GB
#SBATCH -t 00:30:00
#SBATCH --mail-type=END,FAIL,TIME_LIMIT_80 #email you when job stops and/or fails or is nearing its time limit
#SBATCH --error=scripts/outs_errs/"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=scripts/outs_errs/"%x_output.%j" #once your job is completed, any final job report comments will be put in this file

# load modules needed
module load uri/main
module load Bismark/0.23.1-foss-2021b
module load bowtie2/2.5.2

# Set directories and files
reads_dir="../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/"
genome_folder="../data/"

mkdir -p ../output/08-Apul-WGBS/align_paramtest

output_dir="../output/08-Apul-WGBS/align_paramtest"
checkpoint_file="../output/08-Apul-WGBS/align_paramtest/completed_samples.log"

# Create the checkpoint file if it doesn't exist
touch ${checkpoint_file}

# Get the list of sample files and corresponding sample names
files=(${reads_dir}*_R1.fastp-trim.fq.gz)
file="${files[$SLURM_ARRAY_TASK_ID]}"
sample_name=$(basename "$file" "_R1.fastp-trim.fq.gz")

# Check if the sample has already been processed
if grep -q "^${sample_name}$" ${checkpoint_file}; then
    echo "Sample ${sample_name} already processed. Skipping..."
    exit 0
fi

# Define log files for stdout and stderr
stdout_log="${output_dir}/${sample_name}_stdout.log"
stderr_log="${output_dir}/${sample_name}_stderr.log"

# Define the array of score_min parameters to test
score_min_params=(
    "L,0,-0.4"
    "L,0,-0.6"
    "L,0,-0.8"
    "L,0,-1.0"
    "L,-1,-0.6"
)

# Loop through each score_min parameter
for score_min in "${score_min_params[@]}"; do
    echo "Running Bismark for sample ${sample_name} with score_min ${score_min}"
    
    # Create a subdirectory for this parameter
    param_output_dir="${output_dir}/${sample_name}_score_${score_min//,/}"
    mkdir -p ${param_output_dir}

    # Run Bismark alignment
    bismark \
        -genome ${genome_folder} \
        -p 8 \
        -u 10000 \
        -score_min ${score_min} \
        --non_directional \
        -1 ${reads_dir}${sample_name}_R1.fastp-trim.fq.gz \
        -2 ${reads_dir}${sample_name}_R2.fastp-trim.fq.gz \
        -o ${param_output_dir} \
        --basename ${sample_name}_${score_min//,/} \
        2> "${param_output_dir}/${sample_name}-bismark_summary.txt"

    # Check if the command was successful
    if [ $? -eq 0 ]; then
        echo "Sample ${sample_name} with score_min ${score_min} processed successfully."
    else
        echo "Sample ${sample_name} with score_min ${score_min} failed. Check ${stderr_log} for details."
    fi
done

# Mark the sample as completed in the checkpoint file
if [ $? -eq 0 ]; then
    echo ${sample_name} >> ${checkpoint_file}
    echo "All tests for sample ${sample_name} completed."
else
    echo "Sample ${sample_name} encountered errors. Check logs for details."
fi

# Define directories
summary_file="${output_dir}/parameter_comparison_summary.csv"

# Initialize summary file
echo "Sample,Score_Min,Alignment_Rate" > ${summary_file}

# Loop through parameter output directories
for dir in ${output_dir}/*_score_*; do
    if [ -d "$dir" ]; then
        # Extract sample name and score_min parameter from directory name
        sample_name=$(basename "$dir" | cut -d'_' -f1)
        score_min=$(basename "$dir" | grep -o "score_.*" | sed 's/score_//; s/_/,/g')

        # Locate the summary file
        summary_file_path="${dir}/${sample_name}_${score_min}_PE_report.txt"

        # Extract metrics
        mapping=$(grep "Mapping efficiency:" ${summary_file_path} | awk '{print "mapping efficiency ", $3}')
        
        # Append to the summary file
        echo "${sample_name},${score_min},${mapping}" >> ${summary_file}
    fi
done
```

5. Align to genome with best min-score paramters

Array job script based on https://sr320.github.io/tumbling-oysters/posts/33-bismark-array/

```
cd deep-dive-expression/
cd D-Apul/code
nano scripts/bismark_align.sh 
```

```
#!/usr/bin/env bash
#SBATCH --ntasks=1 --cpus-per-task=30 #split one task over multiple CPU
#SBATCH --array=0-4 #for 5 samples
#SBATCH --mem=200GB
#SBATCH -t 24:00:00
#SBATCH --mail-type=END,FAIL,TIME_LIMIT_80 #email you when job stops and/or fails or is nearing its time limit
#SBATCH --error=scripts/outs_errs/"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=scripts/outs_errs/"%x_output.%j" #once your job is completed, any final job report comments will be put in this file

# load modules needed
module load uri/main
module load Bismark/0.23.1-foss-2021b
module load bowtie2/2.5.2

# Set directories and files
reads_dir="../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/"
genome_folder="../data/"

mkdir -p ../output/08-Apul-WGBS/bismark

output_dir="../output/08-Apul-WGBS/bismark"
checkpoint_file="../output/08-Apul-WGBS/bismark/completed_samples.log"


# Create the checkpoint file if it doesn't exist
touch ${checkpoint_file}

# Get the list of sample files and corresponding sample names
files=(${reads_dir}*_R1.fastp-trim.fq.gz)
file="${files[$SLURM_ARRAY_TASK_ID]}"
sample_name=$(basename "$file" "_R1.fastp-trim.fq.gz")

# Check if the sample has already been processed
if grep -q "^${sample_name}$" ${checkpoint_file}; then
    echo "Sample ${sample_name} already processed. Skipping..."
    exit 0
fi

# Define log files for stdout and stderr
stdout_log="${output_dir}/${sample_name}_stdout.log"
stderr_log="${output_dir}/${sample_name}_stderr.log"

# Run Bismark alignment
bismark \
    -genome ${genome_folder} \
    -p 8 \
    -score_min L,0,-1.0 \
    --non_directional \
    -1 ${reads_dir}${sample_name}_R1.fastp-trim.fq.gz \
    -2 ${reads_dir}${sample_name}_R2.fastp-trim.fq.gz \
    -o ${output_dir} \
    --basename ${sample_name} \
    2> "${output_dir}/${sample_name}-bismark_summary.txt"

# Check if the command was successful
if [ $? -eq 0 ]; then
    # Append the sample name to the checkpoint file
    echo ${sample_name} >> ${checkpoint_file}
    echo "Sample ${sample_name} processed successfully."
else
    echo "Sample ${sample_name} failed. Check ${stderr_log} for details."
fi

# Define directories
summary_file="${output_dir}/alignment_summary.csv"

# Initialize summary file
echo "Sample,Score_Min,Alignment_Rate" > ${summary_file}

# Loop through parameter output directories
for file in ${output_dir}/*_report.txt; do
    # Extract sample name and score_min parameter from directory name
    sample_name=$(basename "$file" | cut -d'_' -f1)
    score_min="L0-1.0"

    # Locate the summary file
    summary_file_path="${output_dir}/${sample_name}_PE_report.txt"

    # Extract metrics
    mapping=$(grep "Mapping efficiency:" ${summary_file_path} | awk '{gsub("%", "", $3); print $3}')

    # Append to the summary file
    echo "${sample_name},${score_min},${mapping}" >> ${summary_file}
done
```

5. Results

Test alignments of only 10,000 reads with different min-score parameters:

```
cat align_paramtest/parameter_comparison_summary.csv
```
```
Sample,Score_Min,Alignment_Rate
ACR-140-TP2,L-1-0.6,
ACR-140-TP2,L0-0.4,mapping efficiency  0.0%
ACR-140-TP2,L0-0.6,mapping efficiency  0.0%
ACR-140-TP2,L0-0.8,mapping efficiency  0.0%
ACR-140-TP2,L0-1.0,mapping efficiency  0.1%
ACR-145-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-140-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-145-TP2,L0-0.4,mapping efficiency  0.0%
ACR-140-TP2,L0-0.4,mapping efficiency  0.0%
ACR-145-TP2,L0-0.6,mapping efficiency  0.0%
ACR-140-TP2,L0-0.6,mapping efficiency  0.0%
ACR-145-TP2,L0-0.8,mapping efficiency  0.0%
ACR-140-TP2,L0-0.8,mapping efficiency  0.0%
ACR-145-TP2,L0-1.0,mapping efficiency  0.1%
ACR-140-TP2,L0-1.0,mapping efficiency  0.1%
ACR-150-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-145-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-150-TP2,L0-0.4,mapping efficiency  0.0%
ACR-145-TP2,L0-0.4,mapping efficiency  0.0%
ACR-150-TP2,L0-0.6,mapping efficiency  0.0%
ACR-145-TP2,L0-0.6,mapping efficiency  0.0%
ACR-150-TP2,L0-0.8,mapping efficiency  0.1%
ACR-145-TP2,L0-0.8,mapping efficiency  0.0%
ACR-150-TP2,L0-1.0,mapping efficiency  0.1%
ACR-145-TP2,L0-1.0,mapping efficiency  0.1%
ACR-173-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-150-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-173-TP2,L0-0.4,mapping efficiency  0.0%
ACR-150-TP2,L0-0.4,mapping efficiency  0.0%
ACR-173-TP2,L0-0.6,mapping efficiency  0.0%
ACR-150-TP2,L0-0.6,mapping efficiency  0.0%
ACR-150-TP2,L0-0.8,mapping efficiency  0.1%
ACR-173-TP2,L0-0.8,mapping efficiency  0.0%
ACR-150-TP2,L0-1.0,mapping efficiency  0.1%
ACR-173-TP2,L0-1.0,mapping efficiency  0.1%
ACR-173-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-178-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-173-TP2,L0-0.4,mapping efficiency  0.0%
ACR-178-TP2,L0-0.4,mapping efficiency  0.0%
ACR-173-TP2,L0-0.6,mapping efficiency  0.0%
ACR-178-TP2,L0-0.6,mapping efficiency  0.0%
ACR-173-TP2,L0-0.8,mapping efficiency  0.0%
ACR-178-TP2,L0-0.8,mapping efficiency  0.0%
ACR-173-TP2,L0-1.0,mapping efficiency  0.1%
ACR-178-TP2,L0-1.0,mapping efficiency  0.1%
ACR-178-TP2,L-1-0.6,mapping efficiency  0.0%
ACR-178-TP2,L0-0.4,mapping efficiency  0.0%
ACR-178-TP2,L0-0.6,mapping efficiency  0.0%
ACR-178-TP2,L0-0.8,mapping efficiency  0.0%
ACR-178-TP2,L0-1.0,mapping efficiency  0.1%
```

Alignment of all reads (ACR) against ACR genome:

```
cat alignment_summary.csv
```

```
Sample,Score_Min,Alignment_Rate
ACR-140-TP2,L0-1.0,
ACR-145-TP2,L0-1.0,0.1
ACR-150-TP2,L0-1.0,0.1
ACR-173-TP2,L0-1.0,0.1
ACR-178-TP2,L0-1.0,0.1
```

```
Bismark report for: ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-140-TP2_R1.fastp-trim.fq.gz and ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-140-TP2_R2.fastp-trim.fq.gz (version: v0.23.1)
Bismark was run with Bowtie 2 against the bisulfite genome of /scratch3/workspace/zdellaert_uri_edu-deep_dive/deep-dive-expression/D-Apul/data/ with the specified options: -q --score-min L,0,-1.0 -p 8 --reorder --ignore-quals --no-mixed --no-discordant --dovetail --maxins 500
Option '--non_directional' specified: alignments to all strands were being performed (OT, OB, CTOT, CTOB)
```

(this one is still running)

```
Bismark report for: ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-145-TP2_R1.fastp-trim.fq.gz and ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-145-TP2_R2.fastp-trim.fq.gz (version: v0.23.1)
Bismark was run with Bowtie 2 against the bisulfite genome of /scratch3/workspace/zdellaert_uri_edu-deep_dive/deep-dive-expression/D-Apul/data/ with the specified options: -q --score-min L,0,-1.0 -p 8 --reorder --ignore-quals --no-mixed --no-discordant --dovetail --maxins 500
Option '--non_directional' specified: alignments to all strands were being performed (OT, OB, CTOT, CTOB)

Final Alignment report
======================
Sequence pairs analysed in total:	243394673
Number of paired-end alignments with a unique best hit:	151212
Mapping efficiency:	0.1%
Sequence pairs with no alignments under any condition:	242827412
Sequence pairs did not map uniquely:	416049
Sequence pairs which were discarded because genomic sequence could not be extracted:	0

Number of sequence pairs with unique best (first) alignment came from the bowtie output:
CT/GA/CT:	3242	((converted) top strand)
GA/CT/CT:	69191	(complementary to (converted) top strand)
GA/CT/GA:	75676	(complementary to (converted) bottom strand)
CT/GA/GA:	3103	((converted) bottom strand)

Final Cytosine Methylation Report
=================================
Total number of C's analysed:	2954644

Total methylated C's in CpG context:	176422
Total methylated C's in CHG context:	125336
Total methylated C's in CHH context:	1292339
Total methylated C's in Unknown context:	18381

Total unmethylated C's in CpG context:	195179
Total unmethylated C's in CHG context:	208684
Total unmethylated C's in CHH context:	956684
Total unmethylated C's in Unknown context:	31285

C methylated in CpG context:	47.5%
C methylated in CHG context:	37.5%
C methylated in CHH context:	57.5%
C methylated in unknown context (CN or CHN):	37.0%


Bismark completed in 0d 12h 57m 53s
```

```
Bismark report for: ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-150-TP2_R1.fastp-trim.fq.gz and ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-150-TP2_R2.fastp-trim.fq.gz (version: v0.23.1)
Bismark was run with Bowtie 2 against the bisulfite genome of /scratch3/workspace/zdellaert_uri_edu-deep_dive/deep-dive-expression/D-Apul/data/ with the specified options: -q --score-min L,0,-1.0 -p 8 --reorder --ignore-quals --no-mixed --no-discordant --dovetail --maxins 500
Option '--non_directional' specified: alignments to all strands were being performed (OT, OB, CTOT, CTOB)

Final Alignment report
======================
Sequence pairs analysed in total:	233529125
Number of paired-end alignments with a unique best hit:	173677
Mapping efficiency:	0.1%
Sequence pairs with no alignments under any condition:	232908054
Sequence pairs did not map uniquely:	447394
Sequence pairs which were discarded because genomic sequence could not be extracted:	0

Number of sequence pairs with unique best (first) alignment came from the bowtie output:
CT/GA/CT:	3074	((converted) top strand)
GA/CT/CT:	82236	(complementary to (converted) top strand)
GA/CT/GA:	85279	(complementary to (converted) bottom strand)
CT/GA/GA:	3088	((converted) bottom strand)

Final Cytosine Methylation Report
=================================
Total number of C's analysed:	3057643

Total methylated C's in CpG context:	200899
Total methylated C's in CHG context:	148602
Total methylated C's in CHH context:	1416249
Total methylated C's in Unknown context:	20551

Total unmethylated C's in CpG context:	194171
Total unmethylated C's in CHG context:	214853
Total unmethylated C's in CHH context:	882869
Total unmethylated C's in Unknown context:	29707

C methylated in CpG context:	50.9%
C methylated in CHG context:	40.9%
C methylated in CHH context:	61.6%
C methylated in unknown context (CN or CHN):	40.9%


Bismark completed in 0d 11h 44m 53s
```

```
Bismark report for: ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-173-TP2_R1.fastp-trim.fq.gz and ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-173-TP2_R2.fastp-trim.fq.gz (version: v0.23.1)
Bismark was run with Bowtie 2 against the bisulfite genome of /scratch3/workspace/zdellaert_uri_edu-deep_dive/deep-dive-expression/D-Apul/data/ with the specified options: -q --score-min L,0,-1.0 -p 8 --reorder --ignore-quals --no-mixed --no-discordant --dovetail --maxins 500
Option '--non_directional' specified: alignments to all strands were being performed (OT, OB, CTOT, CTOB)

Final Alignment report
======================
Sequence pairs analysed in total:	213089337
Number of paired-end alignments with a unique best hit:	144472
Mapping efficiency:	0.1%
Sequence pairs with no alignments under any condition:	212569580
Sequence pairs did not map uniquely:	375285
Sequence pairs which were discarded because genomic sequence could not be extracted:	0

Number of sequence pairs with unique best (first) alignment came from the bowtie output:
CT/GA/CT:	2632	((converted) top strand)
GA/CT/CT:	67895	(complementary to (converted) top strand)
GA/CT/GA:	71358	(complementary to (converted) bottom strand)
CT/GA/GA:	2587	((converted) bottom strand)

Final Cytosine Methylation Report
=================================
Total number of C's analysed:	2617042

Total methylated C's in CpG context:	161413
Total methylated C's in CHG context:	110908
Total methylated C's in CHH context:	1207851
Total methylated C's in Unknown context:	16051

Total unmethylated C's in CpG context:	172455
Total unmethylated C's in CHG context:	182093
Total unmethylated C's in CHH context:	782322
Total unmethylated C's in Unknown context:	25092

C methylated in CpG context:	48.3%
C methylated in CHG context:	37.9%
C methylated in CHH context:	60.7%
C methylated in unknown context (CN or CHN):	39.0%


Bismark completed in 0d 11h 17m 40s
```

```
Bismark report for: ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-178-TP2_R1.fastp-trim.fq.gz and ../output/01.00-D-Apul-WGBS-trimming-fastp-FastQC-MultiQC/trimmed-fastqs/ACR-178-TP2_R2.fastp-trim.fq.gz (version: v0.23.1)
Bismark was run with Bowtie 2 against the bisulfite genome of /scratch3/workspace/zdellaert_uri_edu-deep_dive/deep-dive-expression/D-Apul/data/ with the specified options: -q --score-min L,0,-1.0 -p 8 --reorder --ignore-quals --no-mixed --no-discordant --dovetail --maxins 500
Option '--non_directional' specified: alignments to all strands were being performed (OT, OB, CTOT, CTOB)

Final Alignment report
======================
Sequence pairs analysed in total:	182080986
Number of paired-end alignments with a unique best hit:	130790
Mapping efficiency:	0.1%
Sequence pairs with no alignments under any condition:	181608799
Sequence pairs did not map uniquely:	341397
Sequence pairs which were discarded because genomic sequence could not be extracted:	0

Number of sequence pairs with unique best (first) alignment came from the bowtie output:
CT/GA/CT:	2372	((converted) top strand)
GA/CT/CT:	60939	(complementary to (converted) top strand)
GA/CT/GA:	65143	(complementary to (converted) bottom strand)
CT/GA/GA:	2336	((converted) bottom strand)

Final Cytosine Methylation Report
=================================
Total number of C's analysed:	2404419

Total methylated C's in CpG context:	159683
Total methylated C's in CHG context:	108300
Total methylated C's in CHH context:	1126914
Total methylated C's in Unknown context:	15272

Total unmethylated C's in CpG context:	160068
Total unmethylated C's in CHG context:	171051
Total unmethylated C's in CHH context:	678403
Total unmethylated C's in Unknown context:	22482

C methylated in CpG context:	49.9%
C methylated in CHG context:	38.8%
C methylated in CHH context:	62.4%
C methylated in unknown context (CN or CHN):	40.5%


Bismark completed in 0d 9h 48m 44s
```