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

## Trimming Data and performing trimmed multiQC

Used this script [by Emma!!](https://github.com/emmastrand/EmmaStrand_Notebook/blob/master/_posts/2022-02-03-KBay-Bleaching-Pairs-RNASeq-Pipeline-Analysis.md), fastp_multiqc.sh :

**We took out the following because they are less consistent - less adapter content issues and proper trimming.**

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
        --detect_adapter_for_pe \
        --trim_poly_g \
        --trim_front1 15 \
        --trim_front2 15
    fastqc /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/trimmed.${i}
done

echo "Read trimming of adapters complete." $(date)

# Quality Assessment of Trimmed Reads
cd /data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/ #The following command will be run in the /clean directory

# Compile MultiQC report from FastQC files 
multiqc --interactive ./  

echo "Cleaned MultiQC report generated." $(date)
```

```
sbatch scripts/fastp_multiqc.sh
```

## Trimmed FastQC example

![DB_Sample1_R1_fastqc_perbaseseqcont.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/DB_Sample1_R1_fastqc_perbaseseqcont.png?raw=true)

![trimmed_DB_Sample1_R1_fastqc_perbaseseqcont.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_DB_Sample1_R1_fastqc_perbaseseqcont.png?raw=true)

![DB_Sample1_R1_fastqc_perbaseseqqual.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/DB_Sample1_R1_fastqc_perbaseseqqual.png?raw=true)

![trimmed_DB_Sample1_R1_fastqc_perbaseseqqual.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_DB_Sample1_R1_fastqc_perbaseseqqual.png?raw=true)

![DB_Sample1_R1_fastqc_overrepseqs.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/DB_Sample1_R1_fastqc_overrepseqs.png?raw=true)

![trimmed_DB_Sample1_R1_fastqc_overrepseqs.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_DB_Sample1_R1_fastqc_overrepseqs.png?raw=true)


## Trimmed (fastp) MultiQC Report

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/data/trimmed_fastp_multiqc/multiqc_report.html /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/trimmed_fastp_multiqc_report_Oyst_Nut_RNA.html
```

Full report here: https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/trimmed_fastp_multiqc_report_Oyst_Nut_RNA.html



## Next steps:


Download genome file
C. virginica genome (the reference we will be using): https://www.ncbi.nlm.nih.gov/genome/398.

$ wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/002/022/765/GCF_002022765.2_C_virginica-3.0/GCF_002022765.2_C_virginica-3.0_genomic.fna.gz into desired directory.

fna = FastA format file containing Nucleotide sequence (DNA)


Mapping

etc

:-)