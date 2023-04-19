---
layout: post
title: 2023-04-11 Heron Island Pdam Species ID (mtORF confirmation)
date: '2023-04-11 16:00:00'
categories: Processing
tags: [DNA, Pocillopora damicornis, Pocillopora]
---

## Heron Island Pdam Species ID (mtORF confirmation) of samples that were originally not able to be amplified via PCR and Sanger Sequencing

See [base protocol and notes from Hollie](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/SpeciesID-via-PCR-Sanger-Sequencing.md)

Followed [my PCR Protocol exactly](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/PCR-Protocol), based on instruction from Kristina Terpis

## Sample List: RF16, RF24, RS02, RS11

| colony_id | Extraction Date | Tech | Primerset | PCR Date  |
|-----------|-----------------|------|-----------|-----------|
| RF16A     | 20221111        | ZD   | mtORF     | 4/12/2023 |
| RF24B     | 20221102        | ZD   | mtORF     | 4/12/2023 |
| RS02C     | 20221118        | ZD   | mtORF     | 4/11/2023 |
| RS11D     | 20221111        | ZD   | mtORF     | 4/11/2023 |

### Amplification of 4 POC samples with mtORF on 4/11/2023.

Positive control: Kristina's E5 extracted DNA Tube #383 (POC 45).

#### DNA and RNA Quality Check: 1% [Gel](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Gel-Protocol/) at 80V for 30 mins.

![2023-04-11-gel-HeronPdam.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-04-11-gel-HeronPdam.JPG?raw=true)

(cropped from large gel with E5 samples, for original gel image see: (https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/originals/2023-04-11-gel-orig.JPG)

Had to redo RF16 and RF24 on 4/12/23

![2023-04-12-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-04-12-gel.JPG?raw=true)

#### Qubit Values:

| colony_id | Qubit 1 | Qubit 2 | Qubit AVG | Nanodrop |
|-----------|---------|---------|-----------|----------|
| RF16A     | 13.40   | 13.40   | 13.40     | 113.30   |
| RF24B     | 15.70   | 15.70   | 15.70     | 109.90   |
| RS02C     | 6.82    | 7.28    | 7.05      | 90.10    |
| RS11D     | 9.22    | 9.54    | 9.38      | 88.60    |

## Heron Island Pdam POC mtORF cleaned PCR products (ZD61-68) will be sent for sequencing on 4/18/2023.

**SET UP USING QUBIT VALUES, so did not dilute the PCR product.**

| colony_id | Extraction Date | Tech | Primerset | PCR Date  | PCR Notes | GSC Sanger Date | GSC Sample #1 | GSC Sample #2 |
|-----------|-----------------|------|-----------|-----------|-----------|-----------------|---------------|---------------|
| RF16A     | 20221111        | ZD   | mtORF     | 4/12/2023 |           | 4/18/2023       | ZD61_230418   | ZD62_230418   |
| RF24B     | 20221102        | ZD   | mtORF     | 4/12/2023 |           | 4/18/2023       | ZD63_230418   | ZD64_230418   |
| RS02C     | 20221118        | ZD   | mtORF     | 4/11/2023 |           | 4/18/2023       | ZD65_230418   | ZD66_230418   |
| RS11D     | 20221111        | ZD   | mtORF     | 4/11/2023 |           | 4/18/2023       | ZD67_230418   | ZD68_230418   |


| Sample ID | Well (GSC use only) | Template type | A. Template size (bases) | B. Template stock conc. (ng/ul) | C. PCR template: ng needed = ((A/100)*1.25)*2 | D. PCR template: Volume=(C/B)ul | E. Plasmid template: volume= (200ng/B)*2 | F. Volume PCR H20 needed (10-D or E) | G. Volume primer needed 1ul per rxn | Colony  |
|-----------|---------------------|---------------|--------------------------|---------------------------------|-----------------------------------------------|---------------------------------|------------------------------------------|--------------------------------------|-------------------------------------|---------|
| 61 |  | PCR | 1000 | 7.05 | 25 | 3.5 |  | 6.5 | 2 | RS02C |
| 62 |  | PCR | 1000 | 7.05 | 25 | 3.5 |  | 6.5 | 2 | RS02C |
| 63 |  | PCR | 1000 | 9.38 | 25 | 2.7 |  | 7.3 | 2 | RS11D |
| 64 |  | PCR | 1000 | 9.38 | 25 | 2.7 |  | 7.3 | 2 | RS11D |
| 65 |  | PCR | 1000 | 13.4 | 25 | 1.9 |  | 8.1 | 2 | RF16A |
| 66 |  | PCR | 1000 | 13.4 | 25 | 1.9 |  | 8.1 | 2 | RF16A |
| 67 |  | PCR | 1000 | 15.7 | 25 | 1.6 |  | 8.4 | 2 | RF24B |
| 68 |  | PCR | 1000 | 15.7 | 25 | 1.6 |  | 8.4 | 2 | RF24B |