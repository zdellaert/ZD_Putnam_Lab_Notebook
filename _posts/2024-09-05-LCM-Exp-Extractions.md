---
layout: post
title: 2024-09-05 LCM Experiment Extractions
date: '2024-09-05'
categories: Processing
tags: [PAXgene, Fixative, Pocillopora, LCM, LCM-Pilot, RNA, DNA]
---

## Extracting RNA and DNA from LCM-d Pocillopora for LCM Experiment

### Extraction plan:

**15 minute ROOM TEMP ProK digestion only** - can extend to 30 mins; can always try on column proK for dna

- Cell collection procedure:
  1. During LCM, were collected in 40 uL of buffer (see below) in tube cap during LCM
  2. Vortexed and spun down briefly in LCM room before transferring to tube rack on dry ice.
  3. Lysed cells tranferred on dry ice to -80ºC until extraction.
- Cells were collected directly in Zymo Proteinase K Digestion mix (FFPE Section of protocol):
     1. 95 uL DNAse/RNAse free water
     2. 95 uL Zymo 2X Digestion Buffer
     3. 10 uL Proteinase K
- Extraction prep:
  - Thaw tube on ice and then proceed
  - For samples collected in ProK Mix:
    - Added another 60 uL of ProK mix, moved to 1.5 mL tube, making sure to transfer all cellular debris
      - **Incubate at room temp for 15 mins**
      - Only did about 7 minutes on 9/8/24 since the cells sat for a long time at room temp during LCM
    - After incubation, spin at 9,000 rcf for 3 mins to pellet any debris, then move supernatant to new 1.5 mL tube. Add equal parts lysis buffer and mix well, then move whole volume into IC-XM column.
      - **Can double lysis buffer**
      - Used 150 uL on 9/8/24
  - Rest of protocol followed almost exactly [as written](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf). 
    - Spin IC-XM column, move to a new collection tube and move flow-though to 1.5 mL tube, combine with equal parts ethanol and mix well
    - Move into RNA (IC) column and spin down, discard flow through
    - Wash with 400 uL wash buffer, then do DNAse treatment (40 uL)
    - Then 400 uL prep buffer and spin, 700 uL wash buffer and spin, and 400 uL wash buffer and spin.
    - After last wash buffer I did modify the protocol slightly and moved the column to a new collection tube and spun dry for 2 minutes to try to remove any residual ethanol. Could try playing with this step since it is not in the protocol. But, they provide extra collection tubes so it seems appropriate.
    - Eluted RNA in 18 uL (2 X 9uL) nuclease free water, and DNA in 20 uL (2 X 10 uL) nuclease free TRIS, warmed to 60ºC (based on our other Putnam Lab [Zymo Extraction Protocols](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/))
      

**Zoe write up exact extraction method from notebook**


#### RNA Quality Check: Tapestation

Have not been runnning RNA Qubit's because I never detect anything from these super low concentrations.

![2024-09-08-rna](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-08-rna.png?raw=true)

Tapestation concentrations and [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination):

| sample_id      | concentration | RIN | DV200 | 
|----------------|------------|------------|-------|
| #13 (Frag C)   |  381 pg/uL (0.381 ng/uL)  | - | 53.74% |
| #14 (Frag C)   |  367 pg/uL (0.367 ng/uL)  | - | 59.89% |

Positive control is from 6/13/24 #7, the POC that worked well for the NEB library prep kit.

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-08-hsRNA.pdf)

#### DNA Quantity Check: Qubit

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 69.08 (S1) & 24297.05 (S2)

| colony_id                      | DNA_QBIT_1 | DNA_QBIT_2 |   DNA_QBIT_3      | DNA_QBIT_AVG |
|--------------------------------|------------|------------|-------------------|--------------|
| #13 (Frag C)   |  nd   |  nd   |  nd   |     nd      |
| #14 (Frag C) |   nd   |  nd    |    nd       |    nd    |


Hmm.


#### DNA Quality Check: Tapestation

Nothing detected on Qubit. Likely nothing will be on a gel, so trying gDNA tapestation.

![2024-09-08-gdna](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-08-gdna.png?raw=true)

Tapestation concentrations:

| sample_id      | concentration | DIN | 
|----------------|------------|------------|
| #13 (Frag C)   |  7.16 ng/uL  | - | 
| #14 (Frag C)   |  6.06 ng/uL  | - | 

Positive control is from 7/30/24 #22, the POC that worked well for the Zymo Pico Kit.

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-08-gdna.pdf)

Possible DNA on column pro-K:
- DNA extraction changes (see above notes):
  - Wash column with 400 uL wash buffer like before DNAse treatment
  - Make a mixture of 30 µl of PK digestion buffer and 15 µl Proteinase K (1:2 ratio of Proteinase K:PK Digestion Buffer) and pipette whole 45 uL onto DNA column
  - Incubate for 30 min at room temp
  - Normal wash steps, and eluted 2X 9 uL instead of once 15 uL
    - eluted in Tris warmed to 60 ºC
