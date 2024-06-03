---
layout: post
title: Testing Zymo cfDNA DNA Extraction on Cryosectioned and LCM-d P. acuta 
date: '2024-05-28'
categories: Processing
tags: [DNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Zymo cfDNA Kit on LCM Samples

## 5/28/24 - Extracting DNA from LCM-captured cells (LCM date 5/8/24)

Used MAGicBead™ cfDNA Isolation [Kit](https://www.zymoresearch.com/products/magicbead-cfdna-isolation-kit), [protocol](https://files.zymoresearch.com/protocols/%5BD4086%5D+MAGicBead%E2%84%A2+cfDNA+Isolation+Kit+-+Ver+1.0.0.pdf)

### Sectioning performed on 5/6/24 and LCM on 5/9/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Sample-Prep/)

#### Protocol notes:

- Followed the protocol almost exactly, but did all incubations at 56 ºC based on other Paxgene extraction protocols. Made the following notes:
  - Resuspended cells in 200 uL DNAse/RNAse free water. Flicked to mix and spun down in mini (benchtop) centrifuge for 2 minutes
  - Transferred contents to 1.5mL tube with 50uL of digestion buffer and 8uL of Proteinase K, following instructions for 200uL input
  - Vortex and spun down, incubated in thermomixer
    - 15 minutes at 55 ºC
    - 15 minutes at 37 ºC
  - Added 50 uL binding buffer and vortex, add 10 uL of resuspended beads and vortex, put on rotator for 5 minutes at 30 rpm
  - Flick tube, open cap, pellet on magnet for 2 minutes
  - Discard supernatant and remove tube from stand
  - Add 800 uL of wash buffer and transfer to clean 2 mL tube
    - did another wash of 800 uL instead of 300 uL
    - then a final 300 uL wash
  - Did two elutions of 15 uL into separate tubes, quantified seperately
- Used the following two samples
  - LCM sample #1
  - LCM sample #8

#### Qubit Results

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 62.32 (S1) & 22223.15 (S2)

| colony_id                  | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|----------------------------|------------|------------|--------------|
| LCM sample #1, Elution 1   |  0.125     | 0.122      |  0.124 ng/uL |
| LCM sample #1, Elution 2   |  nd        | nd         |  0 ng/uL     |
| LCM sample #8, Elution 1   |  0.865     | 0.850      |  0.858 ng/uL |
| LCM sample #8, Elution 2   |  0.172     | 0.174      |  0.173 ng/uL |

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

Loaded 10 uL of extracted DNA (Elution 1 only) into each well (3&5 ) -- no DNA present.

![2024-05-28-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-05-28-gel.JPG?raw=true)
