---
layout: post
title: Fixing Coral Tissues for Protocol Testing
date: '2023-08-30'
categories: Processing
tags: [DNA, RNA, PAXgene, Fixative, Pocillopora]
---

## Fixing and decalcifying 16 branches of Pocillopora tissue for testing protocols

### Protocol [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/PAXgene-Fix-Decalc-Protocol/)

1. Fixed 16 branches, see protocol post above for images
    - 4 per tissue casette
    - Day 1 (8/30/23): Fixed tissue in PAXgene fixative
    - Day 2 (8/31/23): Replaced fixative with stabilizer, transferred to 4 ºC
    - Day 3 (9/1/23): Started decalcification, kept on shaker in cold room (4 ºC)
    - Day 4 (9/2/23): Changed EDTA solution
    - Day 5 (9/3/23): Decalcification done, tissue washed and transferred to PAXgene stabilizer at -80 ºC
2. Planned RNA Extractions to test effects on RNA integrity at each step
   - Pre-decalc ("control") (put at -80 ºC on 9/1/23), **extracted 9/18/23**
   - Post-decalc (put at -80 ºC on 9/3/23), **extracted 9/18/23**
   - Pre-sucrose (-80 ºC 9/3/23-10/17/23), **extracted 10/22/23**
   - Post-surcrose (-80 ºC 9/3/23-10/16/23, 30% sucrose overnight) **extracted 10/22/23**
   - Try to extract RNA from sections after sectioning

   Weighing starting material to try to keep it consistent is a good idea. 


9/7/23 - test for Hollie for fixing branches in smaller volumes (good for samples we want to keep apart by treatment or species, for example)

Fixed two branches in PAXgene in smaller volumes to test efficacy

"2mL" = fixed in 2 mL of PAXgene fixative in a 2mL tube, **extracted 9/18/23**

"4mL" = fixed in 4 mL of PAXgene fixative in a 5mL tube, **extracted 9/18/23**

- Day 1 (9/7/23): Fixed tissue in PAXgene fixative
- Day 2 (9/8/23): Replaced fixative with stabilizer, transferred to 4 ºC
- Day 3 (9/9/23): Started decalcification, kept on shaker in cold room (4 ºC)
- Day 4 (9/10/23): Changed EDTA solution
- Day 5 (9/11/23): Decalcification done, tissue washed and transferred to PAXgene stabilizer at -80 ºC


### 9/18/23 DNA/RNA extraction results
#### [DNA/RNA Extraction Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

Followed this [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly, but followed steps for samples preserved in RNAlater. Bead-beat for 2 minutes in 1mL of DNA/RNA shield.

Eluted DNA in 100 uL of Tris-EDTA and RNA in 50 uL of DNAse/RNAse free water (reapplied first elution to membrane)

#### Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 192.82 (S1) & 21315.79 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| Control   |  34.8   |  34.4   |   34.6    |
| Decalc    |  2.66   |  2.58   |   2.62    |
| 2mL       |   nd    |   nd    |      nd   |
| 4mL       |  2.74   |  2.60   |    2.67   |

-----


 RNA Standards: 400.14 (S1) & 10504.23 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| Control   |  50.6   |  50.4   |   50.5    |
| Decalc    |  17.8   |  17.8   |   17.8    |
| 2mL       |  14.6   |  14.6   |   14.6    |
| 4mL       |  27.2   |  27.0   |   27.1    |

#### DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2023-09-18-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-09-18-gel.JPG?raw=true)


### 10/16/23 - Starting cryoprotection of 3 branches to test effects of cryoprotection on RNA integrity (using 1 branch + 1 branch not cryoprotected) and to cryosection 2 branches

- one fragment appears not fully decalcified and sunk immediately in the sucrose - will use this one for the extraction test instead of continuing on to embedding to minimize possible negative effects of leftover calcium carbonate on the cryosectioning process.

### 10/22/23 - Test effects of cryoprotection on RNA integrity (using 1 branch + 1 branch not cryoprotected)

#### DNA/RNA extraction results

#### [DNA/RNA Extraction Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

Followed this [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly, but followed steps for samples preserved in RNAlater. Bead-beat for 2 minutes in 1mL of DNA/RNA shield. **Bead-beat on 10/17/23 in DNA/RNA shield and then placed in -80 until extraction on 10/22/23**

Eluted DNA in 100 uL of Tris-EDTA and RNA in 50 uL of DNAse/RNAse free water (reapplied first elution to membrane)

#### Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 DNA Standards: 180.30 (S1) & 18470.25 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| pre-sucrose  |  7.42   |  7.52      |   4.47       |
| post-sucrose |  10.3   |  10.5      |   10.4       |

-----

 RNA Standards: 378.90 (S1) & 10301.47 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| pre-sucrose   |  26.8   |  26.8   |   26.8    |
| post-sucrose  |  52.6   |  52.8   |   52.7    |

#### DNA and RNA Quality Check: Gel, using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2023-10-22-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-10-22-gel.JPG?raw=true)


### 10/17/23 - Embed the two other cryoprotected branches for cryosectioning on 10/23/23

### 10/23/23 - Cryosection the two branches to make several slides. Goal: make several normal slides for test extractions and confocal imaging. Also make sections for test LCM slides received from Giuseppe at College of Pharmacy on 10/16/23.