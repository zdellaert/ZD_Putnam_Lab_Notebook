---
layout: post
title: 2022-10-31 ENCORE RNA and DNA Extractions
date: '2022-10-31 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE, Porites astreoides]
---

## RNA and DNA Extractions for ENCORE Project, October 31, 2022

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 2 samples from ENCORE Project. These samples were collected in Bermuda in August 2022 for the ENCORE TPC project. There are 160 samples total from the following 4 species: *Diploria labyrinthiformis* (DLAB), *Montastraea cavernosa* (MCAV), *Madracis decactis* (MDEC), and *Porites astreoides* (PAST)

## Samples

Forgot to take pictures, but samples were Past-C3 and Past-E3. Neither tubes were particularly pigmented.

## Notes

Today I tried adding BME (beta-mercaptoethanol) to the lysis buffer, as is directed in Zymo's Pathogen and Viral Quick RNA kits. They recommend the following procedure:

> - Add 500 μl beta-mercaptoethanol (user supplied) per 100 ml Lysis DNA/RNA Buffer, (final 0.5% (v/v)).
> - Add 400 µl of Genomic Lysis Buffer to 100 µl of blood, serum, or plasma (4:1) 3.
> - Mix completely by vortexing 4-6 seconds, then let stand 5-10 minutes at room temperature.

So, for a test batch I added 15 uL of BME to a tube with 3 mL of the DNA/RNA Lysis Buffer supplied in the kit. I used this as normal in the extraction [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/), but with **twice the amount of Lysis buffer added**, as is also recommended by the Viral and Pathogen kits. I decided to divide the extractions into two samples, one that was bead-beat and one that just used DNA/RNA shield from the sample tube.

1. For the bead-beat samples, I bead-beat a fragment from the tube in 800 uL of DNA/RNA shield, 200 uL of which came from the sample tube (see my last extraction [post](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/ENCORE-RNA-DNA-Extractions-2022-10-26/)). I took the supernatant into the extraction as written in that post.
2. For the "100 uL + BME" samples I took 100 uL from the sample DNA/RNA shield and diluted with 200 uL of clean DNA/RNA shield.

When the lysis buffer step came, I added 700 uL instead of the usual 345 uL. This meant I had to spin the flow through through multiple times.

Other than the adjustments mentioned above, I followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 195.90 (S1) & 22394.56 (S2)

| Sample #                   | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|----------------------------|------------|------------|--------------|
| Past-C3, bead-beat + BME   | nd         | nd         | 0            |
| Past-E3, bead-beat + BME   | nd         | nd         | 0            |
| Past-C3, 100 uL + BME      | nd         | nd         | 0            |
| Past-E3, 100 uL + BME      | nd         | nd         | 0            |

 RNA Standards: 409.86 (S1) & 9471.14 (S2)

| Sample #                   | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|----------------------------|------------|------------|--------------|
| Past-C3, bead-beat + BME   | nd         | nd         | 0            |
| Past-E3, bead-beat + BME   | nd         | nd         | 0            |
| Past-C3, 100 uL + BME      | nd         | nd         | 0            |
| Past-E3, 100 uL + BME      | nd         | nd         | 0            |

## DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2022-10-31-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2022-10-31-gel.JPG?raw=true)

## Next steps

Taking a step back from *Porites* extractions for a bit. We need to brainstorm if we should try a new kit or just leave these behind for now. There is clearly a little bit of DNA and some degraded RNA in the Bead-Beat samples, but the BME did not help with anything clearly. Maybe adding the 200 uL of sample DNA/RNA shield was a mistake and introduced inhibitors? Either way, we will take a break for now to brainstorm.
