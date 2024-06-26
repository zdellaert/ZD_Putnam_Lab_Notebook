---
layout: post
title: Suucessful? Testing of Charm Biotech DNA Extraction on LCM-d P. acuta 
date: '2024-06-26'
categories: Processing
tags: [DNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Charm DNA Kit on LCM Samples

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Charm-LCM-DNA-Kit-Protocol/)

## 6/26/24 - Extracting DNA from LCM-captured cells (LCM date 6/13/24)

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM) Sample Total DNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_DNA_Kit.pdf)

### Sectioning performed on 6/12/24 and LCM on 6/13/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-2/) 

#### Protocol notes:

- On [6/17/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-DNA-Extractions-Charm/), I followed the Charm FFPE and Frozen tissue protocols almost exaclty, with 2 hour incubation at 56 ºC.
    - This did not work!
- As a last(ish) resort for this kit, I wanted to see what would happen if I significantly increased digestion time. The protocol states you can do an overnight digestion at 52 ºC, so I tried this today.
- Tube 9 was captured in 40 uL DD2 buffer (FFPE protocol)
- Tube 13 was captured in 40 uL DD1 buffer (Frozen Tissue protocol)

Steps taken:

1. Added 50 uL of digestion buffer (DD2 to tube 9 and DD1 to tube 13) and 10 uL of Proteinase K to each PCR tube containing the dissected cells in 40 uL digestion buffer. 
2. Pipetted up and down to mix and then transferred whole volume to a clean 1.5 mL tube, making sure to transfer all visible cells/debris (a wide bore tip might be good here)
3. Vortex tube and spin down and visually confirm that cells are in the bottom of the tube. Cresyl violet staining helps a lot here.
   1. Vortexing already visually breaks down the cells a lot or at least releases some of the dye into solution
4. Transferred to thermomixer for incubation at 52 ºC at 1400 rpm for 16.5 hours (overnight, 15:30 - 8:00)
5. In morning, centrifuged tube with hinges pointed outward for 3 minutes at 9,000 rcf to try to pellet any debris that are left
6. Transferred contents/supernatant (100 uL) to the Charm binding tube and followed all following [instructions as written](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_DNA_Kit.pdf) from step "Binding DNA Products" onward.
   1. Saw a large pellet in both tubes, which was very promising for DNA content!
   2. For each of the wash steps, I very carefully pipetted out the wash buffer with a 200 uL pipette, watching the pellet to make sure I did not touch it or the sides of the tube
7. Eluted the DNA in 15 uL of elution buffer **warmed to 56ºC**. Pipetted up and down until pellet was visibly resuspended and then briefly vortexed and spun down. Pipetted up and down ~5-10 times, then spun down again to remove bubbles, and repeated the pipetting up and down ~5-10 times followed by a spin once more.
  
#### Qubit Results

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
  - I have been doing 2 uL of DNA product with 198 uL of DNA buffer, just to reduce any possible pipetting error. This is corrected for in the Qubit readings.
- All samples read twice, standard only read once

 DNA Standards: 59.35 (S1) & 22341.37 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG | ng in tube (Qubit * 15 uL) | 
|-----------|------------|------------|--------------|--------------|
| LCM sample #10  |  1.81 |  1.81   |  1.81 ng/uL | 27.15 ng |
| LCM sample #14  |  4.29 |  4.29   |  4.29 ng/uL | 64.35 ng |

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 1.5 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 9.5 uL of extracted DNA into each well (3&5)
- Ran at 65 V for 40 minutes

![2024-06-26-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-06-26-gel.JPG?raw=true)

![2024-06-26-gel-zoom.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-06-26-gel-zoom.JPG?raw=true)

Yay!! This is so great! woohoo!