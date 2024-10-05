---
layout: post
title: Gene Expression Pipeline
date: '2024-03-12'
categories: Analysis
tags: [RNA, Bioinformatics, TagSeq]
---

## RNA-seq Data Processing Pipeline

### Below is a pipeline for processing RNA-seq data

#### For this pipeline, I have used the *Pocillopora acuta* genome. Some adjustments may need to be made based on your genome and genome annotation files.

#### Trimming parameters and parameters used at each step of pipeline can/should vary depending on your data quality and type. Look into the manuals of each program used for more information.

To see an example of this pipeline applied to real data, see [repository](https://github.com/zdellaert/LaserCoral/blob/main/code/RNA-seq-bioinf.md) here. In this example, I am submitting all bash scripts on the URI Andromeda Server using slurm.

## Make directory structure

**All scripts and commands in this pipeline will be run from the *RNA_seq_analysis* directory. Update "/full/path/to/" in any scripts to the base directory structure in which you create the directory "RNA_seq_analysis"**

```
cd /full/path/to/
mkdir RNA_seq_analysis
cd RNA_seq_analysis #Enter working directory

mkdir scripts #make folder for scripts
mkdir scripts/outs_errs #make folder for script output and error files
mkdir data_RNA  #make folder for raw data
mkdir output_RNA #make folder for output
```

## Symlink raw data files into data_RNA

```
ln -s data_location/*.fastq.gz ./data_RNA
```

## QC raw files

```
nano scripts/raw_qc.sh #write script for QC, enter text in next code chunk
```

```
#!/bin/bash
#SBATCH -t 24:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --mem=100GB
#SBATCH --export=NONE
#SBATCH --error=outs_errs/"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=outs_errs/"%x_output.%j" #once your job is completed, any final job report comments will be put in this file
#SBATCH -D /full/path/to/RNA_seq_analysis/data_RNA

# load modules needed
module load FastQC/0.11.9-Java-11
module load MultiQC/1.9-intel-2020a-Python-3.8.2

#make raw_qc output folder
mkdir raw_qc/

# Make an array of fastq files to trim
array1=($('ls' *.fastq.gz)) 

#run fastqc on raw data
for i in ${array1[@]}; do
    fastqc ${i} -o raw_qc/
    echo "fastqc ${i} done"
done

#fastqc *.fastq.gz -o raw_qc/

#Compile MultiQC report from FastQC files
multiqc raw_qc/  #Compile MultiQC report from FastQC files 

mv multiqc_report.html raw_qc/raw_qc_multiqc_report.html
mv multiqc_data raw_qc/raw_multiqc_data

echo "Initial QC of Seq data complete." $(date)
```

## Trimming adapters and low-quality bases and short reads (< 20bp)

I am going to use [cutadapt](https://cutadapt.readthedocs.io/en/stable/guide.html) for trimming of adaptors and quality control of low-quality bases. 

**Replace the adaptor sequences below with the adapter-trimming sequences specified in your library prep kit, or the standard illumina adapter sequences**

Example code with comments:

```
cutadapt \
    -a AGATCGGAAGAGCACACGTCTGAACTCCAGTCAC \  # NEB AdaptorRead1 
    -A AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT \  # NEB AdaptorRead2
    -o trimmed_R1.fastq.gz -p trimmed_R2.fastq.gz \ #output files
    input_R1.fastq.gz input_R2.fastq.gz \ #input files
    -q 20,20 \ #trims low-quality bases (score < 20) from the 3' end (first 20) and 5' (second 20) of the read
    --minimum-length 20 #after trimming, only keep a sequence if longer than 20 bp
```

```
nano scripts/cutadapt.sh #write script for trimming and QC, enter text in next code chunk
```

```
#!/bin/bash
#SBATCH -t 24:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --mem=200GB
#SBATCH --export=NONE
#SBATCH --error=../scripts/outs_errs/"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=../scripts/outs_errs/"%x_output.%j" #once your job is completed, any final job report comments will be put in this file
#SBATCH -D /full/path/to/RNA_seq_analysis/data_RNA

# load modules needed
module load cutadapt/4.2-GCCcore-11.3.0

#make arrays of R1 and R2 reads
R1_raw=($('ls' *R1*.fastq.gz))
R2_raw=($('ls' *R2*.fastq.gz))

for i in ${!R1_raw[@]}; do
    cutadapt \
    -a AGATCGGAAGAGCACACGTCTGAACTCCAGTCAC \
    -A AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT \
    -o trimmed_${R1_raw[$i]} -p trimmed_${R2_raw[$i]} \
    ${R1_raw[$i]} ${R2_raw[$i]} \
    -q 20,20 --minimum-length 20 --cores=20

    echo "trimming of ${R1_raw[$i]} and ${R2_raw[$i]} complete"
done

# unload conflicting modules with modules needed below
module unload cutadapt/4.2-GCCcore-11.3.0
module unload GCCcore/11.3.0 Python/3.10.4-GCCcore-11.3.0 libffi/3.4.2-GCCcore-11.3.0

# load modules needed
module load FastQC/0.11.9-Java-11
module load MultiQC/1.9-intel-2020a-Python-3.8.2

#make trimmed_qc output folder
mkdir trimmed_qc/

# Make an array of fastq files to trim
array_trim=($('ls' trimmed*)) 

#run fastqc on trimmed data
for i in ${array_trim[@]}; do
    fastqc ${i} -o trimmed_qc/
    echo "fastqc ${i} done"
done

#Compile MultiQC report from FastQC files
multiqc trimmed_qc/  #Compile MultiQC report from FastQC files 

mv multiqc_report.html trimmed_qc/trimmed_qc_multiqc_report.html
mv multiqc_data trimmed_qc/trimmed_multiqc_data

echo "QC of trimmed data complete." $(date)
```

### Assess the MultiQC and FastQC reports, and determine if another round of trimming needs to be done. 

## Download Genome: [*Pocillopora acuta*](http://cyanophora.rutgers.edu/Pocillopora_acuta/)

Rutgers University Stephens et al. 2022 [Publication](https://academic.oup.com/gigascience/article/doi/10.1093/gigascience/giac098/6815755)

Obtain reference genome assembly and gff annotation file.

```
wget http://cyanophora.rutgers.edu/Pocillopora_acuta/Pocillopora_acuta_HIv2.assembly.fasta.gz

wget http://cyanophora.rutgers.edu/Pocillopora_acuta/Pocillopora_acuta_HIv2.genes.gff3.gz

mkdir references/
mv *gz references/

gunzip references/Pocillopora_acuta_HIv2.assembly.fasta.gz #unzip genome file
gunzip references/Pocillopora_acuta_HIv2.genes.gff3.gz #unzip gff annotation file
```

### Convert GFF files to GTF format for Stringtie assembler

The gff3 file provided with the *Pocillopora acuta* genome is missing some features that are necessary for this pipeline (Stringtie specifically). I can correct the gff3 file and add those fields, but it is easier to convert the gff3 to a gtf file and automatically add those fields in the process. In order to do this, I am going to use the program [gffread](https://github.com/gpertea/gffread). Information and documentation about this package can be found on [the github examples page](https://github.com/gpertea/gffread/tree/master/examples).

```
nano scripts/gffread.sh
```

```
#!/bin/bash
#SBATCH -t 120:00:00
#SBATCH --nodes=1 --ntasks-per-node=1
#SBATCH --mem=100GB
#SBATCH --export=NONE
#SBATCH --error=../scripts/outs_errs/"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=../scripts/outs_errs/"%x_output.%j" #once your job is completed, any final job report comments will be put in this file
#SBATCH -D /full/path/to/RNA_seq_analysis/references

# load modules needed
module load gffread/0.12.7-GCCcore-11.2.0

# "Clean" GFF file if necessary, then convert cleaned file into a GTF
# -E : remove any "non-transcript features and optional attributes"

gffread -E Pocillopora_acuta_HIv2.genes.gff3 -T -o Pocillopora_acuta_HIv2.gtf 

echo "Check how many fields are in each row of the file; currently there are rows with two different lenghts: 10 and 12"
awk '{print NF}' Pocillopora_acuta_HIv2.gtf | sort -u

# Use awk to add "gene_id = TRANSCRIPT_ID" to each of the rows that only have a transcript id listed (the non-transcript lines)
awk 'BEGIN {FS=OFS="\t"} {if ($9 ~ /transcript_id/ && $9 !~ /gene_id/) {match($9, /transcript_id "([^"]+)";/, a); $9 = $9 " gene_id \"" a[1] "\";"}; print}' Pocillopora_acuta_HIv2.gtf > Pocillopora_acuta_HIv2_modified.gtf

echo "Check how many fields are in each row of the file; Now all the rows should be the same length and only one value should be printed, 12"
awk '{print NF}' Pocillopora_acuta_HIv2_modified.gtf | sort -u

# remove the non-modified file
rm Pocillopora_acuta_HIv2.gtf

# rename the modified file
mv Pocillopora_acuta_HIv2_modified.gtf Pocillopora_acuta_HIv2.gtf
```

Script outputs:

- loaded 33730 genomic features from Pocillopora_acuta_HIv2.genes.gff3

- Check how many fields are in each row of the file; currently there are rows with two different lenghts: 10 and 12
    - 10
    - 12
- Check how many fields are in each row of the file; Now all the rows should be the same length and only one value should be printed, 12
    - 12

## HISAT2 Alignment

I will use [Hisat2](https://daehwankimlab.github.io/hisat2/manual/) to align the RNA-seq reads to the *P. acuta* genome

The code below is for unstranded RNA-seq. See notes here: [strand-related settings for RNA-seq tools](https://rnabio.org/module-09-appendix/0009/12/01/StrandSettings/)

```
hisat2 -p 16 \ #use 16 threads
    --time \ Print the wall-clock time required to load the index files and align the reads to stderr
    --dta \ #for input into Stringtie transcriptome assembly
    -q \ #fastq input files
    -x Pacuta_ref \ #index location 
    -1 ${read1} -2 ${read2} \ #input files, R1 and R2
    -S hisat2/${sample_name}.sam #output sam file
```

```
nano scripts/hisat2.sh #write script for alignment, enter text in next code chunk
```

```
#!/bin/bash
#SBATCH -t 120:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --mem=200GB
#SBATCH --export=NONE
#SBATCH --error=../scripts/outs_errs/"%x_error.%j" #write out slurm error reports
#SBATCH --output=../scripts/outs_errs/"%x_output.%j" #write out any program outpus
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --mail-user=zdellaert@uri.edu #your email to send notifications
#SBATCH -D /full/path/to/RNA_seq_analysis/output_RNA #set working directory

# load modules needed
module load HISAT2/2.2.1-gompi-2022a #Alignment to reference genome: HISAT2
module load SAMtools/1.16.1-GCC-11.3.0 #Preparation of alignment for assembly: SAMtools

# index the reference genome, will write to a directory called Pacuta_ref
hisat2-build -f ../references/Pocillopora_acuta_HIv2.assembly.fasta ./Pacuta_ref

echo "Reference genome indexed. Starting alingment" $(date)

# make the output directory if it does not exist (-p checks for this)
mkdir -p hisat2

# call the oligo-trimmed sequences into an array
array=(../data_RNA/trimmed_oligo*_R1_001.fastq.gz)

# align the files to the indexed genome using hisat2
for read1 in ${array[@]}; do
    
    # extract the sample name of R1 files
    sample_name=$(basename $read1 | sed 's/.*trimmed_\([A-Za-z0-9]*_[0-9]*\).*/\1/')
    
    # Define the corresponding reverse read file (R2)
    read2=${read1/_R1_/_R2_}
    
    # perform alignment
    hisat2 -p 16 --time --dta -q -x Pacuta_ref -1 ${read1} -2 ${read2} -S hisat2/${sample_name}.sam
    echo "${sample_name} aligned!"

    # sort the sam file into a bam file
    samtools sort -@ 8 -o hisat2/${sample_name}.bam hisat2/${sample_name}.sam
    echo "${sample_name} bam-ified!"
    
    # index bam file , creating a .bai file which is nice for viewing in IGB
    samtools index hisat2/${sample_name}.bam hisat2/${sample_name}.bai
    
    # remove sam file to save disk space
    rm hisat2/${sample_name}.sam
done

# move the reference index files into the hisat2 directory
mv Pacuta_ref.* hisat2/

#  Calculate mapping percentages
for i in hisat2/*.bam; do
    echo "${i}" >> mapped_reads_counts_Pacuta
    samtools flagstat ${i} | grep "mapped (" >> hisat2/mapped_reads_counts_Pacuta
done
```

## Assembly with Stringtie

I will use [Stringtie](https://ccb.jhu.edu/software/stringtie/index.shtml?t=manual) to perform reference-guided assembly of the RNA-seq data. I am using the simplified stringtie protocol with the "stringtie -eB" option:

<img width="800" alt="stringtie_workflow" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/stringtie_workflow.png?raw=true">

Note: Use of -e (Expression estimation mode) means stringtie will only estimate the abundance of given reference transcripts (only genes from the genome, no novel genes). If you are interested in novel genes or splice variants, see Stringtie documentation:

> StringTie will not attempt to assemble the input read alignments but instead it will only estimate the expression levels of the "reference" transcripts provided in the -G file. With this option, no "novel" transcript assemblies (isoforms) will be produced, and read alignments not overlapping any of the given reference transcripts will be ignored.

```
nano scripts/stringtie.sh #make script for assembly, enter text in next code chunk
```

```
#!/bin/bash
#SBATCH -t 120:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --mem=200GB
#SBATCH --export=NONE
#SBATCH --error=../scripts/outs_errs/"%x_error.%j" #write out slurm error reports
#SBATCH --output=../scripts/outs_errs/"%x_output.%j" #write out any program outpus
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --mail-user=zdellaert@uri.edu #your email to send notifications
#SBATCH -D /full/path/to/RNA_seq_analysis/output_RNA #set working directory

# move into stringtie directory
module load StringTie/2.1.4-GCC-9.3.0

# make the output directory if it does not exist (-p checks for this)
mkdir -p stringtie

# call the hisat2 bam files into an array
array=(hisat2/*.bam)

for i in "${array[@]}"; do 
    sample_name=$(echo "$i" | awk -F'[/.]' '{print $2}')

    # -p 16 : use 16 cores
    # -e : exclude novel genes
    # -B : create Ballgown input files for downstream analysis
    # -v : enable verbose mode
    # -G : gtf annotation file
    # -A : output name for gene abundance estimate files
    # -o : output name for gtf file

    stringtie -p 16 -e -B -v \
        -G ../references/Pocillopora_acuta_HIv2.gtf \
        -A stringtie/"${sample_name}".gene_abund.tab \
        -o stringtie/"${sample_name}".gtf \
        "$i" #input bam file

    echo "StringTie assembly for seq file ${i}" $(date)
done

echo "StringTie assembly COMPLETE" $(date)
```

## Generate gene count matrix using [prepDE.py script from Stringtie](https://ccb.jhu.edu/software/stringtie/index.shtml?t=manual)

Download script from [stringtie website](https://ccb.jhu.edu/software/stringtie/dl/prepDE.py3) or [github repository](https://github.com/gpertea/stringtie/blob/master/prepDE.py3). I am using the python3 version, but this and the original version (prepDE.py) are very similar and should give the exact same result. I am using [this input file format](https://ccb.jhu.edu/software/stringtie/dl/sample_lst.txt).

```
cd scripts
wget https://ccb.jhu.edu/software/stringtie/dl/prepDE.py3
nano prepDE.sh
```

```
#!/bin/bash
#SBATCH -t 120:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --mem=200GB
#SBATCH --export=NONE
#SBATCH --error=../scripts/outs_errs/"%x_error.%j" #write out slurm error reports
#SBATCH --output=../scripts/outs_errs/"%x_output.%j" #write out any program outpus
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --mail-user=zdellaert@uri.edu #your email to send notifications
#SBATCH -D /full/path/to/RNA_seq_analysis/output_RNA #set working directory

# load modules needed
module load StringTie/2.1.4-GCC-9.3.0 #stringtie module, includes Python 3.8.5

# move into stringtie directory
cd stringtie

# make input file
for filename in *.gtf; do
    sample_name=$(echo "$filename" | awk -F'[.]' '{print $1}')

    echo $sample_name $PWD/$filename
done > listGTF.txt

#Compile the gene count matrix
python ../../scripts/prepDE.py3 -g gene_count_matrix.csv -i listGTF.txt

echo "Gene count matrix compiled." $(date)
```