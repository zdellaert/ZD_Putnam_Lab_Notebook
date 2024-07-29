---
layout: post
title: Testing of Charm Biotech DNA Extraction on LCM-d P. compressa 
date: '2024-07-19'
categories: Processing
tags: [DNA, Porites, LCM]
---

## Testing Charm DNA Kit on 7/18 LCM Samples

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Charm-LCM-DNA-Kit-Protocol/)

## 7/19/24 - Extracting DNA from LCM-captured cells (LCM date 7/18/24)

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM) Sample Total DNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_DNA_Kit.pdf). I had good success with this protocol for LCM-d P. acuta on [6/26/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-DNA-Extractions-Charm/).

### Sectioning performed on 7/17/24 and LCM on 7/18/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-4/) 

#### Protocol notes:

- Performed overnight digestion at 52 ºC in thermomixer at 1400 rpm as done successfully for *P. acuta* on [6/26/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-DNA-Extractions-Charm/).
- Samples: #13 and #15, both Porites collected in buffer DD1.
  - 13: big chunk of tissue
  - 15: smaller amount of tissue
  
- Cell collection procedure:
  1. During LCM, were collected in 40 uL of buffer DD1 in tube cap during LCM
  2. Vortexed and spun down briefly in LCM room and let cells lyse for ~5 minutes at room temperature (seeing homogenous leeching of cresyl violet stain into solution) before transferring to tube rack on dry ice.
  3. Lysed cells tranferred on dry ice to -80ºC until extraction.

Extraction steps taken:
1. Added 50 uL of digestion buffer (DD1) and 10 uL of Proteinase K to each PCR tube containing the dissected cells in 40 uL digestion buffer. 
2. Pipetted up and down to mix and then transferred whole volume to a clean 1.5 mL tube, making sure to transfer all visible cells/debris (a wide bore tip might be good here)
3. Vortex tube and spin down and visually confirm that cells are in the bottom of the tube. Cresyl violet staining helps a lot here.
   1. Vortexing already visually breaks down the cells a lot or at least releases some of the dye into solution
4. Transferred to thermomixer for incubation at 52 ºC at 1400 rpm overnight
5. In morning, centrifuged tube with hinges pointed outward for 3 minutes at 9,000 rcf to try to pellet any debris that are left
6. Transferred contents/supernatant (100 uL) to the Charm binding tube and followed all following [instructions as written](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_DNA_Kit.pdf) from step "Binding DNA Products" onward.
   1. Saw a large pellet in both tubes, which was very promising for DNA content!
   2. Used the dumping method of supernatant removal instead of [pipetting out](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-DNA-Extractions-Charm/) (possibly a mistake? See below.)
7. Eluted the DNA in 20 uL of elution buffer **warmed to 60ºC** ([last time](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-DNA-Extractions-Charm/) I warmed it to 56 ºC...). Pipetted up and down until pellet was visibly resuspended and then briefly vortexed and spun down. Pipetted up and down ~5-10 times, then spun down again to remove bubbles, and repeated the pipetting up and down ~5-10 times followed by a spin once more.
  
#### Qubit Results

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
  - I have been doing 2 uL of DNA product with 198 uL of DNA buffer, just to reduce any possible pipetting error. This is corrected for in the Qubit readings.
- All samples read twice, standard only read once

 DNA Standards: 60.16 (S1) & 21073.89 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG | ng in tube (Qubit * 20 uL) | 
|-----------|------------|------------|--------------|--------------|
| LCM sample #13  |  0.612 |  0.620   |  0.616 ng/uL | 12.32 ng     |
| LCM sample #15  |  0.252 |  0.266   |  0.259 ng/uL | 5.18 ng      |

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 1.5 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 5 uL of extracted DNA into each well
  - **this was too little. should've done more.**
- Ran at 65 V for 60 minutes

![2024-07-19-gel-Charm.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-19-gel-Charm.JPG?raw=true)

**Neither samples showed a band on the gel**. Positve control was the DNA from the Pdam Heron Island project (extracted in 11/2022), sample RF14B. Diluted, likely too much....

##### Reran these samples on a gel on 7/24/24:

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 2 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 7 uL of extracted DNA into each well
- Ran at 65 V for 60 minutes

![2024-07-24-gel-Charm-719.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-24-gel-Charm-719.JPG?raw=true)

Okay! They are actually bands there which is cool! This protocol seems to have more success than the Zymo one for extracting DNA. We will have to see if we can learn anything from this to make the Zymo one work better, or if we will need a separate DNA and RNA extraction methods and collection buffer instead of being able to get both from the same tube.

It's really encouraging that the DNA I am getting doesn't look degraded in the slightest. Super sharp bands.