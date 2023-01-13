---
layout: post
title: Point Judith Oyster RNAseq  QC
date: '2023-01-12 06:00:00'
categories: Analysis
tags: [RNA, OysterPaper]
---

# Point Judith Oyster RNAseq Initial QC

RNAseq data for Point Judith Oyster Project. Experimental and sequencing information coming soon.  

Original data lives here: /data/putnamlab/KITT/hputnam/20200119_Oyst_Nut/DB/ and /data/putnamlab/KITT/hputnam/20200119_Oyst_Nut/NS/ , but some of these files need to be re-uploaded from KITT because they were incomplete [or the files were somehow overwritten during first pass at QC - their permissions were not locked like other files in the /data/putnamlab/KITT/hputnam/ folder].

#### Make a new directory for output files

```
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA/data
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA/fastqc_results
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA/scripts
```

## Downloading RNAseq data from SRA, which were uploaded by Emma Strand in 2022

Downloaded all RNA seq files from here (https://www.ncbi.nlm.nih.gov/bioproject/PRJNA899931) using SRA tools using this tutorial (https://erilu.github.io/python-fastq-downloader/ and https://edwards.flinders.edu.au/fastq-dump/), see below:

| Seq ID | File 1              | File 2              | SRR #       |
|--------|---------------------|---------------------|-------------|
| DB 1   | Sample1_R1.fastq.gz | Sample1_R2.fastq.gz | SRR22311695 |
| DB 2   | Sample2_R1.fastq.gz | Sample2_R2.fastq.gz | SRR22311694 |
| DB 3   | Sample3_R1.fastq.gz | Sample3_R2.fastq.gz | SRR22311693 |
| DB 4   | Sample4_R1.fastq.gz | Sample4_R2.fastq.gz | SRR22311692 |
| DB 5   | Sample5_R1.fastq.gz | Sample5_R2.fastq.gz | SRR22311691 |
| DB 6   | Sample6_R1.fastq.gz | Sample6_R2.fastq.gz | SRR22311690 |
| NS 1   | Sample1_R1.fastq.gz | Sample1_R2.fastq.gz | SRR22312596 |
| NS 2   | Sample2_R1.fastq.gz | Sample2_R2.fastq.gz | SRR22312595 |
| NS 3   | Sample3_R1.fastq.gz | Sample3_R2.fastq.gz | SRR22312594 |
| NS 4   | Sample4_R1.fastq.gz | Sample4_R2.fastq.gz | SRR22312593 |
| NS 5   | Sample5_R1.fastq.gz | Sample5_R2.fastq.gz | SRR22312592 |
| NS 6   | Sample6_R1.fastq.gz | Sample6_R2.fastq.gz | SRR22312591 |

### Installing SRA tools to download SRA data

You could probably install this in andromeda, but I decided to download the files to my local machine and then upload to andromeda using scp to minimize connection timeout issues and since I am new to installing things on andromeda and didn't know the best practices re: permissions :).

First, go to [this website](https://github.com/ncbi/sra-tools/wiki/02.-Installing-SRA-Toolkit) and download the binary for your operating system (I downloaded Mac OS X). Follow the installation instructions for your OS. This is what I did:

1. Download binary to my home directory
2. In terminal, in my home directory, I ran the following lines of code (**note, I had to change the code slightly from the tutorial to match the numbers of the version I actually downloaded**):

```
$ tar -vxzf sratoolkit.current-mac64.tar.gz
$ export PATH=$PATH:$PWD/sratoolkit.3.0.2-mac64/bin
$ source ~/.zshrc #I needed to do this to get my computer to recognize the new path
$ which fastq-dump #A test to make sure your computer can now find the code.
```

3. I had some permissions issues with my computer not wanting to run the code, but this was easily fixed by going into System Preferences > Security and Privacy and clicking "Always Allow" after running a command that it didn't like.
4. Configuration: follow [this guide](https://github.com/ncbi/sra-tools/wiki/03.-Quick-Toolkit-Configuration) to make sure the settings are configured and set your desired default directory ("user-repository" on CACHE tab) for output files (mine is: /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut -- it needs to be a new empty directory). Save and exit.

5. Test prefetch and fastq-dump on one file before running batch script if desired:

```
$ cd /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut
$ prefetch SRR22312594
$ fastq-dump --outdir fastq --gzip --readids --dumpbase --split-3 /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut/sra/SRR22312594.sra
```

### Script for downloading SRA data using SRA tools, with known SRA numbers (format = SRR#########)

fastq_download.py : 

```
#Script modified by Z. Dellaert on Jan 11, 2023 from https://erilu.github.io/python-fastq-downloader/

import subprocess

# samples correspond to DB 1, DB 2, DB 3, DB 4, DB 5, DB 6, NS 1, NS 2, NS 3, NS 4, NS 5, and NS 6
sra_numbers = ["SRR22311695", "SRR22311694", "SRR22311693", "SRR22311692", "SRR22311691", "SRR22311690", "SRR22312596", "SRR22312595", "SRR22312594", "SRR22312593", "SRR22312592", "SRR22312591"]

# this will download the .sra files to /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut/fastq/
for sra_id in sra_numbers:
    print ("Currently downloading: " + sra_id)
    prefetch = "prefetch " + sra_id
    print ("The command used was: " + prefetch)
    subprocess.call(prefetch, shell=True)

# this will extract the .sra files from above into a folder named 'fastq'
for sra_id in sra_numbers:
    print ("Generating fastq for: " + sra_id)
    fastq_dump = "fastq-dump --outdir fastq --gzip --readids --dumpbase --split-3  /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut/sra/" + sra_id + ".sra"
    print ("The command used was: " + fastq_dump)
    subprocess.call(fastq_dump, shell=True)
```

**Run the script**

```
$ cd /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut
$ mkdir fastq
$ python fastq_download.py
```

This took about 3.5 hours!

Then, I renamed the files so that they matched the original naming scheme found in the metadata files, and separated them into DB and NS files to match the original scheme.

```
$ cd /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut/fastq
$ mkdir DB
$ mkdir NS
$ mv SRR22311* DB/
$ mv SRR22312* NS/
$ nano rename_SRR.sh
```

rename_SRR.sh :

```
#!/bin/bash

### These are the DB ones

mv SRR22311695_1.fastq.gz Sample1_R1.fastq.gz 
mv SRR22311695_2.fastq.gz Sample1_R2.fastq.gz
mv SRR22311694_1.fastq.gz Sample2_R1.fastq.gz
mv SRR22311694_2.fastq.gz Sample2_R2.fastq.gz
mv SRR22311693_1.fastq.gz Sample3_R1.fastq.gz 
mv SRR22311693_2.fastq.gz Sample3_R2.fastq.gz
mv SRR22311692_1.fastq.gz Sample4_R1.fastq.gz
mv SRR22311692_2.fastq.gz Sample4_R2.fastq.gz
mv SRR22311691_1.fastq.gz Sample5_R1.fastq.gz 
mv SRR22311691_2.fastq.gz Sample5_R2.fastq.gz
mv SRR22311690_1.fastq.gz Sample6_R1.fastq.gz
mv SRR22311690_2.fastq.gz Sample6_R2.fastq.gz

### These are the NS ones

mv SRR22312596_1.fastq.gz Sample1_R1.fastq.gz 
mv SRR22312596_2.fastq.gz Sample1_R2.fastq.gz
mv SRR22312595_1.fastq.gz Sample2_R1.fastq.gz
mv SRR22312595_2.fastq.gz Sample2_R2.fastq.gz
mv SRR22312594_1.fastq.gz Sample3_R1.fastq.gz 
mv SRR22312594_2.fastq.gz Sample3_R2.fastq.gz
mv SRR22312593_1.fastq.gz Sample4_R1.fastq.gz
mv SRR22312593_2.fastq.gz Sample4_R2.fastq.gz
mv SRR22312592_1.fastq.gz Sample5_R1.fastq.gz 
mv SRR22312592_2.fastq.gz Sample5_R2.fastq.gz
mv SRR22312591_1.fastq.gz Sample6_R1.fastq.gz
mv SRR22312591_2.fastq.gz Sample6_R2.fastq.gz
```

```
$ cd DB
$ bash ../rename_SRR.sh
$ cd ../NS
$ bash ../rename_SRR.sh
```

I wanted to write a script or loop to do this in a more elegant way but honestly I want to be very careful to ensure proper naming is consistent.... So saved this as a bash script and executed it.

**Transfer data to andromeda**

Uploaded to Andromeda using:

(on personal machine)

```
$ scp /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut/fastq/DB/* zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/DB

$ scp /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/SRA_Oyst_Nut/fastq/NS/* zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/NS
```

**Raw data are now in**

```
/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA
```

*Symlinked all those files and renamed the symlinks to distinguish between NS and DB: path:*
```
/data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all
```

Code for symlinking and renaming:
```
$ mkdir /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all
$ cd /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all

$ ln -s /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/NS/* .
$ for file in Sample*; do mv -v ${file} NS_${file}; done #name is now: NS_Sample1_R1.fastq.gz (from Sample1_R1.fastq.gz)

$ ln -s /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/DB/* . 
$ for file in Sample*; do mv -v ${file} DB_${file}; done #name is now: DB_Sample1_R1.fastq.gz (from Sample1_R1.fastq.gz)
```

Checked md5 sums and read counts 
```
$ md5sum *.fastq.gz > checkmd5.md5
$ md5sum -c checkmd5.md5
$ zgrep -c "SRR" *.fastq.gz
```


## Initial fastqc on files

Used this script for fastqc [by Jill!!](https://github.com/JillAshey/SedimentStress/blob/master/Bioinf/RNASeq_pipeline_HI.md), fastqc_raw.sh :

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
#SBATCH --error="fastqc_out_raw_error" # error reports go here
#SBATCH --output="fastqc_out_raw" # other script outputs go here

module load FastQC/0.11.8-Java-1.8

for file in /data/putnamlab/shared/Oyst_Nut_RNA/data/raw_SRA/all/*.fastq.gz
do
fastqc $file --outdir /data/putnamlab/shared/Oyst_Nut_RNA/fastqc_results/raw_SRA/all/
done
```

Run script:
```
$ cd /data/putnamlab/shared/Oyst_Nut_RNA/scripts
$ sbatch fastqc_raw.sh
```

Perform MultiQC

```
$ module load MultiQC/1.9-intel-2020a-Python-3.8.2
$ multiqc /data/putnamlab/shared/Oyst_Nut_RNA/fastqc_results/raw_SRA/all/*fastqc.zip  -o /data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results/
```

## Initial MultiQC Report

```
scp  zdellaert@ssh3.hac.uri.edu:/data/putnamlab/shared/Oyst_Nut_RNA/multiqc_results/multiqc_report.html /Users/zoedellaert/Documents/URI/Oyst_Nut_RNA/initial_multiqc_report.html
```

Full report here: https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/results/initial_multiqc_report_Oyst_Nut_RNA.html


****IMPORTANT TO NOTE — This data is the same as the KITT data but the headers are different - the data downloaded from SRA does not have the original headers in the fastq file, so fastqc does not produce the per sequence tile data point, other than this i believe the data are identical.
