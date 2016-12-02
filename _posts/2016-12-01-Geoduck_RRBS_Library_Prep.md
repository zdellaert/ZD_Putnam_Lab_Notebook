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

3µl NEBuffer2
1µl MSPI 20U/µl
16µl DNA (100ng)
10µl of H20
30µl total


 **EPI.Tube.Num**    |**Tank**    | **Treatment**         | **Homogenization**    | **DNA.Extraction**|     **DNA.QC** |    **DNA.Conc.ng.µl**    |**DNA.amount.µg**     |**vol.for.100ng** |    **lambda.0.5%**     |**Water.µl**     |**NSBuffer2.µl**     |**MSPI.µl**
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
EPI_103    |Tank11     |Low    |          20160912 |    20161028 |    20161028 |    18.3 |   2.6 |    5.5 |    1 |    19.5 |    3  |    1
EPI_104    |Tank11     |Low    |        20160912 |    20161007 |    20161010 |    9.28 |      1.3 |    10.8 |    1 |    14.2 |    3  |    1
EPI_111    |Tank12     |Super.Low    |          20160912 |    20161007 |    20161010 |    55.6 |     7.8 |    1.8 |    1 |    23.2 |    3  |    1
EPI_113    |Tank12     |Super.Low    |         20160912 |    20161007 |    20161010 |    18.8 |    2.6 |    5.3 |    1 |    19.7 |    3  |    1
EPI_119    |Tank13     |Ambient    |          20160909 |    20161007 |    20161010 |    17.6 |    2.5 |    5.7 |    1 |    19.3 |    3  |    1
EPI_120    |Tank13     |Ambient    |         20160909 |    20161007 |    20161010 |    16.5 |    2.3 |    6.1 |    1 |    18.9 |    3  |    1
EPI_127    |Tank14     |Low    |     20160909 |    20161004 |    20161010 |    35.2 |      4.9 |    2.8 |    1 |    22.2 |    3  |    1
EPI_128    |Tank14     |Low     |     20160909 |    20161004 |    20161010 |    29.8 |     4.2     |3.4 |    1     |21.6     |3  |    1
EPI_135    |Tank15     |Ambient     |    20160909 |    20161004 |    20161006 |    20.2 |      2.8 |    5 |    1 |    20 |    3  |    1
EPI_136    |Tank15     |Ambient     |     20160909 |    20161004 |    20161006 |    18.2 |    2.5 |    5.5 |    1 |    19.5 |    3  |    1
EPI_143    |Tank16     |Super.Low     |     20160909 |    20161028 |    20161028 |    41.2 |     5.8 |    2.4 |    1 |    22.6 |    3  |    1
EPI_145    |Tank16     |Super.Low     |     20160909 |    20161007 |    20161010 |    9.64 |     1.3 |    10.4 |    1 |    14.6 |    3  |    1


## 20161202

# Step 2 Bisulfite conversion
