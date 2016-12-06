---
layout: post
title: Geoduck RRBS Library Prep
date: '2016-12-01'
categories: Processing
tags: [shellfish, P. generosa, methylation, RRBS, DNA]
---

Prepping RRBS libraries for geoduck juvenile OA acclimatization study.

## 20161201
Chose 12 samples from a single time point (Day 10, 3 treatments * 4 replicates) for the first sequencing library preps. 100ng was used as the starting amount of DNA for each sample and the volume of water in each reaction was adjusted as necessary. 0.5% unmethylated lambda DNA was spiked in (w/w DNA) to determine conversion efficiency by estimating the error rate at which a C count occurs at an unmethylated C position

# Step 1 MSPI DNA Cutting
MSPI restriction endonuclease in NEBuffer2

* MspI - 25,000U (NEB cat: R0106L)
* NEBuffer2 10x (NEB cat: B7002S)

## Reaction Mix
* Samples were mixed as follows to a total reaction volume of 30µl. Samples were incubated at 37°C starting at 15:00 
* Lambda DNA (581ng/µl) was diluted 1:1160 for a concentration of 0.5ng/µl and 1µl added to each sample
* Unmethylated lamda phage DNA (Promega cat: D1501)

	* 3µl NEBuffer2
	* 1µl MSPI 20U/µl
	* 16µl DNA (100ng)
	* 10µl of H20
	* 30µl total


 **EPI.Tube.Num**    |**Tank**    | **Treatment**            | **DNA.Extraction**|         **DNA.Conc.ng.µl**    |**vol.for.100ng** |    **lambda.0.5%**     |**Water.µl**     |**NSBuffer2.µl**     |**MSPI.µl**
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
EPI_103    |Tank11     |Low    |              20161028 |        18.3 |       5.5 |    1 |    19.5 |    3  |    1
EPI_104    |Tank11     |Low    |           20161007 |      9.28 |          10.8 |    1 |    14.2 |    3  |    1
EPI_111    |Tank12     |Super.Low    |              20161007 |     55.6 |         1.8 |    1 |    23.2 |    3  |    1
EPI_113    |Tank12     |Super.Low    |            20161007 |        18.8 |       5.3 |    1 |    19.7 |    3  |    1
EPI_119    |Tank13     |Ambient    |             20161007 |        17.6 |        5.7 |    1 |    19.3 |    3  |    1
EPI_120    |Tank13     |Ambient    |           20161007 |      16.5 |       6.1 |    1 |    18.9 |    3  |    1
EPI_127    |Tank14     |Low    |        20161004 |       35.2 |          2.8 |    1 |    22.2 |    3  |    1
EPI_128    |Tank14     |Low     |         20161004 |      29.8     |3.4 |    1     |21.6     |3  |    1
EPI_135    |Tank15     |Ambient     |        20161004 |        20.2 |          5 |    1 |    20 |    3  |    1
EPI_136    |Tank15     |Ambient     |         20161004 |        18.2 |        5.5 |    1 |    19.5 |    3  |    1
EPI_143    |Tank16     |Super.Low     |         20161028 |      41.2 |         2.4 |    1 |    22.6 |    3  |    1
EPI_145    |Tank16     |Super.Low     |        20161007 |        9.64 |        10.4 |    1 |    14.6 |    3  |    1

### Step 1 conclusions

* no errors were seen on the PCR machine. Samples assumed to have been cut with MSPI

# Step 2 Bisulfite conversion
* Removed from incubator at 09:45 on 20161202
* Proceeded with EZ DNA Methylation-Gold Kit (Catalog Nos. D5005 & D5006)
[EZ DNA Methylation-Gold Manual](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/DNA_Methylation_Gold_Bisulfite_d5005i.pdf)

### Samples
Added additional samples to compare RRBS above with whole genome library preps

 **EPI.Tube.Num**    |**Tank**    | **Treatment**            | **DNA.Extraction**|         **DNA.Conc.ng.µl**    |**vol.for.100ng** |    **lambda.0.5%**     |**Water.µl**     
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
EPI_111    |Tank12     |Super.Low    |              20161007 |     55.6 |         1.8 |    1 |    27.2 |  
EPI_128    |Tank14     |Low     |         20161004 |      29.8     |3.4 |    1     |25.6     |
EPI_135    |Tank15     |Ambient     |        20161004 |        20.2 |          5 |    1 |    24.0 |  


* EPI_111 - Whole Genome sample, no MSPI cutting
* EPI_128 - Whole Genome sample, no MSPI cutting 
* EPI_135 - Whole Genome sample, no MSPI cutting

### Bisulfite conversion kit prep

* Prepared the **CT Conversion Reagent** for larger DNA samples (30µl) by adding 800µl of water, 300µl of M-Dilution and 50µl of M-Dissolving

* Added 30µl of sample described in table to 120 µl of **CT Conversion Reagent**, mixed by flicking, and spun down
* Placed tubes in PCR machine at 10:45 and set as follows:
	* 98°C for 10 min
	* 64°C for 2.5 hours
	* 4°C forever

* followed protocol steps [EZ DNA Methylation-Gold Manual](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/DNA_Methylation_Gold_Bisulfite_d5005i.pdf)

* Eluted in 12µl of elution buffer

* 1µl was used to quantify the samples on the nanodrop

**Sample.ID** | **ng/µl**
---|---
EPI_103 | 18.06
EPI_104 | 19.39
EPI_111 | 19.43
EPI_113 | 18.76
EPI_119 | 18.83
EPI_120 | 20.48
EPI_127 | 21.31
EPI_128 | 22.01
EPI_135 | 21.56
EPI_136 | 20.35
EPI_143 | 19.92
EPI_145 | 19.99
EPI_111 WG | 23.04
EPI_128 WG | 23.69
EPI_135 WG | 23.63


* 1µl was used to assess fragment size on the bioanalyzer.  

### Bisulfite converted ssDNA assessment

Expected DNA size for Gold kit (A)

![Expected DNA size](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/expected_DNAsize_truseq_meth.jpg?raw=true =400x200)

### Results of bisulfite converted samples 

[Chip 1 Data](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-02_15-14-17.pdf)

![Chip1](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/20161202_ssDNA_traces1.jpg?raw=true =400x200)


[Chip 2 Data](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-02_15-39-40.pdf)

![Chip2](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/20161202_ssDNA_traces2.jpg?raw=true =400x200)

* size quantification on sample 111-wg does not seem to be displaying correctly
* Gel marker is offset
* 
![gel offset](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/20161202_ssDNA_gel2.jpg?raw=true =200x300)


### Step 2 conclusions

* All samples are of approptiate size to continue with library prep


# Step 3 Illumina Library Prep

[Ilumina TruSeq DNA Methylation Library Preparation Guide](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/truseq-dna-methylation-library-prep-guide-15066014-a.pdf)

Illumina Adapter Sequences
Document # 1000000002694 v01 17 February 2016 
TruSeq DNA Methylation Index PCR Primers
5’ CAAGCAGAAGACGGCATACGAGAT[6 bases]GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT 

Index 1: ATCACG 
Index 2: CGATGT 
Index 3: TTAGGC 
Index 4: TGACCA 
Index 5: ACAGTG 
Index 6: GCCAAT 
Index 7: CAGATC 
Index 8: ACTTGA 
Index 9: GATCAG 
Index 10: TAGCTT 
Index 11: GGCTAC 
Index 12: CTTGTA 

Illumina library prep was completed according to manufacturer's instructions with modifications as described in red text on the protocol and listed below.

* samples eluted in 12µl post BS conversion
* 200µl of 80% ethanol used for rinsing beads
* Samples were stored at -20 for ~24h between _Purify the Tagged DNA_ and _Amplify the Library and Add an Index_ steps
* Library prep was started 20161202
* Library prep was finished 20121204
* Individual barcodes were used for each sample from the Illumina TruSeq DNA Methylation Index PCR Primers (10 reactions, 12 indexes Cat #: EGIDX81312)


**Sample.ID** | **Index.Number** | **Index.Sequence**
---|---|---
EPI_103 | 1 | ATCACG
EPI_104 | 2 | CGATGT
EPI_111 | 3 | TTAGGC
EPI_113 | 4 | TGACCA
EPI_119 | 5 | ACAGTG
EPI_120 | 6 | GCCAAT
EPI_127 | 7 | CAGATC 
EPI_128 | 8 | ACTTGA
EPI_135 | 9 | GATCAG
EPI_136 | 10 | TAGCTT
EPI_143 | 11 | GGCTAC
EPI_145 | 12 | CTTGTA
EPI_111 WG | 1 | ATCACG
EPI_128 WG | 2 | CGATGT
EPI_135 WG | 3 | TTAGGC

### Library Quantification
20161205
Libraries were quantified on the Qubit using the dsDNA High Sensitivity Kit


**Sample.ID** | **ng/µl**
---|---
EPI_103 | 4.34
EPI_104 | 4.80
EPI_111 | 5.46
EPI_113 | 4.88
EPI_119 | 5.10
EPI_120 | 4.58
EPI_127 | 4.58
EPI_128 | 4.80
EPI_135 | 4.08
EPI_136 | 3.70
EPI_143 | 2.88
EPI_145 | 2.92
EPI_111 WG | 3.40
EPI_128 WG | 4.12
EPI_135 WG | 2.24


# Library Quality 
Libraries were not concentrated enough to measure using Agilent DNA 12000 kit 20161204
* 1µl of sample was used for each and no data were visible with DNA 12000 kit

20161205

* 1.0µl of each sample was run on the Agilent DNA High Sensitivity Kit
* A few diluted DNA samples were also run in extra cells to view original DNA with more resolution

Illumina DNA Methylation kit expected library size on high sensitivity chip
![expected size](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/expected_librarysize_truseq_meth_.jpg?raw=true =400x200)

[Chip 1 Data](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_High_Sensitivity_DNA_Assay_DE72902486_2016-12-05_15-09-17.pdf)

![RRBS Library Chip 1](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/20161205_RRBS_library_traces1.JPG?raw=true =300x200)

* EPI_103
* EPI_104
* EPI_111
* EPI_113
* EPI_119
* EPI_120
* EPI_127
* EPI_128
* EPI_135
* EPI_136
* EPI_143
* EPI_1451

[Chip 2](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_High_Sensitivity_DNA_Assay_DE72902486_2016-12-05_15-57-57.pdf)

![RRBS Library Chip 2](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/20161205_RRBS_library_traces1.JPG?raw=true =300x200)

* EPI_145
* EPI_111 WG
* EPI_128 WG
* EPI_135 WG
* EPI_103 DNA Diluted 1:1
* EPI_104 DNA Diluted 1:1
* EPI_111 DNA Diluted 1:10
* EPI_113 DNA Diluted 1:1
* EPI_119 DNA Diluted 1:1
* EPI_128 DNA Diluted 1:3
* EPI_135 DNA Diluted 1:3


* Original DNA samples overloaded the chip sensitivity and data are not useful






