---
layout: post
title: Nuclei Isolation for Coral single nuclei RNA-seq 
date: '2026-07-16 7:00:00'
categories: Protocols, Processing
tags: [Pocillopora, Porites, Montipora]
---

# Nuclei Isolation for Coral single nuclei RNA-seq 

- [**Protocol**](#protocol)
    - [Levitas protocol notes (https://levitasbio.com/leviprep/nuclei-kit/)](#levitas-protocol-notes-httpslevitasbiocomleviprepnuclei-kit)
- [**Final Nuclei QC:**](#final-nuclei-qc)
  - [Montipora](#montipora)
  - [Porites](#porites)
  - [Pocillopora](#pocillopora)

## Protocol

1. Soak frozen tissue in Ca2+ Mg2+ free PBS for 20 minutes (7 mL + 3 uL RNAseOut)
    1. 7 mL PBS (ph 7.2, Ca2+/Mg2+-free, Thermo Fisher Cat #20012027) with 3 μL RNAseOut RNAse inhibitor (Thermo Fisher Cat #10777019). 
3. Pour off PBS and immediately waterpik as much tissue off the skeleton with fresh PBS
   1. _CVS Water Flosser Cat #638777_
   1. try to use < 30 mL PBS total per fragment
   2. Realistically we had to use ~ 45 mL per fragment
4. Filter slurry through 70 um filter into new conical tube
5. Spin tissue slurry at 100 rcf for 10 min at 4 ºC
   1. GOAL: pellet syms, not nuclei -- will naturally lose nuclei.
6. Move supernatant to new tube and spin this at 700 rcf for 5 minutes at 4 ºC
   1. GOAL: pellet nuclei
7. Discard supernatant (save if nervous)
8. Immediatelly proceed with Levitas protocol for NIB lysis of pellet:
   1. Resuspend pellet in 200-500 uL of NIB (we shot for a 1:2 ratio of pellet to lysis buffer) with a wide-bore tip and move to a 1.5 mL tube
   2. Recipie at end of protocol
   3. Buffer NIB, LeviPrep Nuclei Kit II; Levitas #1005055
   4. https://levitasbio.com/leviprep/nuclei-kit/
9. Homogenize slurry with a sterile pestle, 10X
   1. Do not over homogenize!
10. Incubate homogenized tissue on ice for 5 min
11. Pre-wet a 40 um strainer over a pre-labelled 50 mL tube with 500 uL of 1X Wash buffer 
12. Pipet the entire sample through the 40 um strainer into the 50 mL tube
13. Rinse the 1.5 mL tube and strainer with 4 mL of ice-cold 1X Wash Buffer. Total volume should be 5 mL
14. Centrifuge the sample 4 ºC, 500 rcf for 3 min at 4 ºC
15. *Here the levitas protocol has another wash which we skipped due to pre-filtering and wanting to process the nuclei as fast as possible*
16. Remove supernatant (as much as comfortable) and resuspend in 50 uL PBS-BSA with a wide-bore tip
    1.  Because of leftover supernatant in pellet, final resuspension volume will be closer to 150 uL 
17. QC nuceli in final pellet and prepare for chromium
    1.  to QC: 5 uL Trypan Blue + 5 uL Nuclei suspension, count on hemocytometer
18. If there is still clumps of debris in the QC, pass whole suspension through a Flow-Mi filter
19. Dilute nuclei suspension as needed to achieve between 300 (minimum) - 2000 nuclei/uL
20. Proceed immediately with Chromium Gem-X 3' Chip loading for a targeted recovery of 6,000 cells.

#### Levitas protocol notes (https://levitasbio.com/leviprep/nuclei-kit/)

NIB Buffer recipie:

| Reagent     | Volume for 1 sample (uL), with overage | Volume for 3 samples | 
|-------------|------------------------------------|----------------------|
| Buffer N3   |             506                    |        1518          |
| Component L |             6                      |        18            |
| Component R |             3                      |        9             |
| Component A |             58                     |        174           |
| RNAseOut    |             3                      |        9             |
| **Total**   |             **576**                |        **1728**      |

Notes from levitas:
- When homogenizing soft tissue, go straight up and down and do not twist or grind the sample - to reduce nuclei clumps
- For tougher organs, the pestle can be twisted by a quarter turn
- When mixing, set pipette to half the volume of the sample and pipette mix 1-2 times per second for a total of 5-10 times for best results. Avoid vortexing or aggressive mixing.

## **Final Nuclei QC:**

Overview:

| Species | QC Description | Nuclei Count  | Result |
|---------|----------------|---------------|--------|
| *Montipora capitata* (MON)| Pre-FlowMi     |  1600 nuclei/uL in 175 uL    |  Whole volume passed through FlowMi filter (40 um)   |
| ***Montipora capitata* (MON)**| **Post-FlowMi**    |  **1280 nuclei/uL in 170 uL**    | **Nuclei suspension used for Chromium!**  |
| *Porites compressa* (POR) | Pre-FlowMi      |  960 nuclei/uL in 145 uL    |  Whole volume passed through FlowMi filter (40 um)   |
| ***Porites compressa* (POR)** | **Post-FlowMi**    |  **700 nuclei/uL in 140 uL**     |  **Nuclei suspension used for Chromium!**  |
| *Pocillopora acuta* (POC) | Pre-dilution   |  24,960 nuclei/uL in 153 uL    |  Suspension diluted and re-QC'd   |
| *Pocillopora acuta* (POC) | 1:12 dilution   |  3520 nuclei/uL in 120 uL   |  Original suspension diluted and re-QC'd   |
| ***Pocillopora acuta* (POC)** | **1:24 dilution**    |  **1200 nuclei/uL in 240 uL**  |  **Nuclei suspension used for Chromium!**  |

### Montipora

| QC Description | Magnification | Image | Nuclei Count | Result |
|----------------|---------------|-------|--------------|--------|
| Pre-FlowMi     |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/MON_20250117/MON_20250117_Nuclei_10X.jpeg" style="width: 100%; height: auto;" ></div> | 1600 nuclei/uL in 175 uL |  Whole volume passed through FlowMi filter (40 um)   |
| Pre-FlowMi     |  20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/MON_20250117/MON_20250117_Nuclei_20X.jpeg" style="width: 100%; height: auto;" ></div> | " |   "  |
| Post-FlowMi    | 10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/MON_20250117/MON_20250117_Nuclei_Final_FlowMi_10X.jpeg" style="width: 100%; height: auto;" ></div>  |  1280 nuclei/uL in 170 uL  |  Nuclei suspension used for Chromium!  |

### Porites

| QC Description | Magnification | Image | Nuclei Count | Result |
|----------------|---------------|-------|--------------|--------|
| Pre-FlowMi     |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_10X_1.jpeg" style="width: 100%; height: auto;" ></div> | 960 nuclei/uL in 145 uL |  Whole volume passed through FlowMi filter (40 um)   |
| Pre-FlowMi     |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_10X_2.jpeg" style="width: 100%; height: auto;" ></div> | " |   "  |
| Pre-FlowMi     |  20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_20X_1.jpeg" style="width: 100%; height: auto;" ></div> | " |   "  |
| Pre-FlowMi     |  20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_20X_2.jpeg" style="width: 100%; height: auto;" ></div> | " |   "  |
| Post-FlowMi    | 10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_Final_FlowMi_10X.jpeg" style="width: 100%; height: auto;" ></div>  |  700 nuclei/uL in 140 uL  |  Nuclei suspension used for Chromium!  |
| Post-FlowMi    | 20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_Final_FlowMi_20X_1.jpeg" style="width: 100%; height: auto;" ></div>  | " |   "  |
| Post-FlowMi    | 20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POR_20250117/POR_20250117_Nuclei_Final_FlowMi_20X_2.jpeg" style="width: 100%; height: auto;" ></div>  | " |   "  |

### Pocillopora

| QC Description | Magnification | Image | Nuclei Count | Result |
|----------------|---------------|-------|--------------|--------|
| Pre-dilution     |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_10X.jpeg" style="width: 100%; height: auto;" ></div> | 24,960 nuclei/uL in 153 uL |  Suspension diluted and re-QC'd  |
| Pre-dilution     |  20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_20X.jpeg" style="width: 100%; height: auto;" ></div> | " |   "  |
| 1:12 dilution of original suspension   |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_dilution1to12_10X_1.jpeg" style="width: 100%; height: auto;" ></div> | 3520 nuclei/uL in 120 uL |  Original suspension diluted further and re-QC'd  |
| 1:12 dilution of original suspension   |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_dilution1to12_10X_2.jpeg" style="width: 100%; height: auto;" ></div> | "|  "  |
| 1:12 dilution of original suspension   |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_dilution1to12_10X_3.jpeg" style="width: 100%; height: auto;" ></div> | "|  "  |
| 1:12 dilution of original suspension   |  20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_dilution1to12_20X.jpeg" style="width: 100%; height: auto;" ></div> | "|  "  |
| 1:24 dilution of original suspension   |  10X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_Final_dilution1to24_10X.jpeg" style="width: 100%; height: auto;" ></div> | 1200 nuclei/uL in 240 uL |  Nuclei suspension used for Chromium!  |
| 1:24 dilution of original suspension   |  20X  | <div style="width: 390px;"><img src="../images/protocols/nuclei-isolation/20250117/POC_20250117/POC_20250117_Nuclei_Final_dilution1to24_20X.jpeg" style="width: 100%; height: auto;" ></div> | " |  " |
