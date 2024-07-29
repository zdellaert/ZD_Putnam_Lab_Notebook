---
layout: post
title: Testing Zymo Quick DNA/RNA Microprep Kit on LCM-d P. acuta and P. compressa
date: '2024-07-19'
categories: Processing
tags: [RNA, DNA, Pocillopora, Porites, LCM]
---

## Testing Zymo Quick-DNA/RNA Microprep Kit on 7/18 LCM Samples

### [Protocol Link](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf)

## 7/19/24 - Extracting RNA from LCM-captured cells (LCM date 7/18/24)

Used Quick-DNA/RNA™ Microprep [Kit](https://www.zymoresearch.com/products/quick-dna-rna-microprep-plus-kit), [protocol](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf).

### Sectioning performed on 7/17/24 and LCM on 7/18/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-4/) 

#### Protocol notes:

- Cell collection procedure:
  1. During LCM, were collected in 40 uL of buffer (see below) in tube cap during LCM
  2. Vortexed and spun down briefly in LCM room and let cells lyse for ~5 minutes at room temperature (seeing homogenous leeching of cresyl violet stain into solution) before transferring to tube rack on dry ice.
  3. Lysed cells tranferred on dry ice to -80ºC until extraction.
- Cells were collected directly into either:
  1. DNA/RNA Lysis buffer from kit
  2. Zymo Proteinase K Digestion mix (FFPE Section of protocol):
     1. 95 uL DNAse/RNAse free water
     2. 95 uL Zymo 2X Digestion Buffer
     3. 10 uL Proteinase K
- Extraction prep:
  - Thaw tube on ice and then proceed
  - For samples collected in ProK Mix:
    - Added another 60 uL of ProK mix, moved to 1.5 mL tube, making sure to transfer all cellular debris, and incubated at 52 ºC on the thermomixer, shaking 1400 rpm, for either overnight (OVERNIGHT SAMPLES) or 1 hour (1 HOUR SAMPLES)
    - After incubation, spin at 9,000 rcf for 3 mins to pellet any debris, then move supernatant to new 1.5 mL tube. Add equal parts lysis buffer and mix well, then move whole volume into IC-XM column.
  - For samples collected in lysis buffer:
    - Added another 160 uL of lysis buffer (final vol = 200 uL) and vortex 5 seconds to homogenize and further lyse cells
    - Went straight into IC-XM column (1st step in Zymo protocol)
  - Rest of protocol followed almost exactly [as written]((https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf)). 
    - Spin IC-XM column, move to a new collection tube and move flow-though to 1.5 mL tube, combine with equal parts ethanol and mix well
    - Move into RNA (IC) column and spin down, discard flow through
    - Wash with 400 uL wash buffer, then do DNAse treatment (40 uL)
    - Then 400 uL prep buffer and spin, 700 uL wash buffer and spin, and 400 uL wash buffer and spin.
    - After last wash buffer I did modify the protocol slightly and moved the column to a new collection tube and spun dry for 2 minutes to try to remove any residual ethanol. Could try playing with this step since it is not in the protocol. But, they provide extra collection tubes so it seems appropriate.
    - Eluted RNA in 15 uL nuclease free water, and DNA in 20 uL nuclease free TRIS, warmed to 60ºC (based on our other Putnam Lab [Zymo Extraction Protocols](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/))

#### RNA Quality Check: Tapestation

Have not been runnning RNA Qubit's because I never detect anything from these super low concentrations.

![2024-07-19.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-19.JPG?raw=true)

Tapestation concentrations and [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination):

| sample_id | concentration | RIN | DV200 | 
|-----------|------------|------------|-------|
| #1, Porites, Lysis Buffer   |  344 pg/uL (0.344 ng/uL) | - | 54.38% | 
| #5, Porites, ProK 52 ºC 1 hour  |   311 pg/uL (0.311 ng/uL)  | - |  70.99% | 
| #6, Porites, ProK 52 ºC overnight  |   603 pg/uL (0.603 ng/uL)  | 2.5 | 64.89% | 
| #17, Pocillopora, Lysis Buffer   |  1350 pg/uL (1.350 ng/uL) | 1.0 | 36.68% | 
| #20, Pocillopora, ProK 52 ºC 1 hour  |   811 pg/uL (0.811 ng/uL)  | 1.2 | 47.06% | 
| #21, Pocillopora, ProK 52 ºC overnight  |   1220 pg/uL (1.220 ng/uL)  | 1.0 | 46.23% | 

Positive control: Pdam Heron Island project (RNA I extracted in 11/2022) sample RF14B. Diluted, used 1 uL RNA and 1 uL nucelase-free water for the tapestation.

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-19.pdf)

#### DNA Quantity Check: Qubit

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 60.16 (S1) & 21073.89 (S2)

| colony_id            | DNA_QBIT_1 | DNA_QBIT_2 |    DNA_QBIT_AVG |
|----------------------|------------|------------|-----------------|
| #1, Porites, Lysis Buffer         | nd    |  nd      |   nd      |
| #5, Porites, ProK 52 ºC 1 hour    | 0.299 |  0.296   |   0.298   |
| #6, Porites, ProK 52 ºC overnight | 0.319 | 0.328    |   0.324   |
| #17, Pocillopora, Lysis Buffer    | 0.245 |  0.247   |   0.246   |
| #20, Pocillopora, ProK 52 ºC 1 hour  | 0.991 | 0.981 |   0.986   |
| #21, Pocillopora, ProK 52 ºC overnight | 1.32 | 1.31 |   1.32    |

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 1.5 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 5 uL of extracted DNA into each well
  - **this was too little. should've done more.**
- Ran at 65 V for 60 minutes

![2024-07-19-gel-Zymo.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-19-gel-Zymo.JPG?raw=true)

Mayyybe bands for the 2 Pocillopora ProK digestions (# 20,21) ? Positve control was the DNA from the Pdam Heron Island project (extracted in 11/2022), sample RF14B. Diluted, likely too much....

##### Reran these samples on a gel on 7/24/24:

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 2 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 7 uL of extracted DNA into each well
- Ran at 65 V for 60 minutes

![2024-07-24-gel-Zymo-719.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-24-gel-Zymo-719.JPG?raw=true)

Same result. 20 and 21 have bands but streaky. No bands for any other samples. 

### Thoughts:

1. RNA:
   1. This is some of the best RNA I've gotten from LCM! Even though the concentration was too low to calculate a RIN, the 1 hour ProK digestion for Porites (#5) looks super good with very clear 18S and 28S bands.
   2. The overnight digestion caused a lot of RNA degredation, so I think we can try to move away from this. However, it may be needed for DNA, so I will reach out to zymo for advice.
   3. The Pocillopora RNA (#s 17, 20, 21) did not work as well. This could be because the input was so low, or it could be the sample prep in general. I had issues with the Pocillopora sectioning (detailed [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-4/)), and these issues contributed to a lot of tissue loss and other issues. The Pocillopora RNA from my [last LCM test](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-RNA-Extractions-Zymo/) looked better than today. For that extraction, the cells were just collected in lysis buffer, with no ProK digestion. However, the cells collected in lysis buffer for this extraction looked the most degraded. There is a chance we may need to use different collection buffers for different species. Will continue to try some different protocols.
2. DNA:
   1. Not a lot. Pocillopora worked better than Porites, but this is much less visible on the gel than from the Charm kit. I did load less on the gel (5uL vs 10uL), but still. Need to make this better.
   2. I don't understand why the POR RNA works so well and the DNA doesn't and vice versa (ish) for POC! Need to think through how different tissue inputs and digestion timepoints would impact DNA vs. RNA accessibility/degredation. Want to reach out to Zymo, too.