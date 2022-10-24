---
layout: post
title: 2022-10-24 ENCORE RNA and DNA Extractions
date: '2022-10-24 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE]
---

## RNA and DNA Extractions for ENCORE Project, October 24, 2022

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 3 samples from ENCORE Project. These samples were collected in Bermuda in August 2022 for the ENCORE TPC project. There are 160 samples total from the following 4 species: *Diploria labyrinthiformis* (DLAB), *Montastraea cavernosa* (MCAV), *Madracis decactis* (MDEC), and *Porites astreoides* (PAST)

## Samples

Today I am trying to homogenize the sample by bead-beating using [Kevin Wong's protocol](https://kevinhwong1.github.io/KevinHWong_Notebook/20201027-DNA-RNA-Extractions-Porites-July-Bleaching-Experiment/) here:

> Sample Preparation and Digestion
>
> 1. Add 0.25 mL of glass beads (0.5mm) and add 500 μl of RNA/DNA shield into each empty centrifuge tube.
> 2. Take samples out from -80 °C on dry ice.
> 3. Using sterile clippers, add 0.25mm of tissue into the centrifuge tube with beads and RNA/DNA shield.
> 4. Vortex at max speed for 2 minutes.
> 5. Remove 400 μl of the supernatant and transfer to a new centrifuge tube.
> 6. Centrifuge at 9000 rcf for 3 minutes.
> 7. Transfer 300 μl supernatant to a new centrifuge tube and discard the pellet.
> 8. Add 30 μl of Proteinase K digestion buffer (10:1 ratio of sample:digestion buffer), and 15 μl of Proteinase K (2:1 ratio of digestion buffer:Proteinase K) to each sample.
> 9. Vortex and spin down.
> 10. Add 345 μl of lysis buffer.
> 11. Continue with DNA and RNA extraction protocol

![22022-10-24-tubes.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-24-tubes.JPG?raw=true)
![2022-10-24-caps.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-24-caps.JPG?raw=true)

## Notes

- Followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly.

- I followed Kevin's bead-beating protocol as written at the end of my [last notebook entry](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/ENCORE-RNA-DNA-Extractions-2022-10-17/). I added 0.25 mL of glass 0.5mm beads to a clean screw-top 1.5 mL tube and added one of the fragments (to the tube with none of the sample DNA/RNA shield and trying to minimize mucus carry-over) with **500** of clean DNA/RNA shield. Then, I bead-beat using a vortexer on high speed for **3** minutes. Then, I removed 400 uL of the supernatant into a clean 1.5 mL tube and spun down at 9,000 rcf for 3 minutes. Then, I removed 300 uL of the supernatant into a clean tube and proceeded with the ProK digestion as written in the protocol.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 189.35 (S1) & 23403.63 (S2)

| colony_id | Species              | Temp.Cat | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|--------------------- |----------|------------|------------|--------------|
| Past-A5   | *Porites astreoides* | 22       | 5.06       | 4.88       | 4.97         |
| Past-E2   | *Porites astreoides* | 40       | 10.5       | 10.2       | 10.35        |
| Past-F6   | *Porites astreoides* | 26       | 5.88       | 5.74       | 5.81         |

 RNA Standards: 419.78 (S1) & 9776.84 (S2)

| colony_id | Species              | Temp.Cat | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|----------------------|----------|------------|------------|--------------|
| Past-A5   | *Porites astreoides* | 22       | nd         | nd         | 0            |
| Past-E2   | *Porites astreoides* | 40       | nd         | nd         | 0            |
| Past-F6   | *Porites astreoides* | 26       | nd         | nd         | 0            |

## DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2022-10-24-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2022-10-24-gel.JPG?raw=true)

## Next steps

Yay. Still not working!

Some posibilities that are totally different approaches instead of tiny tweaks

- bead-beat in lysis buffer instead of DNA/RNA shield
  - Basing this off of the [Zymo Quick RNA protocol](https://files.zymoresearch.com/protocols/_r1054_r1055_quick-rna_miniprep_kit.pdf) (as opposed to the Quick DNA/RNA protocol) which suggests homogenizing tissue in Lysis buffer. I will take fragments out of the DNA/RNA shield, submerge in lysis buffer + beads, and then bead beat? Then will take 400 uL of the supernatant and skip the Pro K digestion.
- **Alternatively, I could also increase the amount of lysis buffer. Instead of 1:1, I could do add 500 ul to the 345 uL of sample + proK mixture.**
- According to Kevin, 55ºC heating is not recommended by Zymo anymore, so I will no longer be trying to optimize that step. Kevin recommends optimizing the centrifugation after ProK digestion to remove symbiont cells.
