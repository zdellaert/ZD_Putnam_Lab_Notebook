
---
layout: post
title: Geoduck RRBS Testing
date: '2016-11-28'
categories: Processing
tags: [Bioinformatics, shellfish, P. generosa, methylation, RRBS]
---


Testing RRBS protocol using MSPI, BS treatment, and Illumina Trueseq DNA methylation kit

MSPI enzyme cuts between Cs at CCGG sites in the genome. When bisulfite treatment is used after cutting, data can be gathered from the beginning of the read CG and at other CGs within the sequence read lenght (~100bp). This cutting and conversion creates the imput material for the library prep. The concern is that the  Illumina Trueseq DNA methylation kit was optimized for whole genome library prep and the DNA following the MSPI cutting and BS treatmetn might have the wrong size and quantitify of frgaments to generate good deqeuncing results. 

I am testing this process with 3 samples with 1µg of DNA from each.

# Step 1 MSPI cutting

Mix the following and incubate overnight at 37°C.

**Reagents** | **Epi 272**	|**Epi 298**	|**Epi 42**
---| --- | --- | ---NEBuffer2 10x |	3µl |	3µl |	3µl MSPI 20U/µl	| 1µl |	1µl |	1µl H20|	16.5µl	|13.5µl|	13.3µl1µg DNA|	9.5µl	|12.5µl	|12.7µltotal|	30µl|	30µl|	30µl
# Step 2 BS treatment
EZ DNA Methylation-GoldTM Kit Catalog Nos. D5005 & D5006
Eluted in 10µl and repeated elution in another 10µl

Ran RNA Pico chip to quant ssDNA following bisulfite conversion
[BS converson results](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_ssBS_DNA_2016-11-30_14-51-01.pdf)

comparision of the same sample is highlighted in yellow. MSPI cutting and lambda DNA addtion (top), MSPI cutting and no lambda DNA addtion (middle), Genomic DNA, no cutting, and lambda DNA addtion (bottom).

![sample comparison](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/20161130_ssBSDNA_trace_comparison.jpg?raw=true)

The peaks in my samples are ~700bp, whereas the image from the illumina prep guide shows a a peak at ~1000
![sample comparison](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/expected_DNAsize_truseq_meth.jpg?raw=true)