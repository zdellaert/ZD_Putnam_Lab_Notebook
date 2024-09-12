---
layout: post
title: Further Testing of Zymo Quick DNA/RNA Microprep Kit on LCM-d P. acuta and P. compressa
date: '2024-07-24'
categories: Processing
tags: [RNA, DNA, Pocillopora, Porites, LCM]
---

## Further Testing of Zymo Quick-DNA/RNA Microprep Kit on 7/18 LCM Samples

### [Protocol Link](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf)

## 7/24/24 - Extracting RNA from LCM-captured cells (LCM date 7/18/24)

Used Quick-DNA/RNA™ Microprep [Kit](https://www.zymoresearch.com/products/quick-dna-rna-microprep-plus-kit), [protocol](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf).

### Sectioning performed on 7/17/24 and LCM on 7/18/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-4/) 

I had some great success in [extracting high quality](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240718-RNA-DNA-Extractions-Zymo/) (even if very low concentration) from the *Porites* LCM samples from 7/18/24, and found most success with cells collected in the ProK digestion buffer with a 1-hour digestion at 52 ºC prior to extraction. I wanted to repeat this extraction with additional samples, with a few modifications:
- Try a 30 minute incubation in addition to a 1 hour incubation, to see if this improves or decreases anything
- Do the incubation in the incubator genie instead of the thermomixer, as I have heard from other labmates that they have had better success for RNA quality with this method, maybe the temperature is more consistent
- I also wanted to retry an extraction from cells collected in lysis buffer instead of ProK buffer, just to see if there would be any success with them. Instead of adding 160 uL of lysis buffer to those samples for a lysis volume of 200 uL, I added 60 uL for a final lysis volume of 100 uL. This is what I originally did for the [mediocre-quality RNA extraction of POC LCM samples with the Quick RNA Microkit](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-RNA-Extractions-Zymo/).
- Since I only have one sample of POC left collected in ProK digestion buffer, I did not test a POC ProK extraction today. Will try to learn more from POR today and then test further with POC.
- **Based on some super low-input RNA column-based kits I have seen online, I tried some modifications to the spins to see if this would increase binding at all**
  - When binding DNA/RNA to the IC-XM or IC column for the first time, sping 2 mins at 100 rcf before doing the 1 minute spin at 15,000 rcf
  - Also do the same for the elution of the DNA and RNA. The goal is to fully saturate the column without adding too much time for degredation.

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
    - Added another 60 uL of ProK mix, moved to 1.5 mL tube, making sure to transfer all cellular debris, and incubated at 52 ºC on the incubator genie with no agitation, for either 30 mins (sample #11) or 1 hour (sample # 7)
    - After incubation, spin at 9,000 rcf for 3 mins to pellet any debris, then move supernatant to new 1.5 mL tube. Add equal parts lysis buffer and mix well, then move whole volume into IC-XM column.
  - For samples collected in lysis buffer (samples #2 (POR) and #18 (POC)):
    - Added another 60 uL of lysis buffer (final vol = 100 uL) and vortex 5 seconds to homogenize and further lyse cells
    - Went straight into IC-XM column (1st step in Zymo protocol)
  - Rest of protocol followed almost exactly [as written](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf). 
    - Spin IC-XM column, move to a new collection tube and move flow-though to 1.5 mL tube, combine with equal parts ethanol and mix well
    - Move into RNA (IC) column and spin down, discard flow through
    - Wash with 400 uL wash buffer, then do DNAse treatment (40 uL)
    - Then 400 uL prep buffer and spin, 700 uL wash buffer and spin, and 400 uL wash buffer and spin.
    - After last wash buffer I did modify the protocol slightly and moved the column to a new collection tube and spun dry for 2 minutes to try to remove any residual ethanol. Could try playing with this step since it is not in the protocol. But, they provide extra collection tubes so it seems appropriate.
    - Eluted RNA in 15 uL nuclease free water, and DNA in 20 uL nuclease free TRIS, warmed to 60ºC (based on our other Putnam Lab [Zymo Extraction Protocols](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/))

#### RNA Quality Check: Tapestation

Have not been runnning RNA Qubit's because I never detect anything from these super low concentrations.

![2024-07-24.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-24.JPG?raw=true)

Tapestation concentrations and [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination):

| sample_id | concentration | RIN | DV200 | 
|-----------|------------|------------|-------|
| #2, Porites, Lysis Buffer   |  270 pg/uL (0.270 ng/uL) | - | 64.33% |
| #7, Porites, ProK 52 ºC 1 hour  |   280 pg/uL (0.280 ng/uL)  | - | 66.86% |
| #11, Porites, ProK 52 ºC 30 mins (*low tissue input!!*)  |   304 pg/uL (0.304 ng/uL)  | - | 60.03% |
| #18, Pocillopora, Lysis Buffer   |  484 pg/uL (0.484 ng/uL) | 2.7 | 48.13% |

Positive control was my successful [RNA extraction from 7/19/24 (POR sample #5)](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240718-RNA-DNA-Extractions-Zymo/), but I did not thaw it on ice which was a mistake....

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-24.pdf)

#### DNA Quantity Check: Qubit

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 66.88 (S1) & 22835.04 (S2)

| colony_id                      | DNA_QBIT_1 | DNA_QBIT_2 |   DNA_QBIT_3      | DNA_QBIT_AVG |
|--------------------------------|------------|------------|-------------------|--------------|
| #2, Porites, Lysis Buffer      |    nd      |    nd      |       nd          |        nd    |
| #7, Porites, ProK 52 ºC 1 hour |    0.306   |    0.308   |       0.306       |      0.307   |
| #11, Porites, ProK 52 ºC 30 mins (*low tissue input!!*)  |  0.081    | 0.080 |    0.084    |   0.082   |
| #18, Pocillopora, Lysis Buffer |    0.134   |    0.139   |       0.141       |    0.138    |

#### DNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

- Made a 1% gel (50 uL TAE + 0.5g agarose) with 2 uL Gel Green (bumping up from normal amount to maximize visualization)
- Loaded 7 uL of extracted DNA into each well
- Ran at 65 V for 60 minutes

![2024-07-24-gel-Zymo.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2024-07-24-gel-Zymo.JPG?raw=true)

Annoying gel artifacts, shadow bands from the imager. But #7 looks to be the only one with a very faint, streaky band.

### Thoughts: 

ProK-digested Porites RNA continues to look great! DNA not so much. Maybe a smudge for #7, the 1 hour ProK digestion for *Porites*.

For the RNA, I am beginning to wonder how much of it is actually changing by the digestions, and how much of it is just dependent on how much tissue is going in. The Porites tubes likely consistently have more tissue than the Pocillopora tubes, which may be the reason in-tact RNA is able to persist in those samples. For the lowest-input Porites tube I've tried so far, # 11, I had low concentration and not great tapestation. Yes, it was only digested for 30 minutes, which could be the reason, but I think the tissue input will play a big role.