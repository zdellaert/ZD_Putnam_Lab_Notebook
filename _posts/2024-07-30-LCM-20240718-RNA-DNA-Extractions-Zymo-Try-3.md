---
layout: post
title: Continued Testing of Zymo Quick DNA/RNA Microprep Kit on LCM-d P. acuta and P. compressa
date: '2024-07-30'
categories: Processing
tags: [RNA, DNA, Pocillopora, Porites, LCM]
---

## Continued Testing of Zymo Quick-DNA/RNA Microprep Kit on 7/18 LCM Samples

### [Protocol Link](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf)

## 7/30/24 - Extracting RNA from LCM-captured cells (LCM date 7/18/24)

Used Quick-DNA/RNA™ Microprep [Kit](https://www.zymoresearch.com/products/quick-dna-rna-microprep-plus-kit), [protocol](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf).

### Sectioning performed on 7/17/24 and LCM on 7/18/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-4/) 

### Thoughts from [7/24/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240718-RNA-DNA-Extractions-Zymo-Try-2/): 

ProK-digested Porites RNA continues to look great! DNA not so much. Maybe a smudge for #7, the 1 hour ProK digestion for *Porites*.

For the RNA, I am beginning to wonder how much of it is actually changing by the digestions, and how much of it is just dependent on how much tissue is going in. The Porites tubes likely consistently have more tissue than the Pocillopora tubes, which may be the reason in-tact RNA is able to persist in those samples. For the lowest-input Porites tube I've tried so far, # 11, I had low concentration and not great tapestation. Yes, it was only digested for 30 minutes, which could be the reason, but I think the tissue input will play a big role.

### Ways forward to improve POC RNA quality

- Do the ProK digestion but at lower temp and/or less time
  - **15 minute ProK digestion** at 45°C using a shaker–incubator at 1400 rpm
    - [paxgene simultaneous DNA/RNA protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Simultaneous_DNA_RNA.pdf)
  - 15 minute ProK digestion, room temp?
  - Elute twice, 9 uL and 9 uL

### Ways forward to improve POR DNA yield

- on column proteinase K digestion?! 
  - The [paxgene simultaneous DNA/RNA protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Simultaneous_DNA_RNA.pdf) does the following:
    - **15 minute ProK digestion** at 45°C using a shaker–incubator at 1400 rpm
    - Then, this mixture gets mixed with lysis buffer and goes into the DNA column
    - Then, flow through is saved for RNA extraction, and DNA column is set aside for time being (at 4 ºC)
    - RNA extraction pretty standard 
    - DNA extraction has an **extra on-column ProK digestion step**!!
      - Wash step TD3, 350 uL (*This wash buffer (TD3) is not just a normal wash buffer, has guanidine salt*)
        - could this potentially be like the prep buffer in the zymo kit?
      - Add 25 μl proteinase K to 50 μl Buffer TD3 in a 1.5 ml microcentrifuge tube. Mix by gently flicking the tube, and centrifuge briefly to collect residual liquid from the sides of the tube.
      - Pipet the proteinase K incubation mix (75 μl) directly onto the PAXgene DNA spin column, and incubate for 30 min at ambient temperature (20–30°C)
      - Wash step TD3, 350 uL
      - Wash step TD4, 500 uL
      - Elution

### Steps taken today

Samples: 12 (POR, low input, ProK buffer) & 22 (POC, low input, ProK buffer)

- added 60 uL more buffer after thawing on ice, then incubated at 45 ºC in incubator genie (in original PCR tube) on speed 9 for 15 minutes
- then transferred to 1.5 mL tube and spun down (9000 rcf, 3 mins) to pellet debris and moved supernatant to new tube
- added 100 uL lysis buffer to the 100 uL of supernatant and mixed well via vortex. Transferred all volume to IC-XM (DNA column) and proceeded as usual.
- put DNA columns in fridge while proceeding with RNA extraction as normal, with an elution of 2X 9 uL instead of once 15 uL
- DNA extraction changes (see above notes):
  - Wash column with 400 uL wash buffer like before DNAse treatment
  - Make a mixture of 30 µl of PK digestion buffer and 15 µl Proteinase K (1:2 ratio of Proteinase K:PK Digestion Buffer) and pipette whole 45 uL onto DNA column
  - Incubate for 30 min at room temp
  - Normal wash steps, and eluted 2X 9 uL instead of once 15 uL
    - eluted in Tris warmed to 60 ºC

Otherwise details of protocol were same as [7/24/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240718-RNA-DNA-Extractions-Zymo-Try-2/)

#### RNA Quality Check: Tapestation

Have not been runnning RNA Qubit's because I never detect anything from these super low concentrations.

![2024-07-30.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-30.JPG?raw=true)

Tapestation concentrations and [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination):

| sample_id | concentration | RIN | DV200 | 
|-----------|------------|------------|-------|
| #12, Porites,  ProK 45 ºC 15 min   |  352 pg/uL (0.352 ng/uL) | - | 60.60% |
| #22, Pocillopora, ProK 45 ºC 15 min  |   1480 pg/uL (1.480 ng/uL)  | 2.1 | 50.57% |

No postitive control, trying to save on reagents.

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-30.pdf)

#### DNA Quantity Check: Qubit

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 66.72 (S1) & 24527.74 (S2)

| colony_id                      | DNA_QBIT_1 | DNA_QBIT_2 |   DNA_QBIT_3      | DNA_QBIT_AVG |
|--------------------------------|------------|------------|-------------------|--------------|
| ##12, Porites,  ProK 45 ºC 15 min   |  0.088   |  0.084  |  0.088       |    0.087     |
| #22, Pocillopora, ProK 45 ºC 15 min | 2.56     |  2.55   |  2.54        |      2.55    |

Well that's pretty good increase for DNA from the Zymo kit! At least for POC...

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 2 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 7 uL of extracted DNA into each well
- Ran at 65 V for 60 minutes

![2024-07-30-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-30-gel.JPG?raw=true)

### Thoughts

- Okay, so unfortunately decreasing the digestion time and temperature did not magically make the POC RNA not be degraded. That's the last sample I have collected in ProK digestion buffer, but can continue to play around with the lysis buffer samples. But there is something weird going on that I don't fully understand. 

- Once again, all of this could be dependent mostly on tissue input and the more tissue that goes in the more intact RNA that comes out.

- emailed Zymo support with basically the following questions
  - Why would we get degraded RNA from the DNA/RNA kit if we were getting less degraded RNA from the [RNA only kit](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-RNA-Extractions-Zymo/)?
  - Why would we be able to get great RNA from Porites with the DNA/RNA kit but not DNA?
  - Vice versa, why would we be able to get great DNA from Pocillopora but not RNA?
    - Didn't use the species names, but just brought up this question/idea
  - Asked if they have recommendations for digestion times and/or on-column proteinase K digestion.