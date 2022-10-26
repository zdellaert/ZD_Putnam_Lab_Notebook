---
layout: post
title: 2022-10-26 ENCORE RNA and DNA Extractions
date: '2022-10-26 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE]
---

## RNA and DNA Extractions for ENCORE Project, October 26, 2022

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 3 samples from ENCORE Project. These samples were collected in Bermuda in August 2022 for the ENCORE TPC project. There are 160 samples total from the following 4 species: *Diploria labyrinthiformis* (DLAB), *Montastraea cavernosa* (MCAV), *Madracis decactis* (MDEC), and *Porites astreoides* (PAST)

## Samples

![22022-10-26-tubes.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-26-tubes.JPG?raw=true)
![2022-10-26-caps.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-26-caps.JPG?raw=true)

## Notes

Today I tried 3 different methods with the hope of narrowing in on the problem with the Porites. I am no longer trying the 55 ºC heating step during the proteinase K digestion as discussed in my "Next Steps" section in my [last extraction post](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/ENCORE-RNA-DNA-Extractions-2022-10-24/). I am also trying today to elute in 50 uL of RNAse free water instead of 100 uL to try to bump up the concentration of RNA in case it is there and we just can't see it on the gel. In this case, I re-apply the 50 uL from the first elution to the membrane for a second elution instead of adding another clean 50 uL of DNAse/RNAse free water.

- Protocol 1 (Bead-beat, or BB): Bead-beating with 750 uL of clean DNA/RNA shield. To a tube with 750 uL of DNA/RNA shield and ~0.2 mL of 0.5 mm glass beads, I add the fragment from the tube with sterilized forceps. Bead beat for 2 minutes. Briefly spin down and remove 400 uL of the supernatant to a clean tube. Spin this at 12,000 rcf for 3 minutes and then remove 300 uL of the supernatant to a clean tube. Proceed with proK digestion and extraction as descibed in the protocol linked below.

- Protocol 2 (2X Lysis Buffer, or 2XL):

- Other than the adjustments mentioned above, I followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 184.60 (S1) & 21839.64 (S2)

| colony_id | Species              | Temp.Cat | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|----------------------|----------|------------|------------|--------------|
| Past-A3, bead-beat   | *Porites astreoides* | 33       | 4.48       | 4.4        | 4.44         |
| Past-B4, bead-beat   | *Porites astreoides* | 16       | 19.3       | 19.3       | 19.3         |
| Past-C5, bead-beat   | *Porites astreoides* | 22       | 3.36       | 3.2        | 3.28         |
| Past-A3,2X Lysis Buffer   | *Porites astreoides* | 33       | nd         | nd         | 0            |
| Past-B4,2X Lysis Buffer   | *Porites astreoides* | 16       | 2.2        | 2.12       | 2.16         |
| Past-C5,2X Lysis Buffer   | *Porites astreoides* | 22       | nd         | nd         | 0            |
| Past-A3   | *Porites astreoides* | 33       | nd         | nd         | 0            |
| Past-B4   | *Porites astreoides* | 16       | 2.02       | 2          | 2.01         |
| Past-C5   | *Porites astreoides* | 22       | nd         | nd         | 0            |

RNA Standards: 417.18 (S1) & 9518.56 (S2)

| colony_id | Species              | Temp.Cat | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|----------------------|----------|------------|------------|--------------|
| Past-A3, bead-beat   | *Porites astreoides* | 33       | nd         | nd         | 0            |
| Past-B4, bead-beat   | *Porites astreoides* | 16       | 18.4       | 18         | 18.2         |
| Past-C5, bead-beat   | *Porites astreoides* | 22       | nd         | nd         | 0            |
| Past-A3,2X Lysis Buffer   | *Porites astreoides* | 33       | 11.6       | 11.6       | 11.6         |
| Past-B4,2X Lysis Buffer   | *Porites astreoides* | 16       | 15.6       | 15.6       | 15.6         |
| Past-C5,2X Lysis Buffer   | *Porites astreoides* | 22       | nd         | nd         | 0            |
| Past-A3   | *Porites astreoides* | 33       | 13.6       | 13.2       | 13.4         |
| Past-B4   | *Porites astreoides* | 16       | 14.4       | 14.2       | 14.3         |
| Past-C5   | *Porites astreoides* | 22       | nd         | nd         | 0            |

## DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2022-10-26-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2022-10-26-gel.JPG?raw=true)

## Next steps

- No longer want to elute with 55ºC heated water. Just in case this is causing any degredation.
