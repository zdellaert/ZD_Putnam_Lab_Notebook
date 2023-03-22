---
layout: post
title: 2023-03-15 E5 ACR Deep Dive RNA and DNA Extractions
date: '2023-03-15 16:00:00'
categories: Processing
tags: [DNA, RNA, E5, Porites, Pocillopora]
---

# E5 Species ID (POC and POR) via PCR and Sanger Sequencing

See [base protocol and notes from Hollie](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/blob/master/protocols/SpeciesID-via-PCR-Sanger-Sequencing.md)

Master Mix Information

[EmeraldAmp® GT PCR Master Mix Cat # RR310A RR310B](https://www.takarabio.com/documents/User%20Manual/RR310A_DS.v1902Da-a_116982.pdf)


For all primer sets below, I used the same reaction formula:

| Master Mix 25 uL reaction |                                   |
|---------------------------|-----------------------------------|
| 12.55                     | Emerald Master Mix                |
| 10.8                      | Nuclease Free Water               |
| 0.32                      | 10µM working stock of For Primer (10 uM) |
| 0.32                      | 10µM working stock of Rev Primer (10 uM) |
| 1.00                      | DNA Template                      |
| 25                        | Total Volume                      |

This is based on a 33 uL formula from Kristina:

For all primer sets below, I used the same reaction formula:

| Master Mix 33 uL reaction |                                   |
|---------------------------|-----------------------------------|
| 16.66                     | Emerald Master Mix                |
| 14.66                     | Nuclease Free Water               |
| 0.43                      | 10µM working stock of For Primer (10 uM) |
| 0.43                      | 10µM working stock of Rev Primer (10 uM) |
| 1                         | DNA Template                      |
| 33.18                     | Total Volume                      |

## Primer Dilution from Hydrated Primers (200 uM) to 10 uM

25 uL of 200 uM primer + 475 uL H2O

## _Pocillopora_

### mtORF

#### Reference
[Johnston et al PeerJ mtORF](https://peerj.com/articles/4355/)

#### mtORF Primers 
FatP6.1 5′-TTTGGGSATTCGTTTAGCAG-3′    
RORF 5′-SCCAATATGTTAAACASCATGTCA-3′

#### mtORF PCR profile:  
1 cycle: 94 °C for 60 s   
40 cycles: 94 °C for 30 s, 53 °C for 30 s, and 72 °C for 75 s   
1 cycle: 72 °C for 5 min.  

[Notebook Example](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/mtORF-protocol/)

### PocHistone 3 region

DNA from individuals of mtORF type 1 (P. meandrina and P. eydouxi) need also to be amplified using novel primers for the histone 3 region 

#### Reference
[Johnston et al PeerJ PocHistone](https://peerj.com/articles/4355/)

#### PocHistone Primers
PocHistoneF: 5′-ATTCAGTCTCACTCACTCACTCAC-3′ 
PocHistoneR: 5′-TATCTTCGAACAGACCCACCAAAT-3′

#### PocHistone PCR profile:  
1 cycle: 94 °C for 60 s   
40 cycles: 94 °C for 30 s, 53 °C for 30 s, and 72 °C for 60 s   
1 cycle: 72 °C for 5 min.

## _Porites_

### Coral nuclear histone region spanning H2A to H4 (H2)

#### Reference
[Tisthammer et al PeerJ 2020 nuclear histone region](https://peerj.com/articles/8550/)

#### H2 Primers
zH2AH4f 5′-GTGTACTTGGCTGCYGTRCT-3′    
zH4Fr 5′-GACAACCGAGAATGTCCGGT-3′

expected band size ∼1,500 bp   
coral nuclear histone region spanning H2A to H4 (H2) with novel primers 

#### H2 PCR profile:  
1 cycle: 96 °C for 2 min   
34 cycles: 96 °C for 20 s, 58.5 °C for 20 s, and 72 °C for 90 s   
1 cycle: 72 °C for 5 min.    


## Sample List: All POC and POR colonies from the E5 timeseries need to be ID'd at one of the timepoints.

### Starting with Site 1

| n.  | timepoint | collection_site | colony_id | Extraction Date | Tech |
|-----|-----------|-----------------|-----------|-----------------|------|
| 383 | TP2       | site1           | POC-45    | 20211001        | KXT  |
| 385 | TP2       | site1           | POC-47    | 20211012        | KXT  |
| 387 | TP2       | site1           | POC-44    | 20211105        | KXT  |
| 389 | TP2       | site1           | POC-42    | 20211116        | KXT  |
| 391 | TP2       | site1           | POC-55    | 20211118        | KXT  |
| 393 | TP2       | site1           | POC-50    | 20210903        | KXT  |
| 395 | TP2       | site1           | POC-56    | 20211028        | KXT  |
| 397 | TP2       | site1           | POC-40    | 20210927        | KXT  |
| 399 | TP2       | site1           | POC-52    | 20211102        | KXT  |
| 401 | TP2       | site1           | POC-53    | 20211118        | KXT  |
| 403 | TP2       | site1           | POC-48    | 20211129        | KXT  |
| 405 | TP2       | site1           | POC-68    | 20211001        | KXT  |
| 407 | TP2       | site1           | POC-41    | 20211015        | KXT  |
| 411 | TP2       | site1           | POC-43    | 20210902        | KXT  |
| 417 | TP2       | site1           | POC-57    | 20211020        | KXT  |

| n.  | timepoint | collection_site | colony_id | Extraction Date | Tech |
|-----|-----------|-----------------|-----------|-----------------|------|
| 415 | TP2 | site1 | POR-75 | 20210902 | KXT |
| 421 | TP2 | site1 | POR-82 | 20211008 | KXT |
| 425 | TP2 | site1 | POR-80 | 20211014 | KXT |
| 469 | TP2 | site1 | POR-83 | 20220208 | KXT |
| 471 | TP2 | site1 | POR-76 | 20211015 | KXT |
| 473 | TP2 | site1 | POR-77 | 20211116 | KXT |
| 475 | TP2 | site1 | POR-78 | 20210921 | KXT |
| 477 | TP2 | site1 | POR-69 | 20211015 | KXT |
| 479 | TP2 | site1 | POR-74 | 20211020 | KXT |
| 483 | TP2 | site1 | POR-81 | 20220208 | KXT |
| 485 | TP2 | site1 | POR-70 | 20211109 | KXT |
| 487 | TP2 | site1 | POR-71 | 20211122 | KXT |
| 489 | TP2 | site1 | POR-79 | 20211129 | KXT |
| 491 | TP2 | site1 | POR-73 | 20211101 | KXT |
| 493 | TP2 | site1 | POR-72 | 20211109 | KXT |



### DNA and RNA Quality Check: 1% [Gel](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Gel-Protocol/) at 80V for 30 mins.

No loading dye needed to add to samples because

![2023-03-14-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-03-14-gel.JPG?raw=true)


![2023-03-15-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-03-15-gel.JPG?raw=true)


## Ethanol precipitation to clean up PCR product

- Sodium acetate EtoH precipitation, protocol coming soon!


## Nanodrop of cleaned PCR product

![2023-03-15-Nanodrop-PCR-POC-E5-SpeciesID.JPG.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tables/2023-03-15-Nanodrop-PCR-POC-E5-SpeciesID.JPG.JPG?raw=true)


![2023-03-15-Nanodrop-PCR-POR-E5-SpeciesID.JPG.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tables/2023-03-15-Nanodrop-PCR-POR-E5-SpeciesID.JPG.JPG?raw=true)

## For Sanger Sequencing

### Primer Dilution from 10 uM Primer Working stock to 3.2 uM for sequencing

1.6 uL of 10 uM primer + 3.4 uL H2O = 5 uL

Make enough for # of sequencing reactions, 2uL per reaction (e.g. 35 uL for 15 samples, 30 uL plus extra for error)