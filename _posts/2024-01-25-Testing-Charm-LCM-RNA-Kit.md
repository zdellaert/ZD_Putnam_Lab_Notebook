---
layout: post
title: Testing Charm Biotech RNA Extraction on Cryosectioned and LCM-d P. acuta 
date: '2024-01-25'
categories: Processing
tags: [DNA, RNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Charm Kit on P. acuta

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Charm-LCM-RNA-Kit-Protocol/)

## 11/10/23 - Extracting RNA from LCM-captured RNA as well as from cryosections manually dissected fom slides

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM)Sample Total RNA/MicroRNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/c90a9f5225f541e20b15b3125f474c77712cd64b/protocols/Charm_Biotech_LCM_RNA_Kit.pdf)

### Sectioning performed on 10/23/23 and LCM on 10/24/23. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-LCM/)

- For the LCM sample, I had to make some adjustments to the protocol. After LCM, I originally resuspended the cells in 50 uL of RNAse/DNAse-free water, but I should have made digestion buffer and resuspended the captured cells in this. To try to make up for this, I made the digestion buffer at 2X concentration of BME and Proteinase K by doing the following:
    - 40 uL buffer RD2 + 9 uL Proteinase K + 2 uL BME
        - I later realized this was actually 4X concentration of BME...
- Then, I followed the protocol as written for FFPE, with a 3 hour digestion at 60 ºC.
- For the other two samples, I removed a cryosectioned slide from -80 ºC (same sample/sectioning round as used for LCM) thawed a slide on dry ice 
    - Rinsed slide in 70% Ethanol for 5 minutes on dry ice
    - Replaced ethanol with RNAse/DNAse-free water to rinse
    - Remove slide to dark background over PCR rack (over dry ice, though be careful to not freeze the water once the volume on the slide is low, if that's freezing move to regular ice) and use sterile razor blade, cleaned with RNAse cleaner, to scrape off tissue sections into a tube filled with prepared RD2 digestion buffer.
    - Then, I followed the protocol as written for FFPE, with a 3 hour digestion at 60 ºC.


#### Qubit Results

- Used Broad range RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 374.78 (S1) & 10451.62 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample "C"   |  nd |  nd        |   nd         |
| One Section  |  16.0   |  15.8      |   15.9       |
| Three Sections  |  21.0   |  21.2   |   21.1       |

#### RNA Quality Check: Tapestation

![2023-11-10.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2023-11-10.JPG?raw=true)

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2023-11-10.pdf)


## 1/25/24 - Extracting RNA from cryosections manually dissected fom slides, using frozen tissue protocol instead of FFPE protocol

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM)Sample Total RNA/MicroRNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/c90a9f5225f541e20b15b3125f474c77712cd64b/protocols/Charm_Biotech_LCM_RNA_Kit.pdf)

### Sectioning performed on 10/23/23 and LCM on 10/24/23. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-LCM/)

- Removed a cryosectioned slide from -80 ºC (same sample/sectioning round as used for LCM) thawed a slide on dry ice 
    - Rinsed slide in 70% Ethanol for 5 minutes on dry ice
    - Replaced ethanol with RNAse/DNAse-free water to rinse
    - Remove slide to dark background over PCR rack (over dry ice, though be careful to not freeze the water once the volume on the slide is low, if that's freezing move to regular ice) and use sterile razor blade, cleaned with RNAse cleaner, to scrape off tissue sections into a tube filled with prepared RD1 digestion buffer.
    - Then, I followed the protocol as written for frozen tissue, with a 1 hour digestion at 52 ºC.

#### Qubit Results

- Used Broad range RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 370.23 (S1) & 9494.15 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| Charm_Low_Input   |  10.8   |  10.4     |   10.6       |
| Charm_High_Input  |  10.8   |  11.0     |   10.9       |

#### RNA Quality Check: Tapestation

![2024-01-25.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-01-25.JPG?raw=true)

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-01-25.pdf)

### Thoughts:

It seems like the FFPE protocol/RD2 buffer worked better than the frozen one. Maybe we should try the RD2 protocol again but with a shorter incubation? The RIN was higher for the RD2 protocol (for FFPE).