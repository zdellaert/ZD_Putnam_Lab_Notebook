---
layout: post
title: 2022-10-19 ENCORE RNA and DNA Extractions
date: '2022-10-19 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE]
---

## RNA and DNA Extractions for ENCORE Project, October 19, 2022

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 2 samples from ENCORE Project. These samples were collected in Bermuda in August 2022 for the ENCORE TPC project. There are 160 samples total from the following 4 species: *Diploria labyrinthiformis* (DLAB), *Montastraea cavernosa* (MCAV), *Madracis decactis* (MDEC), and *Porites astreoides* (PAST)

## Samples

Testing different extraction methods for PAST samples.

- Test 1: Using less of the sample DNA/RNA shield (100 uL) in the initial ProK digestion
- Test 2: Bead-beating using [Kevin Wong's protocol](https://kevinhwong1.github.io/KevinHWong_Notebook/20201027-DNA-RNA-Extractions-Porites-July-Bleaching-Experiment/) here:

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

![22022-10-19-tubes.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-19-tubes.JPG?raw=true)
![2022-10-19-caps.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-19-caps.JPG?raw=true)

## Notes

- Followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly.

- I did two extractions per tube. For one, of those extractions, I took 100 uL of the DNA/RNA shield from the sample tube and added 200 uL of clean DNA/RNA shield before proceeding with the extraction as written.

- For the second extraction, I followed Kevin's bead-beating protocol as written at the end of my [last notebook entry](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/ENCORE-RNA-DNA-Extractions-2022-10-17/). I added 0.25 mL of glass 0.5mm beads to a clean screw-top 1.5 mL tube and added 200 of the sample DNA/RNA shield with 200 of clean DNA/RNA shield. Then, I bead-beat using a vortexer on high speed for 2 minutes. Then, I removed 400 uL of the supernatant (to achieve this, I needed to add another 100 uL of clean DNA/RNA shield, so in the future I will add 300 uL of clean DNA/RNA shield at the beginning instead of 200 uL) into a clean 1.5 mL tube and spun down at 9,000 rcf for 3 minutes. Then, I removed 300 uL of the supernatant into a clean tube and proceeded with the ProK digestion as written in the protocol.

- Throughout the RNA extraction, the filters of two bead-beat samples were pigmented. So were the final RNA for those tubes.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 190.31 (S1) & 21981.24 (S2)

| colony_id | Species              | Temp.Cat | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|----------------------|----------|------------|------------|--------------|
| Past-A6   | *Porites astreoides* | 26       | 2.34       | 2.26       | 2.3          |
| Past-A6, bead-beat   | *Porites astreoides* | 26       | 5.38       | 5.26       | 5.32         |
| Past-C1   | *Porites astreoides* | 29       | 2.48       | 2.38       | 2.43         |
| Past-C1, bead-beat   | *Porites astreoides* | 29       | 11.1       | 10.9       | 11           |

 RNA Standards: 417.20 (S1) & 9353.57 (S2)

| colony_id | Species              | Temp.Cat | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|----------------------|----------|------------|------------|--------------|
| Past-A6   | *Porites astreoides* | 26       | nd         | nd         | 0            |
| Past-A6, bead-beat   | *Porites astreoides* | 26       | nd         | nd         | 0            |
| Past-C1   | *Porites astreoides* | 29       | nd         | nd         | 0            |
| Past-C1, bead-beat   | *Porites astreoides* | 29       | 11.4       | 11.2       | 11.3         |

## DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2022-10-19-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2022-10-19-gel.JPG?raw=true)

## Next steps

- As mentioned in the "Notes" section above, if I bead-beat again I will use 300 uL of clean DNA/RNA shield (or a different combination of clean and sample DNA/RNA shield) to achieve a final volume of 500 uL in the bead-beating tube.

- I am still disappointed by the quantity of RNA... 

- RNA is still pigmented, especially from the bead-beat samples which also had colored RNA filters. Maybe bead-beating is still an option with less of the sample DNA/RNA shield.

Here is an image of the two PAST-A6 final RNA tubes, with the bead-beat sample on the right.
![2022-10-19-RNA-A6.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-19-RNA-A6.JPG?raw=true)

Here is an image of the two PAST-C1 final RNA tubes, with the bead-beat sample on the right.
![2022-10-19-RNA-C1.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-19-RNA-C1.JPG?raw=true)