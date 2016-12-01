---
layout: post
title: Oly Oyster DNA Methylation Analysis
date: '2016-11-25'
categories: Analysis
tags: [Bioinformatics, shellfish, O. lurida, methylation]
---


Using Bismark to extract CpG methylation information from _Ostrea lurida_ sequence data [Oly Oyster Methylation Project](https://github.com/hputnam/Oly_Oyster_DNA_Methylation)

Bismark Bisulfite Mapper [V0.16.3](https://rawgit.com/FelixKrueger/Bismark/master/Docs/Bismark_User_Guide.html) "Bismark is a program to map bisulfite treated sequencing reads to a genome of interest and perform methylation calls in a single step"

[Bismark: a flexible aligner and methylation caller for Bisulfite-Seq applications](https://www.ncbi.nlm.nih.gov/pubmed/21493656)

requires bowtie/bowtie2, samtools, perl

To detect methylation, DNA is treated with sodium bisulfite, which leaves methylated cytosines intact, but converts unmethylated cytosines to uracil and further PCR amplification converts uracil to thyamine.  By mapping the bisulfite treated DNA to a reference genome, the location and percent methylation of the reads at any CpG (and other contexts) can be determined realtive to T.

## Step 1 - Genome Preparation

* bismark_genome_preparation
	* initial genome preparation requires a fasta file and path to the folder that contains he genome fasta file.  The prep creates two files, one that converts C->T  and the other that converts G->A (equivalent to a C-to-T conversion on the reverse strand). These files are indexed with bowtie and are then ready for mapping of bisulfite read data.

## Step 2 - Sequence Mapping

* bismark
* 	Use bowtie to align and map reads to the converted reference genome. Bisulfite treatment and subsequent PCR amplification can result in four individual strands of DNA which all have the potential to end up in the sequence data. The four possibilities are aligned and bismark can then determine the strand origin of each read, so bismark can handle sequence data from both directional and non-directional library preps. The output of the bismark call includes  a line for every read with mapping position, stand of alignment, read sequence, genomic sequence, and methylation call.
	* sample_bismark.bam (contains all alignments plus methylation call strings) 
	* sample_bismark_SE_report.txt (contains alignment and methylation summary)

	
## Step 3 - Methylation Data Extraction

* bismark_methylation_extractor
* Determine the methylation state of each cytosine position in the sequence data. The expectation is primarily CpG, but CHG and CHH context is also common in plants and all contexts can be determined. The extaction output files contain one line per cytosine, with "+"" indicating methylated cytosine and "-" indicating non-methylated cytosine
* OT = original top strand
* OB = orignal bottom strand

If all contexts are examined the output is split into multiple files * CpG_OT_sample_bismark.bt2.txt* CpG_OB_sample_bismark.bt2.txt* CHG_OT_sample_bismark.bt2.txt* CHG_OB_sample_bismark.bt2.txt* CHH_OT_sample_bismark.bt2.txt* CHH_OB_sample_bismark.bt2.txt* sample_splitting_report.txt* sample_M-bias.txt
## Step 4 - Summarize Methylation Data
* bismark2summary


# 20161125 Running Bismark on 18 Oly MBD samples

## Step 1 

* Completed successfully

## Step 2 

* Completed successfully with ~3% mapping on average
* sorted and converted bam files to sam files and found data in scaffolds > scaffold number 10,000 (which was the problem with BSMap, no data in scaffolds with scaffold number >10,000)
## Step 3 Issues
* bismark_methylation_extractor will not output coverage file beacsue it dies in sorting in memory of the gazillion scaffolds
```%%bash
/Users/hollie/Documents/BioInf_Programs/bismark_v0.16.3/bismark_methylation_extractor \
-s \
--gazillion \
--merge_non_CpG \
--bedGraph \
--zero_based \
--buffer_size 4G \
/Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/zr1394_1_cleaned_all_bismark_bt2_sorted.bam \
--output /Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted```


## Error Message
> Using these input files: /Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted/CpG_OT_zr1394_1_cleaned_all_bismark_bt2_sorted.txt /Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted/CpG_OB_zr1394_1_cleaned_all_bismark_bt2_sorted.txt /Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted/Non_CpG_OT_zr1394_1_cleaned_all_bismark_bt2_sorted.txt /Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted/Non_CpG_OB_zr1394_1_cleaned_all_bismark_bt2_sorted.bam.txt

> **Summary of parameters for bismark2bedGraph conversion**

> ======================================================
* bedGraph output:		zr1394_1_cleaned_all_bismark_bt2_sorted.bedGraph.gz
* output directory:		/Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted/<
* remove whitespaces:		no
* CX context:			no (CpG context only, default)
* No-header selected:		no
* Sorting method:			Unix sort-based (smaller memory footprint, but slower)
* Sort buffer size:		4G
* Coverage threshold:		1

=============================================================================
> **Methylation information will now be written into a bedGraph and coverage file**

> =============================================================================

>Using the following files as Input:
Writing bedGraph to file: zr1394_1_cleaned_all_bismark_bt2_sorted.bedGraph.gz
Also writing out a coverage file including counts methylated and unmethylated residues to file: zr1394_1_cleaned_all_bismark_bt2_sorted.bismark.cov.gz
Also writing out a 0-based, half-open coverage file including counts methylated and unmethylated residues to file: zr1394_1_cleaned_all_bismark_bt2_sorted.bedGraph.gz.bismark.zero.cov

>Changed directory to /Users/hollie/Documents/Oly_Oyster_DNA_Methylation/Data/MBD/Bismark_Output/Methy_extract_sorted/
The genome of interest was specified to contain gazillions of chromosomes or scaffolds. Merging all input files and sorting everything in memory instead of writing out individual chromosome files...
Writing all merged methylation calls to temp file zr1394_1_cleaned_all_bismark_bt2_sorted.bedGraph.gz.methylation_calls.merged

> Finished writing methylation calls from CpG_OT_zr1394_1_cleaned_all_bismark_bt2_sorted.txt to merged temp file
Finished writing methylation calls from CpG_OB_zr1394_1_cleaned_all_bismark_bt2_sorted.txt to merged temp file
Sorting input file zr1394_1_cleaned_all_bismark_bt2_sorted.bedGraph.gz.methylation_calls.merged by positions (using -S of 4G)
**_sort: stray character in field spec: invalid field specification `3,3V'
Died at /Users/hollie/Documents/BioInf_Programs/bismark_v0.16.3/bismark2bedGraph line 485._**
Finished BedGraph conversion ...

* **no coverage files to veiw or load into methylkit analysis pipeline**


# Methylkit issue
### Tried to skip methylation extraction by loading the bam or sam files directly into R using methylkit function **_processBismarkAln()_** 

* Process crashes R

file.list <- list("zr1394_1_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_2_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_3_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_4_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_5_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_6_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_7_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_8_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_9_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_10_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_11_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_12_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_13_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_14_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_15_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_16_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_17_cleaned_all_bismark_bt2_sorted.sam",
"zr1394_18_cleaned_all_bismark_bt2_sorted.sam")

sample.id <- list("hc1_2B",
 "hc1_4B",
 "hc2_15B",
 "hc2_17",
 "hc3_1",
 "hc3_5",
 "hc3_7",
 "hc3_10",
 "hc3_11",
 "ss2_9B",
 "ss2_14B",
 "ss2_18B",
 "ss3_3B",
 "ss3_14B",
 "ss3_15B",
 "ss3_16B",
 "ss3_20",
 "ss5_18")
 
 treatment <- c(0,0,0,0,0,0,0,0,0,1,1,1,1,1,1,1,1,1)
 
 myobj <- processBismarkAln(file.list, sample.id, assembly="10K", treatment=treatment)
 
* **The processBismarkAln call crashes the kernel in the R notebook, Have tried this on bam and sorted sam and bam**


