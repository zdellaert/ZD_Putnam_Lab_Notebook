---
layout: post
title: LCM Zymo Trio WGBS Library Prep Test
date: '2024-12-06'
categories: Processing
tags: [DNA, Pocillopora, LCM, Library Prep]
---

## LCM Zymo Trio WGBS Library Prep

Protocol link [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Zymo-Trio-WGBS-Library-Prep/)

## Samples: Test extraction of LCM Pilot Samples #17 & 18 (12/6/24)

- Eluted DNA in 20 uL Tris-HCl, used 3 uL for Qubit and 1 uL for gDNA tapestation
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_17_gDNA.png?raw=true" height="250">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_gDNA.png?raw=true" height="250">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-06-test-extraction-gDNA.pdf) (and [here for RNA](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-06-test-extraction-RNA.pdf))

## Library Prep

- Split samples in half:
  - 1: 8 uL of each sample processed using EZ Methylation Gold Kit for Bisulfite Conversion, cleaned according to protocol and eluted in 19 uL DNA elution buffer and stored at -20 ºC overnight 
  - 2: 8 uL of each sample sonicated 10 minutes at 50% amplitude using [Qsonica](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qsonica/)
    - Sample 17 was pretty degraded and did not have a clear chromatin peak. 
    - Sample 18 has a very small chromatin peak 
    - After sonication, sample 17 had bascially no DNA in the right size range, so I only moved on with # 18. However, the concentration of #18 was also very very low. 
      - <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_sonicated.png?raw=true" height="250">
        - Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-07-post-sonication-D5000.pdf)
    - Prepped 18 using Section 1 of the Zymo Trio kit (Lightning conversion), left at 4 ºC overnight and did the clean-up next day.
- Followed Sections 2-3 as written for the FFPE protocol for all 3 samples (17 (UI01), 18 (UI02), 18_Sonicated (UI03))
  - used 14 cycles for all samples in Section 3

## Results

- Quite a bit of primer dimer or adapter dimer, and also very low concentration. However, Zymo does not give an estimated ng output.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_libraries.png?raw=true" height="300">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_17_library.png?raw=true" height="300">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_library.png?raw=true" height="300">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_sonicated_library.png?raw=true" height="300">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-08-WGBS-Trio-Test.pdf)