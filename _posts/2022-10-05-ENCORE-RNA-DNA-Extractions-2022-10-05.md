---
layout: post
title: 2022-10-05 ENCORE RNA and DNA Extractions
date: '2022-10-05 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE]
---

## RNA and DNA Extractions for ENCORE Project, October 05, 2022

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 10 samples from ENCORE Project. These samples were collected in Bermuda in August 2022 for the ENCORE TPC project. There are 160 samples total from the following 4 species: *Diploria labyrinthiformis* (DLAB), *Montastraea cavernosa* (MCAV), *Madracis decactis* (MDEC), and *Porites astreoides* (PAST).

## Samples:
These samples are part of our "Round A" of processing. We selected 16 samples from the 160 that were representative of all 4 species at the following 4 temperatures: 16 ºC, 26 ºC, 29 ºC, and 36 ºC. Within each species, the four samples selected for "Round A" all originated from different colonies (given by the letter after the species. For example, for sample Dlab-D1, the colony was colony D and the fragment was fragment 1.) Today, I extracted the remaining 8/16 after the [2022-10-03 extraction](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/ENCORE-RNA-DNA-Extractions-2022-10-03/) as well as re-extracting the two *Porites astreoides* (PAST) samples from that date that were unsuccessfully extracted (Past-D7 and Past-F4).

![22022-10-05-tubes.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-05-tubes.JPG?raw=true)
![2022-10-05-caps.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2022-10-05-caps.JPG?raw=true)

## Notes:
- Followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly. Took 300 uL from the sample tubes for all species except for *Porites astreoides* (PAST). For *Porites astreoides* (PAST), I took 150 uL of the DNA/RNA shield from the sample tube and added 150 uL of clean DNA/RNA shield before proceeding with the extraction as written.

- I had to centrifuge the PAST samples **Past-A1 and Past-B6** multiple times to successfully pellet the debris after the Proteinase K digestion. I found that using a P200 pipette set to 200 uL was the easiest way to remove the supernatant without disturbing the very loose pellets from the PAST samples.
- Throughout the RNA extraction, the filters of all the PAST samples were pigmented. Past-A1 had the most pigmented RNA filter column. At the end of the extractio the RNA from samples **Past-A1 and Past-F4** were pale brown.

## Qubit Results
 - Used Broad range dsDNA and RNA Qubit [Protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/)
 - All samples read twice, standard only read once

 DNA Standards: 198.66 (S1) & 24171.04 (S2)
 RNA Standards: 412.67 (S1) & 9635.27 (S2)

| **colony_id** | **Species**                   | **Temp.Cat** | **DNA_QBIT_1** | **DNA_QBIT_2** | **DNA_QBIT_AVG** | **RNA_QBIT_1** | **RNA_QBIT_2** | **RNA_QBIT_AVG** |
|-----------|---------------------------|----------|------------|------------|--------------|------------|------------|--------------|
| Dlab-A4   | *Diploria labyrinthiformis* | 16       | 5.28       | 5.08       | 5.18         | 13.6       | 13.4       | 13.5         |
| Dlab-C7   | *Diploria labyrinthiformis* | 36       | 10.1       | 9.92       | 10.01        | 11.2       | 10.2       | 10.7         |
| Mcav-E6   | *Montastraea cavernosa*     | 26       | 4.96       | 4.8        | 4.88         | 11.8       | 11.4       | 11.6         |
| Mcav-F7   | *Montastraea cavernosa*     | 36       | 12.9       | 12.8       | 12.85        | 10.6       | 10.4       | 10.5         |
| Mdec-D4   | *Madracis decactis*         | 16       | 5          | 4.78       | 4.89         | 12.8       | 12.6       | 12.7         |
| Mdec-E1   | *Madracis decactis*         | 29       | 8.06       | 8.02       | 8.04         | 22.2       | 21.8       | 22           |
| Past-A1   | *Porites astreoides*        | 29       | nd         | nd         | 0            | 12.4       | 12         | 12.2         |
| Past-B6   | *Porites astreoides*        | 26       | nd         | nd         | 0            | nd         | nd         | 0            |
| Past-D7   | *Porites astreoides*        | 36       | nd         | nd         | 0            | nd         | nd         | 0            |
| Past-F4   | *Porites astreoides*        | 16       | nd         | nd         | 0            | nd         | nd         | 0            |


## DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2022-10-05-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2022-10-05-gel.JPG?raw=true)


## Next steps:

I will talk to Hollie and Kristina about next steps for the PAST samples. Currently, I am thinking of bead beating the fragments in the tube in a bead tube with fresh DNA/RNA sheild following [Kevin Wong's protocol](https://kevinhwong1.github.io/KevinHWong_Notebook/20201027-DNA-RNA-Extractions-Porites-July-Bleaching-Experiment/) here:

Sample Preparation and Digestion
> > 1. Add 0.25 mL of glass beads (0.5mm) and add 500 μl of RNA/DNA shield into each empty centrifuge tube.
> > 2. Take samples out from -80 °C on dry ice.
> > 3. Using sterile clippers, add 0.25mm of tissue into the centrifuge tube with beads and RNA/DNA shield.
> > 4. Vortex at max speed for 2 minutes.
> > 5. Remove 400 μl of the supernatant and transfer to a new centrifuge tube.
> > 6. Centrifuge at 9000 rcf for 3 minutes.
> > 7. Transfer 300 μl supernatant to a new centrifuge tube and discard the pellet.
> > 8. Add 30 μl of Proteinase K digestion buffer (10:1 ratio of sample:digestion buffer), and 15 μl of Proteinase K (2:1 ratio of digestion buffer:Proteinase K) to each sample.
> > 9. Vortex and spin down.
> > 10. Add 345 μl of lysis buffer.
> > 11. Continue with DNA and RNA extraction protocol