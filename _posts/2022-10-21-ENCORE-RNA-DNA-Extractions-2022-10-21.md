---
layout: post
title: 2022-10-21 ENCORE RNA and DNA Extractions
date: '2022-10-21 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE]
---

## RNA and DNA Extractions for ENCORE Project, October 21, 2022

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 2 samples from ENCORE Project. These samples were collected in Bermuda in August 2022 for the ENCORE TPC project. There are 160 samples total from the following 4 species: *Diploria labyrinthiformis* (DLAB), *Montastraea cavernosa* (MCAV), *Madracis decactis* (MDEC), and *Porites astreoides* (PAST)

## Samples

Testing different extraction methods for PAST samples.

- Test 1: Using less of the sample DNA/RNA shield (100 uL) in the initial ProK digestion **and** heating to 55ºC for 60 minutes during the ProK digestion.
- Test 2: Bead-beating using a **modified version** of [Kevin Wong's protocol](https://kevinhwong1.github.io/KevinHWong_Notebook/20201027-DNA-RNA-Extractions-Porites-July-Bleaching-Experiment/) here:

> Sample Preparation and Digestion
>
> 1. Add 0.25 mL of glass beads (0.5mm) and add 500 μl of RNA/DNA shield into each empty centrifuge tube.
> 2. Take samples out from -80 °C on dry ice.
> 3. Using sterile clippers, add 0.25mm of tissue into the centrifuge tube with beads and RNA/DNA shield. **Add 200 uL of the sample DNA/RNA shield to the tube**
> 4. Vortex at max speed for 2 minutes.
> 5. Remove 400 μl of the supernatant and transfer to a new centrifuge tube.
> 6. Centrifuge at 9000 rcf for 3 minutes.
> 7. Transfer 300 μl supernatant to a new centrifuge tube and discard the pellet.
> 8. Add 30 μl of Proteinase K digestion buffer (10:1 ratio of sample:digestion buffer), and 15 μl of Proteinase K (2:1 ratio of digestion buffer:Proteinase K) to each sample.
> 9. Vortex and spin down.
> 10. Add 345 μl of lysis buffer.
> 11. Continue with DNA and RNA extraction protocol

![22022-10-21-tubes.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-21-tubes.JPG?raw=true)
![2022-10-21-caps.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-21-caps.JPG?raw=true)

## Notes

- Followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly.

- I did two extractions per tube. For one, of those extractions, I took 100 uL of the DNA/RNA shield from the sample tube and added 200 uL of clean DNA/RNA shield before proceeding with the extraction as written. Then I heated these at 55ºC for 60 minutes during the ProK digestion step.

- For the second extraction, I followed Kevin's bead-beating protocol as written at the end of my [last notebook entry](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/ENCORE-RNA-DNA-Extractions-2022-10-17/). I added 0.25 mL of glass 0.5mm beads to a clean screw-top 1.5 mL tube and added 200 of the sample DNA/RNA shield with **500** (on 10/19/22 I only added 200 uL) of clean DNA/RNA shield. Then, I bead-beat using a vortexer on high speed for 2 minutes. Then, I removed 400 uL of the supernatant into a clean 1.5 mL tube and spun down at 9,000 rcf for 3 minutes. Then, I removed 300 uL of the supernatant into a clean tube and proceeded with the ProK digestion as written in the protocol.

- The heated to 55 ºC extraction for PAST-D1 had issues:

  - The pellet was very loose after spinning down after the ProK/heating step. 
  - The supernatant was still very viscous here, and was not mixing well with the lysis buffer.
  - The RNA filter was pigmented throughout the extraction.
  - The RNA was pigmented at the end of the extraction.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 189.15 (S1) & 23503.13 (S2)

| colony_id | Species                         | Temp.Cat | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|---------------------------------|----------|------------|------------|--------------|
| Past-C6, heated      | *Porites astreoides* | 26       | nd         | nd         | 0            |
| Past-C6, bead-beat   | *Porites astreoides* | 26       | 3.00       | 2.92       | 2.96         |
| Past-D1, heated      | *Porites astreoides* | 29       | 2.18       | 2.08       | 2.13         |
| Past-D1, bead-beat   | *Porites astreoides* | 29       | 7.98       | 7.80       | 7.89         |

 RNA Standards: 417.59 (S1) & 9757.72 (S2)

| colony_id            | Species              | Temp.Cat | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|----------------------|----------------------|----------|------------|------------|--------------|
| Past-C6, heated      | *Porites astreoides* | 26       | nd         | nd         | 0            |
| Past-C6, bead-beat   | *Porites astreoides* | 26       | nd         | nd         | 0            |
| Past-D1, heated      | *Porites astreoides* | 29       | nd         | nd         | 0            |
| Past-D1, bead-beat   | *Porites astreoides* | 29       | nd         | nd         | 0            |

## DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2022-10-21-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2022-10-21-gel.JPG?raw=true)

## Next steps