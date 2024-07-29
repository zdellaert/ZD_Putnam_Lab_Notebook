---
layout: post
title: Testing of Charm Biotech DNA Extraction on LCM-d P. compressa and P. acuta
date: '2024-07-24'
categories: Processing
tags: [DNA, PAXgene, Fixative, Pocillopora, Porites, LCM]
---

## Testing Charm DNA Kit on 7/18 LCM Samples, Second Try

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Charm-LCM-DNA-Kit-Protocol/)

## 7/24/24 - Extracting DNA from LCM-captured cells (LCM date 7/18/24)

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM) Sample Total DNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_DNA_Kit.pdf). I had good success with this protocol for LCM-d P. acuta on [6/26/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-DNA-Extractions-Charm/), and less great success trying it for the first time on *Porites* LCM samples on [7/19/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240718-DNA-Extractions-Charm/). I wanted to try again to get DNA out of *Porites* with this method, and concurrently wanted to extract another *Pocillopora* sample to confirm my 6/26/24 success was reproducible. But, made a few adjustments from 7/19/24, notably:
   - no shaking on the thermomixer, just 52 ºC overnight
   - exclusively used pipetting method for supernatant removal, no dumping
   - Spun 8 minutes instead of 5 in initial binding spin to try to bind as much DNA to the tube as possible

### Sectioning performed on 7/17/24 and LCM on 7/18/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-4/) 

#### Protocol notes:

- Samples: #14 and #23, both collected in buffer DD1.
  - 14: Porites, big chunk
  - 23: Pocillopora, also big chunk
  
- Cell collection procedure:
  1. During LCM, were collected in 40 uL of buffer DD1 in tube cap during LCM
  2. Vortexed and spun down briefly in LCM room and let cells lyse for ~5 minutes at room temperature (seeing homogenous leeching of cresyl violet stain into solution) before transferring to tube rack on dry ice.
  3. Lysed cells tranferred on dry ice to -80ºC until extraction.

Extraction steps taken:
1. Added 50 uL of digestion buffer (DD1) and 10 uL of Proteinase K to each PCR tube containing the dissected cells in 40 uL digestion buffer. 
2. Pipetted up and down to mix and then transferred whole volume to a clean 1.5 mL tube, making sure to transfer all visible cells/debris (a wide bore tip might be good here)
3. Vortex tube and spin down and visually confirm that cells are in the bottom of the tube. Cresyl violet staining helps a lot here.
   1. Vortexing already visually breaks down the cells a lot or at least releases some of the dye into solution
4. Transferred to thermomixer for incubation at 52 ºC (**no shaking**) overnight
5. In morning, centrifuged tube with hinges pointed outward for 3 minutes at 9,000 rcf to try to pellet any debris that are left
6. Transferred contents/supernatant (100 uL) to the Charm binding tube and followed all following [instructions as written](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_DNA_Kit.pdf) from step "Binding DNA Products" onward.
   1. Saw a large pellet in both tubes, which was very promising for DNA content!
   2. For each of the wash steps, I very carefully pipetted out the wash buffer with a 200 uL pipette, watching the pellet to make sure I did not touch it or the sides of the tube
7. Eluted the DNA in 20 uL of elution buffer **warmed to 60ºC**. Pipetted up and down until pellet was visibly resuspended and then briefly vortexed and spun down. Pipetted up and down ~5-10 times, then spun down again to remove bubbles, and repeated the pipetting up and down ~5-10 times followed by a spin once more.
  
#### Qubit Results

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
  - I have been doing 2 uL of DNA product with 198 uL of DNA buffer, just to reduce any possible pipetting error. This is corrected for in the Qubit readings.
- All samples read twice, standard only read once

 DNA Standards: 66.88 (S1) & 22835.04 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG | ng in tube (Qubit * 20 uL) | 
|-----------|------------|------------|--------------|--------------|
| LCM sample #14  |  1.67 |  1.68   |  1.68 ng/uL | 33.6 ng     |
| LCM sample #23  |  4.40 |  4.43  |  4.42 ng/uL | 88.4 ng      |

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 2 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 7 uL of extracted DNA into each well
- Ran at 65 V for 60 minutes

![2024-07-24-gel-Charm.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-24-gel-Charm.JPG?raw=true)

Great bands, especially for the *Pocillopora* sample, which is consistent with previous results. For some reason, at least with both this kit and the Zymo kit, I am able to get good DNA from *Pocillopora* and it is harder to get that amount from *Porites*, even if the tissue input is greater. 

But! improvement on the DNA from 7/19/24, and this is definitely a viable option for both species.