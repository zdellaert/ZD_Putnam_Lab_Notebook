---
layout: post
title: 2023-01-23 E5 ACR Deep Dive RNA and DNA Extractions
date: '2023-01-23 16:00:00'
categories: Processing
tags: [DNA, RNA, E5, Acropora]
---

## RNA and DNA Extractions for E5 ACR Deep Dive Project, January 23, 2023

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

### Extraction of 18 ACR samples from Moorea from the E5 Time Series (Time Points 1 & 4, sampled January and November 2020)

## Samples

![2023-01-23-tubes.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2023-01-23-tubes.JPG?raw=true)
![2023-01-23-tubes-a.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2023-01-23-tubes-a.JPG?raw=true)
![2023-01-23-tubes-b.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2023-01-23-tubes-b.JPG?raw=true)

(*Note, the order of ACR-237 TP1 and TP4 are backward in this photo, but they were extracted in the right order.*)

![2023-01-23-caps-a.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2023-01-23-caps-a.JPG?raw=true)
![2023-01-23-caps-b.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/samples/2023-01-23-caps-b.JPG?raw=true)

## Notes

- I located these flash frozen samples on January 18 and clipped them following [this protocol](https://emmastrand.github.io/EmmaStrand_Notebook/KBay-Coral-Chipping-2021/) into 2.0 screw cap tubes with 1000 uL of DNA/RNA shield and 0.25 mL of 0.5mm glass beads. These were kept on dry ice during clipping and immediately put into the -80 ºC freezer.

- On extraction day, I did the following steps (homogenization very similar to how it is detailed in the [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/):
    1. Bead beat for 1-1.5 minutes on the vortex at max speed. I started off with one minute for all samples but added a minute of bead-beating for samples if the liquid still looked very light-colored after one minute of homogenization.
    2. Briefly spin down and remove 400 uL of supernatant into a clean tube. Spin for 3 mins at 9,000 rcf.
    3. Put original samples and bead tubes back in -80 ºC freezer.
    4. Remove 300 uL of the supernatant into a new tube and continue on with the protocol below (from the Pro K step) as written.

- Other than the adjustments mentioned above, I followed [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/) exactly.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

**Samples ACR-228 TP1 and ACR-234 TP1 were pale and were bead-beat for an extra 30 seconds to remove any last tissue. They had less tissue in the tubes than some of the other samples.**

 DNA Standards: 188.29 (S1) & 20735.98 (S2)
 
| colony_id | timepoint | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG |
|-----------|-----------|------------|------------|--------------|
| ACR-225   | TP1       | 93         | 94.2       | 93.6         |
| ACR-225   | TP4       | 115        | 116        | 115.5        |
| ACR-228   | TP1       | 40         | 40.2       | 40.1         |
| ACR-228   | TP4       | 9.26       | 9.62       | 9.44         |
| ACR-229   | TP1       | 194        | 195        | 194.5        |
| ACR-229   | TP4       | 96.6       | 98.8       | 97.7         |
| ACR-234   | TP1       | 44.4       | 45.2       | 44.8         |
| ACR-234   | TP4       | 60.2       | 61.6       | 60.9         |
| ACR-237   | TP1       | 67.8       | 69.2       | 68.5         |
| ACR-237   | TP4       | 150        | 155        | 152.5        |
| ACR-244   | TP1       | 47.2       | 48         | 47.6         |
| ACR-244   | TP4       | 93.8       | 96.4       | 95.1         |
| ACR-256   | TP1       | 85.6       | 87         | 86.3         |
| ACR-256   | TP4       | 98.6       | 99.6       | 99.1         |
| ACR-265   | TP1       | 38.2       | 38.6       | 38.4         |
| ACR-265   | TP4       | 109        | 107        | 108          |
| ACR-267   | TP1       | 82.4       | 84.6       | 83.5         |
| ACR-267   | TP4       | 67.2       | 67.4       | 67.3         |

 RNA Standards: 412.03 (S1) & 8733.93 (S2)

| colony_id | timepoint | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|-----------|------------|------------|--------------|
| ACR-225   | TP1       | 27.8       | 28.4       | 28.1         |
| ACR-225   | TP4       | 35         | 35.4       | 35.2         |
| ACR-228   | TP1       | 28         | 27.4       | 27.7         |
| ACR-228   | TP4       | 46.6       | 47.6       | 47.1         |
| ACR-229   | TP1       | 48.8       | 49.8       | 49.3         |
| ACR-229   | TP4       | 75         | 74.4       | 74.7         |
| ACR-234   | TP1       | 33.6       | 33.4       | 33.5         |
| ACR-234   | TP4       | 52         | 52         | 52           |
| ACR-237   | TP1       | 41.6       | 41.6       | 41.6         |
| ACR-237   | TP4       | 31.8       | 31.6       | 31.7         |
| ACR-244   | TP1       | 26.6       | 27         | 26.8         |
| ACR-244   | TP4       | 26.8       | 26.4       | 26.6         |
| ACR-256   | TP1       | 69.2       | 69.6       | 69.4         |
| ACR-256   | TP4       | 32.8       | 34         | 33.4         |
| ACR-265   | TP1       | 71.2       | 71.6       | 71.4         |
| ACR-265   | TP4       | 34.4       | 34.6       | 34.5         |
| ACR-267   | TP1       | 24.8       | 25         | 24.9         |
| ACR-267   | TP4       | 21.6       | 21.4       | 21.5         |

## DNA and RNA Quality Check: Gel

Using [Kristina's gel protocol at the bottom of this page.](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Protocols_Zymo_Quick_DNA_RNA_Miniprep_Plus/)

![2023-01-23-gel.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/gels/2023-01-23-gel.JPG?raw=true)

## RNA Quality Check: Tapestation

I ran a tapestation on three of these samples (ACR-225 TP1, ACR-244 TP1, ACR-256 TP1) on 01/25/2023 to confirm the degradation of the RNA. We also included three of Kristina's samples from the same set (one ACR #35 that did not work (ACR-234 TP1) and two that did: "41" (ACR-225 TP1) and "45" (ACR-256 TP1)). Hers were extracted from the molecular clippings preserved in the field in DNA/RNA shield.

Order:
| Ladder | Kristina's RNA | Kristina's RNA | Kristina's RNA | Zoe's RNA | Zoe's RNA | Zoe's RNA |
|----|----|----|----|----|----|----|
| Ladder | 35 (ACR-234 TP1) | 41 (ACR-225 TP1) | 45 (ACR-256 TP1) | ACR-244 TP1 | ACR-225 TP1 | ACR-256 TP1 |

Results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/29acef02b466112cef5ae8e8772fa567c3d7e346/images/tapestation/2023-01-25.pdf#L1)

## Next steps

While the concentration of all samples looks good, the DNA and RNA both appear to be highly degraded on the gel. I will run them on the tapestation to try to better understand what is going on. Data (including Kristina's original extraction data) are [here](https://docs.google.com/spreadsheets/d/1YQW_eSrx8G3aRED1sNt-cNuIOLqd7TfiNCBkCvEfwOU/edit?usp=sharing) (email me for access or request access at the link).

After running on the tapestation, the RNA appear severely degraded. We will reassess if we can utilize other samples that may not have thawed in transit. We could also try adjusting the homogenization technique and try immediately bead beating in DNA/RNA shield after clipping. The samples that Kristina used have been completely used up. 