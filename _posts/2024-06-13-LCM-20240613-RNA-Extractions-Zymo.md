---
layout: post
title: Testing Zymo Quick RNA Microprep Kit on Cryosectioned and LCM-d *P. acuta* 
date: '2024-06-13'
categories: Processing
tags: [RNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Zymo Quick-RNA Microprep Kit on LCM Samples

### [Protocol Link](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf)

## 6/13/24 - Extracting RNA from LCM-captured cells (LCM date 6/13/24)

Used Quick-RNA™ Microprep [Kit](https://www.zymoresearch.com/products/quick-rna-microprep-kit), [protocol](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf) based off of a protocol used in [this paper](https://onlinelibrary.wiley.com/doi/full/10.1111/ics.12956)

### Sectioning performed on 6/12/24 and LCM on 6/14/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-2/) 

#### Protocol notes:

- Cells were collected directly into lysis buffer with no proteinase K digestion step or any other incubation steps. 
- Collected cells in 40 uL RNA lysis buffer in tube cap during LCM
  1. Spun down briefly in LCM room and let cells lyse for ~5 minutes at room temperature (seeing homogenous leeching of cresyl violet stain into solution) before transferring to tube rack on dry ice.
  2. Lysed cells tranferred on dry ice to -80ºC until extraction.
- During extraction:
  - Thaw tube on ice and then proceed
  - Added another 60 uL of RNA lysis buffer and vortex 5 seconds to homogenize and further lyse cells
  - Added equal volume of ethanol (100 uL) and mixed well by pipetting
  - Rest of protocol followed almost exactly as written. Eluted in 15 uL nuclease free water.
    - After last wash buffer I did modify the protocol slightly and moved the column to a new collection tube and spun dry for 2 minutes to try to remove any residual ethanol. Could try playing with this step since it is not in the protocol.

#### Qubit Results

- Used High Sensitivity RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 45.89 (S1) & 1056.01 (S2) (**used the HS qubit RNA kit from the fridge instead of molecular drawer, and normally the S2 value is much lower**)

| sample_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample 6/13 #3   |  nd |  nd        |   nd         |
| LCM sample 6/13 #7  |  nd |  nd        |   nd         |

#### RNA Quality Check: Tapestation

Maybe something! This really looks like RNA! And is DNA free as well. Especially in sample #7, which had a very large chunk of tissue and the lysis buffer was visibly purple from the cresyl violet.

![2024-06-13-RNAmicro.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-13-RNAmicro.JPG?raw=true)


Tapestation concentrations:

| sample_id | concentration |
|-----------|------------|
| LCM sample 6/13 #3   |  451 pg/uL (0.451 ng/uL) |
| LCM sample 6/13 #7  |   1240 pg/uL (1.240 ng/uL)  |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-13.pdf)
