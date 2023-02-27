---
layout: post
title: Point Judith Oyster RNAseq  QC
date: '2023-02-27 06:00:00'
categories: Analysis
tags: [RNA, OysterPaper]
---

# Point Judith Oyster RNAseq Initial QC : https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Point-Judith-RNAseq-QC/

## Location of data:

```
/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA
```

*Symlinked all those files and renamed the symlinks to distinguish between NS and DB: path:*
```
/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all
```

## Trimming Data

```
cd /data/putnamlab/shared/Oyst_Nut_RNA/
mkdir data/trimmed
cd /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all
gunzip * #unzip all files
```

```
nano scripts/trimmomatic.sh
```

Used this script for trimming [by Jill!!](https://github.com/JillAshey/SedimentStress/blob/master/Bioinf/RNASeq_pipeline_HI.md), fastqc_raw.sh :

```
#!/bin/bash
#SBATCH -t 18:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --export=NONE
#SBATCH --mem=100GB
#SBATCH --mail-type=BEGIN,END,FAIL # sends email to below email when job starts, finishes, or fails
#SBATCH --mail-user=zdellaert@uri.edu # your email
#SBATCH --account=putnamlab # putnamlab account
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/scripts # output directory for error/output files
#SBATCH --error="trimmomatic_error" # error reports go here
#SBATCH --output="trimmomatic_out" # other script outputs go here

module load Trimmomatic/0.38-Java-1.8

for file in /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all/*.fastq
do
        java -jar $EBROOTTRIMMOMATIC/trimmomatic-0.38.jar SE -phred33 $file $file.trim.fq ILLUMINACLIP:/data/putnamlab/jillashey/Francois_data/Hawaii/data/Illumina_adapter_reads_PE_SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:20 >> amtTrimmed.txt
done
```

Run script:
```
$ cd /data/putnamlab/shared/Oyst_Nut_RNA/scripts
$ sbatch trimmomatic.sh
$ cd /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all
$ mv *trim.fq /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed
```

## Post-trim fastqc on files

Used this script for fastqc [by Jill!!](https://github.com/JillAshey/SedimentStress/blob/master/Bioinf/RNASeq_pipeline_HI.md), fastqc_raw.sh :

```
mkdir /data/putnamlab/shared/Oyst_Nut_RNA/fastqc_results/trimmed/
mkdir /data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results/trimmed/
nano fastqc_trimmed.sh
```

```
#!/bin/bash
#SBATCH -t 18:00:00
#SBATCH --nodes=1 --ntasks-per-node=20
#SBATCH --export=NONE
#SBATCH --mem=100GB
#SBATCH --mail-type=BEGIN,END,FAIL # sends email to below email when job starts, finishes, or fails
#SBATCH --mail-user=zdellaert@uri.edu # your email
#SBATCH --account=putnamlab # putnamlab account
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/scripts # output directory for error/output files
#SBATCH --error="fastqc_trimed_out_raw_error" # error reports go here
#SBATCH --output="fastqc_trimmed_out_raw" # other script outputs go here

module load FastQC/0.11.8-Java-1.8

for file in /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed/*.fastq.gz
do
fastqc $file --outdir /data/putnamlab/shared/Oyst_Nut_RNA/fastqc_results/trimmed/
done
```

Run script:
```
$ cd /data/putnamlab/shared/Oyst_Nut_RNA/scripts
$ sbatch fastqc_trimmed.sh
```

Perform MultiQC

```
$ module load MultiQC/1.9-intel-2020a-Python-3.8.2
$ multiqc /data/putnamlab/shared/Oyst_Nut_RNA/fastqc_results/trimmed/*fastqc.zip  -o /data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results/trimmed/
```

## Trimmed MultiQC Report

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results/trimmed/multiqc_report.html /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/trimmed_multiqc_report.html
```

Full report here: _____

## Trimming with fastp, [an alternative](https://github.com/emmastrand/EmmaStrand_Notebook/blob/master/_posts/2022-02-03-KBay-Bleaching-Pairs-RNASeq-Pipeline-Analysis.md)

```
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
#SBATCH -D /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all               
#SBATCH --error=../"%x_error.%j" #if your job fails, the error report will be put in this file
#SBATCH --output=../"%x_output.%j" #once your job is completed, any final job report comments will be put in this file

# Load modules needed 
module load fastp/0.19.7-foss-2018b
module load FastQC/0.11.8-Java-1.8
module load MultiQC/1.9-intel-2020a-Python-3.8.2

# Make an array (list) of sequences to trim
# Needs to be in directory above (raw data directory)
array1=($(ls *.fastq.gz))

# fastp and fastqc loop 
for i in ${array1[@]}; do
    fastp --in1 ${i} \
        --in2 $(echo ${i}|sed s/_R1/_R2/)\
        --out1 /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.${i} \
        --out2 /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.$(echo ${i}|sed s/_R1/_R2/) \
        --qualified_quality_phred 20 \
        --unqualified_percent_limit 10 \
        --length_required 100 \
        --detect_adapter_for_pe \
        --cut_right cut_right_window_size 5 cut_right_mean_quality 20
    fastqc /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.${i}
done

echo "Read trimming of adapters complete." $(date)

# Quality Assessment of Trimmed Reads
cd /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/ #The following command will be run in the /clean directory

# Compile MultiQC report from FastQC files 
multiqc --interactive ./  

echo "Cleaned MultiQC report generated." $(date)
```

## Trimmed (fastp) MultiQC Report

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results/trimmed_fastp_multiqc/multiqc_report.html /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/trimmed_fastp_multiqc_report.html
```

Full report here: _____


## Next steps:
