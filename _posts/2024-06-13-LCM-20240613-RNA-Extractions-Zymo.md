---
layout: post
title: Testing Zymo Quick RNA Microprep Kit on Cryosectioned and LCM-d P. acuta 
date: '2024-06-13'
categories: Processing
tags: [RNA, Pocillopora, LCM]
---

## Testing Zymo Quick-RNA Microprep Kit on LCM Samples

### [Protocol Link](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf)

## 6/13/24 - Extracting RNA from LCM-captured cells (LCM date 6/13/24)

Used Quick-RNA™ Microprep [Kit](https://www.zymoresearch.com/products/quick-rna-microprep-kit), [protocol](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf) based off of a protocol used in [this paper](https://onlinelibrary.wiley.com/doi/full/10.1111/ics.12956)

### Sectioning performed on 6/12/24 and LCM on 6/13/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-2/) 

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
- **Tube #7 had a big chunk of tissue and the lysis buffer was visibly purple from the cresyl violet stain**

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

| sample_id | concentration | RIN |
|-----------|------------|------------|
| LCM sample 6/13 #3   |  451 pg/uL (0.451 ng/uL) | - |
| LCM sample 6/13 #7  |   1240 pg/uL (1.240 ng/uL)  | 1.5 | 

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-13.pdf)

## I also tried one sample with an expired Zymo Quick [DNA/RNA Microprep](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf) sample kit, on sample #5. Neither the DNA or RNA extractions of these were successful, but here are some notes.

- Basically exact same protocol as the Quick RNA but you spin the lysis buffer on a DNA column before adding ethanol, and instead you add ethanol to the flow-through of this column and the proceed with this onto the RNA column. Perform DNAse digestion on the RNA column and then all steps after are the same washes and such.

#### Qubit Results

- Used High Sensitivity RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

  RNA Standards: 45.89 (S1) & 1056.01 (S2) (**used the HS qubit RNA kit from the fridge instead of molecular drawer, and normally the S2 value is much lower**)

| sample_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample 6/13 #5  |  nd |  nd        |   nd      |

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 61.30 (S1) & 21623.16 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample 6/13 #5  | nd |  nd        |   nd      |


#### RNA Quality Check: Tapestation

Nada.

Tapestation concentrations:

| sample_id | concentration | RIN |
|-----------|-----------|------|
| LCM sample 6/13 #5  |   451 pg/uL (0.451 ng/uL)  | 1.0 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-13.pdf)

#### DNA Quality Check: Tapestation

Nada.

![2024-06-17-DNAZymoDNARNAmicro5.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17-DNAZymoDNARNAmicro5.JPG?raw=true)

Tapestation concentrations:

| sample_id | concentration | 
|-----------|-------------------------------------|
| LCM sample 6/13 #5  |    - |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17-DNA.pdf)

## Modifications to protocol to try:

- Elute in less volume?
- Be faster in general with the extraction - dont do the long spins
- Try a proteinase K digestion?
  - 15 mins at 56 ºC?
    - 100 uL sample in lysis buffer + 10 uL PK digestion buffer + 5 uL PK
    - then add 115 uL ethanol after 15 mins

## 6/17/24 - Extracting RNA from LCM-captured cells (LCM date 6/13/24) with ProK digestion

Used Quick-RNA™ Microprep [Kit](https://www.zymoresearch.com/products/quick-rna-microprep-kit), [protocol](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf) based off of a protocol used in [this paper](https://onlinelibrary.wiley.com/doi/full/10.1111/ics.12956)

### Sectioning performed on 6/12/24 and LCM on 6/13/24. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Test-2/) 

#### Protocol notes:

- Same as above. Same sample and LCM date, but adding a ProK digestion step to see if this helps or hurts our problem. Tried to be extra quick with spins and only did the final dry spin for 1 minute. Let the water sit on column for 5 whole minutes before elution spin to fully soak column.

#### Qubit Results

- Used High Sensitivity RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 28.29 (S1) & 301.79 (S2)

| sample_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample 6/13 #8  |  nd |  nd        |   nd         |

#### RNA Quality Check: Tapestation

Maybe something! But, more degraded than last week (see above). The ProK did not seem to increase RNA concnetration but may have introduced degredation. This is super helpful to know! We can skip this :) 

![2024-06-17-RNAmicro.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17-RNAmicro.JPG?raw=true)

Tapestation concentrations:

| sample_id | concentration | RIN  | DV200 | 
|-----------|------------|------------|------|
| LCM sample 6/13 #8  |   735 pg/uL (0.735 ng/uL)  | 2.1 | 56.31 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17.pdf)


## I also tried one sample with an expired Zymo Quick [DNA/RNA Microprep](https://files.zymoresearch.com/protocols/_d7005t_d7005_quick-dna-rna_microprep_plus_kit.pdf) sample kit, on sample #6. Neither the DNA or RNA extractions of these were successful, but here are some notes.

- Same protocol as 6/13 for Quick DNA/RNA but with the same 15 minute proK digestion mentioned above for the other 6/17 extraction.
 
#### Qubit Results

- Used High Sensitivity RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 28.29 (S1) & 301.79 (S2) 

| sample_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample 6/13 #6  |  nd |  nd        |   nd      |

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 64.64 (S1) & 23642.49 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample 6/13 #6  | nd |  nd        |   nd      |

#### RNA Quality Check: Tapestation

Nada.

![2024-06-17-ZymoDNARNAmicro.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17-ZymoDNARNAmicro.JPG?raw=true)

Tapestation concentrations:

| sample_id | concentration |  RIN | DV200 | 
|-----------|-------------------------------------|----|----|
| LCM sample 6/13 #6  |   302 pg/uL (0.302 ng/uL)  | - | 62.59 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17.pdf)

#### DNA Quality Check: Tapestation

Nada.

![2024-06-17-DNAZymoDNARNAmicro5.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17-DNAZymoDNARNAmicro6.JPG?raw=true)

Tapestation concentrations:

| sample_id | concentration | 
|-----------|-------------------------------------|
| LCM sample 6/13 #6  |    - |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-06-17-DNA.pdf)
