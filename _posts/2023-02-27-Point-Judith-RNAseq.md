---
layout: post
title: Point Judith Oyster RNAseq Analysis
date: '2023-02-27 06:00:00'
categories: Analysis
tags: [RNA, OysterPaper]
---

# Point Judith Oyster RNAseq Analysis
### Point Judith Oyster RNAseq Initial QC : https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Point-Judith-RNAseq-QC/

## Notes

**We took out the following because they are less consistent - less adapter content issues and proper trimming.**

```
    --qualified_quality_phred 20 
    --unqualified_percent_limit 10 
    --length_required 75 
    --cut_right cut_right_window_size 5 cut_right_mean_quality 20
```

Based trimming of front1 and front2 set at 15 based on MulitQC "Per base sequence content". If we see issues down the line then we could do more filtering based on quality.

- db and NS batch effects
- write the methods and rationale as you go on


## Location of data:
```
/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all
```

## Round 1: Trimming Data and performing trimmed multiQC

Used this script [by Emma!!](https://github.com/emmastrand/EmmaStrand_Notebook/blob/master/_posts/2022-02-03-KBay-Bleaching-Pairs-RNASeq-Pipeline-Analysis.md), fastp_multiqc.sh :

**We took out the following because they are less consistent - less adapter content issues and proper trimming.**

Also changed the way the files were being imported, since fastp wants R1 and R2 to be dealt with at the same time and Emma's version was doing it correctly for R1 (R1 and R2 were being trimmed together) but then R2 as being trimmed and overwriting the R2 output from the R1/R2 trimming. So changed it so it would loop through just the R1 files and not all files (because the fastp code runs through the R2 files already using "|sed s/_R1/_R2/") and then made a second line for fastp to loop through the R2 files as well.

```
    --qualified_quality_phred 20 
    --unqualified_percent_limit 10 
    --length_required 75 
    --cut_right cut_right_window_size 5 cut_right_mean_quality 20
```

```
cd /data/putnamlab/shared/Oyst_Nut_RNA/
mkdir /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/
nano scripts/fastp_multiqc.sh
```

```
#!/bin/bash
#SBATCH -t 100:00:00
#SBATCH --nodes=1 --ntasks-per-node=1
#SBATCH --export=NONE
#SBATCH --mem=100GB
#SBATCH --account=putnamlab
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc               
#SBATCH --error=../"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=../"%x_output.%j" #once your job is completed, any final job report comments will be put in this file

# Load modules needed 
module load fastp/0.19.7-foss-2018b
module load FastQC/0.11.8-Java-1.8
module load MultiQC/1.9-intel-2020a-Python-3.8.2

# Make an array (list) of sequences to trim
# Needs to be in the raw data directory

cd /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all 
array1=($(ls *R1.fastq.gz))

# fastp and fastqc loop 
for i in ${array1[@]}; do
    fastp --in1 ${i} \
        --in2 $(echo ${i}|sed s/_R1/_R2/)\
        --out1 /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.${i} \
        --out2 /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.$(echo ${i}|sed s/_R1/_R2/) \
        --detect_adapter_for_pe \
        --trim_poly_g \
        --trim_front1 15 \
        --trim_front2 15
    fastqc /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.${i}
    fastqc /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.$(echo ${i}|sed s/_R1/_R2/)
done

echo "Read trimming of adapters complete." $(date)

# Quality Assessment of Trimmed Reads
cd /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/ #go to output directory

# Compile MultiQC report from FastQC files 
multiqc --interactive ./  

echo "Cleaned MultiQC report generated." $(date)
```

```
sbatch scripts/fastp_multiqc.sh
```

### Trimmed FastQC example

Very interestingly, overrepresented seqs increased after trimming. Everything else generally looked better. 

![DB_Sample1_R1_fastqc_perbaseseqcont.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/DB_Sample1_R1_fastqc_perbaseseqcont.png?raw=true)

![trimmed_DB_Sample1_R1_fastqc_perbaseseqcont.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_DB_Sample1_R1_fastqc_perbaseseqcont.png?raw=true)

![DB_Sample1_R1_fastqc_perbaseseqqual.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/DB_Sample1_R1_fastqc_perbaseseqqual.png?raw=true)

![trimmed_DB_Sample1_R1_fastqc_perbaseseqqual.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_DB_Sample1_R1_fastqc_perbaseseqqual.png?raw=true)

![DB_Sample1_R1_fastqc_overrepseqs.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/DB_Sample1_R1_fastqc_overrepseqs.png?raw=true)

![trimmed_DB_Sample1_R1_fastqc_overrepseqs.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_DB_Sample1_R1_fastqc_overrepseqs.png?raw=true)


### Trimmed (fastp) MultiQC Report

![MultiQC_MeanQualScores.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_MeanQualScores.png?raw=true)

![MultiQC_trimmed_MeanQualScores.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_trimmed_MeanQualScores.png?raw=true)

![MultiQC_AdapterContent.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_AdapterContent.png?raw=true)

![MultiQC_trimmed_AdapterContent.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_trimmed_AdapterContent.png?raw=true)

#### Weird things:

R1 has slightly more wobbly-ness for "Per Base Sequence Content" at the beginning than R2 for all samples.

![MultiQC_trimmed_R1_PerBaseSeqContent.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_trimmed_R1_PerBaseSeqContent.png?raw=true)

![MultiQC_trimmed_R2_PerBaseSeqContent.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_trimmed_R2_PerBaseSeqContent.png?raw=true)

Sequence Duplication Levels got worse:

![MultiQC_DupLevels.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_DupLevels.png?raw=true)

![MultiQC_trimmed_DupLevels.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_trimmed_DupLevels.png?raw=true)

![MultiQC_StatusCheck.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_StatusCheck.png?raw=true)

![MultiQC_trimmed_StatusCheck.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/MultiQC_trimmed_StatusCheck.png?raw=true)

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/multiqc_report.html /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/trimmed_fastp_multiqc_report_Oyst_Nut_RNA.html
```

Full report here: [link](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_fastp_multiqc_report_Oyst_Nut_RNA.html)

and here: [link](https://github.com/hputnam/Cvir_Nut_Int/blob/master/output/RNASeq/trimmed_fastp_multiqc_report_Oyst_Nut_RNA.html)

## Round 2: Trimming Data with extra quality control and performing trimmed multiQC

Used this script [by Emma!!](https://github.com/emmastrand/EmmaStrand_Notebook/blob/master/_posts/2022-02-03-KBay-Bleaching-Pairs-RNASeq-Pipeline-Analysis.md), fastp_multiqc.sh :

**Added in "--qualified_quality_phred 30"  to filter by minimum phred quality score of >30.**

```
cd /data/putnamlab/shared/Oyst_Nut_RNA/s
mkdir /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/
nano scripts/fastp_qual_multiqc.sh
```

```
#!/bin/bash
#SBATCH -t 100:00:00
#SBATCH --nodes=1 --ntasks-per-node=1
#SBATCH --export=NONE
#SBATCH --mem=100GB
#SBATCH --account=putnamlab
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/            
#SBATCH --error=../"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=../"%x_output.%j" #once your job is completed, any final job report comments will be put in this file

# Load modules needed 
module load fastp/0.19.7-foss-2018b
module load FastQC/0.11.8-Java-1.8
module load MultiQC/1.9-intel-2020a-Python-3.8.2

# Make an array (list) of sequences to trim

# Needs to be in the raw data directory

cd /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all 
array1=($(ls *R1.fastq.gz))

# fastp and fastqc loop 
for i in ${array1[@]}; do
    fastp --in1 ${i} \
        --in2 $(echo ${i}|sed s/_R1/_R2/)\
        --out1 /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/trimmed_qual.${i} \
        --out2 /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/trimmed_qual.$(echo ${i}|sed s/_R1/_R2/) \
        --detect_adapter_for_pe \
        --qualified_quality_phred 30 \
        --trim_poly_g \
        --trim_front1 15 \
        --trim_front2 15
    fastqc /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/trimmed_qual.${i}
    fastqc /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/trimmed_qual.$(echo ${i}|sed s/_R1/_R2/)
done

echo "Read trimming of adapters complete." $(date)

# Quality Assessment of Trimmed Reads
cd /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/ #go to output directory

# Compile MultiQC report from FastQC files 
multiqc --interactive ./  

echo "Cleaned MultiQC report generated." $(date)
```

```
sbatch scripts/fastp_qual_multiqc.sh
```

## Trimmed (fastp with q >30) MultiQC Report

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_qual_fastp_multiqc/multiqc_report.html /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/trimmed_qual_fastp_multiqc_report_Oyst_Nut_RNA.html
```

Full report here: [link](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_qual_fastp_multiqc_report_Oyst_Nut_RNA.html)

and here: [link](https://github.com/hputnam/Cvir_Nut_Int/blob/master/output/RNASeq/trimmed_qual_fastp_multiqc_report_Oyst_Nut_RNA.html)

Going to proceed with the original trimming with the less stringent quality control ("trimmed_fastp_multiqc" directory) becuase the sequences were longer overall and the extra quality control did not change any of the FastQC graphs or metrics by a significant amount. Trimming notes from above:
- Still some wavy-ness at the beginning of the R1 reads
- There is a little drop-off in quality at the end of reads, but not too significant. We could trim the ends if desired
- Overrepresented seqs increased after trimming
- Everything else generally looked better
- Still need to figure out the batch effects....
- **I am also confused because on the [github repo](https://github.com/hputnam/Cvir_Nut_Int) it says that these were sent for 2x150bp sequencing, but the initial files are 101 bp.**
  - "The 36 metatranscriptomic libraries were sequenced using a half lane of Illumina NovaSeq S4 chemistry to obtain 2x150 bp paired-end reads at the Yale Center for Genome Analysis."

## Genome download

Download genome file and gff file: [C. virginica genome](https://www.ncbi.nlm.nih.gov/genome/398)

```
mkdir /data/putnamlab/shared/Oyst_Nut_RNA/references
cd /data/putnamlab/shared/Oyst_Nut_RNA/references
wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/002/022/765/GCF_002022765.2_C_virginica-3.0/GCF_002022765.2_C_virginica-3.0_genomic.fna.gz
gunzip GCF_002022765.2_C_virginica-3.0_genomic.fna.gz

wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/002/022/765/GCF_002022765.2_C_virginica-3.0/GCF_002022765.2_C_virginica-3.0_genomic.gff.gz 
gunzip GCF_002022765.2_C_virginica-3.0_genomic.gff.gz
```

## Alignment of trimmed reads to genome, based on [Emma's script](https://github.com/emmastrand/EmmaStrand_Notebook/blob/master/_posts/2022-02-03-KBay-Bleaching-Pairs-RNASeq-Pipeline-Analysis.md)

Hisat2 arugments:

-  -p 8  #use 8 processors
- --dta #Report alignments tailored for transcript assemblers including StringTie
- --rna-strandness RF #see note below
- -x Cvir_ref #basename of the index for the reference genome
- -1 ${i} #R1 trimmed files
- -2 $(echo ${i}|sed s/_R1/_R2/) #R2 trimmed files
- -S ${sample_name}.sam #file to write SAM alignments to

 **thought about removing " --rna-strandness RF" because the default for HIsat2 is unstranded, and even though these reads were paired-end I believe this library was unstranded but the manual is confusing here.**

```
cd /data/putnamlab/shared/Oyst_Nut_RNA
nano scripts/align.sh
```

```
#!/bin/bash
#SBATCH -t 120:00:00
#SBATCH --nodes=1 --ntasks-per-node=10
#SBATCH --export=NONE
#SBATCH --mem=100GB
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --mail-user=zdellaert@uri.edu #your email to send notifications
#SBATCH --account=putnamlab
#SBATCH --error="align_error" #if your job fails, the error report will be put in this file
#SBATCH --output="align_output" #once your job is completed, any final job report comments will be put in this file
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/

# load modules needed
module load HISAT2/2.2.1-foss-2019b #Alignment to reference genome: HISAT2
module load SAMtools/1.9-foss-2018b #Preparation of alignment for assembly: SAMtools

# index the reference genome for C. virginica output index to working directory
hisat2-build -f /data/putnamlab/shared/Oyst_Nut_RNA/references/GCF_002022765.2_C_virginica-3.0_genomic.fna ./Cvir_ref # called the reference genome (scaffolds)
echo "Referece genome indexed. Starting alingment" $(date)

# This script exports alignments as bam files
# sorts the bam file because Stringtie takes a sorted file for input (--dta)
# removes the sam file because it is no longer needed

array=($(ls /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/*fastq.gz)) # call the clean sequences - make an array to align

for i in ${array[@]}; do
        sample_name=`echo $i| awk -F [.] '{print $2}'`
        hisat2 -p 8 --rna-strandness RF --dta -x Cvir_ref -1 ${i} -2 $(echo ${i}|sed s/_R1/_R2/) -S ${sample_name}.sam
        samtools sort -@ 8 -o ${sample_name}.bam ${sample_name}.sam
                echo "${i} bam-ified!"
        rm ${sample_name}.sam
done
```

```
sbatch scripts/align.sh
```

### To view mapping percentages

```
module load SAMtools/1.9-foss-2018b #Preparation of alignment for assembly: SAMtools

for i in *.bam; do
    echo "${i}" >> mapped_reads_counts_Cvir
    samtools flagstat ${i} | grep "mapped (" >> mapped_reads_counts_Cvir
done
```

#### Results: Average mapping 80.87%% for DB samples, 81.63% for NS samples

- took 8 hours

![mapped_Cvir.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/mapped_Cvir.png?raw=true)

## Assemble + quantify transcripts (script in progress)

Stringtie

Arguments:
- Also output a file with the gene abundances
- -p 8 #use 8 processors
- -e #Expression estimation mode (-e), exclude novel genes, no "novel" transcript assemblies (isoforms) will be produced
- -B #enables the output of Ballgown input table files (*.ctab) containing coverage data for the reference transcripts given with the -G option
- -G #Use reference annotation gff or gff3 file

```
cd /data/putnamlab/shared/Oyst_Nut_RNA
mkdir Stringtie
nano scripts/assemble.sh
```

```
#!/bin/bash
#SBATCH -t 500:00:00
#SBATCH --nodes=1 --ntasks-per-node=1
#SBATCH --export=NONE
#SBATCH --mem=128GB
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --mail-user=zdellaert@uri.edu #your email to send notifications
#SBATCH --account=putnamlab
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/               
#SBATCH --error="%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output="%x_output.%j" #once your job is completed, any final job report comments will be put in this file

module load StringTie/2.1.4-GCC-9.3.0 #new version for next time: StringTie/2.2.1-GCC-11.2.0

# Transcript assembly: StringTie

array1=($(ls *.bam)) #Make an array of sequences to assemble

for i in ${array1[@]}; do
    sample_name=`echo $i| awk -F [_] '{print $1"_"$2"_"$3}'`
    stringtie -p 8 -e -B -G /data/putnamlab/shared/Oyst_Nut_RNA/references/GCF_002022765.2_C_virginica-3.0_genomic.gff -A ../../Stringtie/${sample_name}.gene_abund.tab -o ../../Stringtie/${sample_name}.gtf ${i}
    echo "StringTie assembly for seq file ${i}" $(date)
done

echo "Stringtie alignment complete" $(date)
```

```
sbatch scripts/assemble.sh
```
Took about ~1 hour

*new version of Stringtie for next time: StringTie/2.2.1-GCC-11.2.0*



**New modele load for gff compare: GffCompare/0.12.6-GCC-11.2.0**

## Gene count matrix using PrepDE

This step uses a script called prepDE.py that can be downloaded from the [Stringtie github repository](https://github.com/gpertea/stringtie/blob/master/prepDE.py) and uploaded to andromeda into your scripts folder or copy-pasted into a new script as shown below

```
cd /data/putnamlab/shared/Oyst_Nut_RNA
cp /data/putnamlab/zdellaert/Pdam-TagSeq/scripts/prepDE.py scripts/ #copy this from other directory 
#nano scripts/prepDE.py #paste in code from github page above
```

```
nano scripts/prepDE.sh #make script for running this code, enter text in next code chunk
```

```
#!/bin/bash
#SBATCH -t 120:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --export=NONE
#SBATCH --mem=200GB
#SBATCH --mail-type=BEGIN,END,FAIL #email you when job starts, stops and/or fails
#SBATCH --mail-user=zdellaert@uri.edu #your email to send notifications
#SBATCH --account=putnamlab              
#SBATCH --error="prepDE_error" #if your job fails, the error report will be put in this file
#SBATCH --output="prepDE_output" #once your job is completed, any final job report comments will be put in this file
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/Stringtie

#load packages
module load GCCcore/9.3.0 #I needed to add this to resolve conflicts between loaded GCCcore/7.3.0 and GCCcore/9.3.0
module load Python/2.7.15-foss-2018b #Python
module load StringTie/2.1.4-GCC-9.3.0 #Transcript assembly: StringTie
module load GffCompare/0.12.6-GCC-11.2.0 #Transcript assembly QC: GFFCompare

#make gtf_list.txt file
ls *.gtf > gtf_list.txt

stringtie --merge -e -p 8 -G /data/putnamlab/shared/Oyst_Nut_RNA/references/GCF_002022765.2_C_virginica-3.0_genomic.gff -o Cvir_merged.gtf gtf_list.txt #Merge GTFs 
echo "Stringtie merge complete" $(date)

gffcompare -r /data/putnamlab/shared/Oyst_Nut_RNA/references/GCF_002022765.2_C_virginica-3.0_genomic.gff -G -o merged Cvir_merged.gtf #Compute the accuracy 
echo "GFFcompare complete, Starting gene count matrix assembly..." $(date)

#Note: the merged part is actually redundant and unnecessary unless we perform the original stringtie step without the -e function and perform
#re-estimation with -e after stringtie --merge, but will redo the pipeline later and confirm that I get equal results.

#make gtf list text file
for filename in *bam.gtf; do echo $filename $PWD/$filename; done > listGTF.txt

python ../scripts/prepDE.py -g Cvir_gene_count_matrix.csv -i listGTF.txt #Compile the gene count matrix

echo "Gene count matrix compiled." $(date)
```

Had to add -e to stringtie --merge function, Emma, Danielle, Kevin, Ariana and Sam did not do this

I used the same version of Stringtie as in the Stringtie.sh script in case there would be any inconsistencies, but next time will use the updated module (*StringTie/2.2.1-GCC-11.2.0*).

Done. Output:

> 67891 reference transcripts loaded.
> 
> 37 duplicate reference transcripts discarded.
> 
> 67872 query transfrags loaded.

> Stringtie merge complete Fri Mar 10 08:08:58 EST 2023
> 
> GFFcompare complete, Starting gene count matrix assembly... Fri Mar 10 08:09:11 EST 2023
> 
> Gene count matrix compiled. Fri Mar 10 08:09:53 EST 2023

Stats: (merged.stats)

![merged.stats.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/merged.stats.png?raw=true)

## Export gene count matrix report to computer using scp and upload results to [Github repo](https://github.com/hputnam/Cvir_Nut_Int/blob/master/output/RNASeq/Cvir_gene_count_matrix.csv)

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/Stringtie/Cvir_gene_count_matrix.csv /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/Cvir_gene_count_matrix.csv
```