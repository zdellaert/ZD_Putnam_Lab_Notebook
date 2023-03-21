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
| 0.32                      | 10µM working stock of For Primer  |
| 0.32                      | 10µM working stock of Rev Primer  |
| 1.00                      | DNA Template                      |
| 25                        | Total Volume                      |

This is based on a 33 uL formula from Kristina:

For all primer sets below, I used the same reaction formula:

| Master Mix 33 uL reaction |                                   |
|---------------------------|-----------------------------------|
| 16.66                     | Emerald Master Mix                |
| 14.66                     | Nuclease Free Water               |
| 0.43                      | 10µM working stock of For Primer  |
| 0.43                      | 10µM working stock of Rev Primer  |
| 1                         | DNA Template                      |
| 33.18                     | Total Volume                      |

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