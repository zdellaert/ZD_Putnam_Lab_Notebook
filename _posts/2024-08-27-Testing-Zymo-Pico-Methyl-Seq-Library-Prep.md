---
layout: post
title: Testing Pico Methyl-Seq Library Prep
date: '2024-08-27'
categories: Protocols
tags: [RNA, Pocillopora, Porites, LCM, Library Prep]
---

## Testing NEBNext Low Input RNA Library Prep

Product: [Zymo Pico Methyl Seq Library Prep](https://www.zymoresearch.com/products/pico-methyl-seq-library-prep-kit)

I am basing my test off of [Jill's protocol](https://github.com/JillAshey/JillAshey_Putnam_Lab_Notebook/blob/master/_posts/2024-06-13-Zymo-Pico-Methyl-Seq-Library-Prep.md), and you can also see [Zymo's protocol here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manual_picomethylseq.pdf) and the general [Putnam Lab protocol here](https://github.com/meschedl/MESPutnam_Open_Lab_Notebook/blob/master/_posts/2020-09-18-WGBS-PMS-protocol.md).

### Here's the Pico Methyl-Seq library prep workflow: 

![](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manual_picomethylseq.png)

### Materials 

- [Kit contents](https://www.zymoresearch.com/products/pico-methyl-seq-library-prep-kit)
- PCR tubes 
- Thermocycler 
- Heating block 
- Mini centrifuge
- Vortex 
- Aluminum beads (to keep things on ice)
- Magnetic stand for PCR tubes 
- 1.5 mL tubes 
- Shaker

#### Kit contents

| Pico Methyl-Seq™ Library Prep Kit | D5456 (25 preps) | Storage Temperature  |
|-----------------------------------|------------------|----------------------|
| Lightning Conversion Reagent      | 3 tubes          | Room Temp.           |
| M-Binding Buffer                  | 20 ml            | Room Temp.           |
| M-Wash Buffer*                    | 6 ml (conc.)     | Room Temp.           |
| L-Desulphonation Buffer           | 10 ml            | Room Temp.           |
| DNA Elution Buffer                |  2 ml            | Room Temp.           |
| PrepAmp Polymerase (13 U/μL)      |  15 ul           |       -20 °C         |
| PrepAmp Buffer (5X)               |  75 µl           |       -20 °C         |
| PrepAmp Primer (40 μM)            |  30 µl           |       -20 °C         |
| PrepAmp Pre-Mix                   |  120 µl          |       -20 °C         |  
| DNase/RNase-Free Water            |  1 ml            | Room Temp.           |
| Zymo-Spin™ IC Columns             | 100              | Room Temp.           |
| Collection Tubes                  |  100             | Room Temp.           |
| DNA Binding Buffer                |  25 ml           | Room Temp.           |
| DNA Wash Buffer                   |  6 ml (conc.)    | Room Temp.           |
| LibraryAmp Master Mix (2X)        |  625 µl          |       -20 °C         |  
| LibraryAmp Primers (10 μM)        |  30 µl           |       -20 °C         |
| Index Primer Sets - 6 Sets(10 μM) |  30 µl           |       -20 °C         |  


## Protocol

See Jill: https://github.com/JillAshey/JillAshey_Putnam_Lab_Notebook/blob/master/_posts/2024-06-13-Zymo-Pico-Methyl-Seq-Library-Prep.md

## Samples: Starting library prep 8/28/24

Just going to start with two, and then will try again and see if I need to pool RNA or anything.

- POR:
  - #14, [7/24 Charm Extraction](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2024-07-24-LCM-20240718-DNA-Extractions-Charm-Try-2.md)
  - ![2024-07-24-gel-Charm.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-24-gel-Charm.JPG?raw=true)
- POC:
  -  #22, [7/30 Zymo Extraction](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2024-07-30-LCM-20240718-RNA-DNA-Extractions-Zymo-Try-3.md)
  - ![2024-07-30-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-30-gel.JPG?raw=true)

### Protocol notes

In section 4, I used 9 cycles for 10 ng input and 12 cycles for 1 ng input samples.

### FINISHED SUCCESSFUL LIBRARY PREP

![2024-08-28.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-28.JPG?raw=true)

![2024-08-28-POR-1ng.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-28-POR-1ng.JPG?raw=true)
![2024-08-28-POR-10ng.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-28-POR-10ng.JPG?raw=true)
![2024-08-28-POC-1ng.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-28-POC-1ng.JPG?raw=true)
![2024-08-28-POC-10ng.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-28-POC-10ng.JPG?raw=true)

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-28.pdf)

| sample_id     | tapestation concentration | ng Library  (conc * 14 uL) |
|---------------|---------------------------|----------------------------|
| POR_14, 1ng   |  5.74                  | 80.36       |
| POR_14, 10 ng | 10.8                  | 151.2       |
| POC_22, 1 ng  |  6.36                  | 89.04       |
| POC_22, 10ng  | 4.62                  | 64.68       |
