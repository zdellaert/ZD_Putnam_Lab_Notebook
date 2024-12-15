---
layout: post
title: LCM Zymo Trio WGBS Library Prep Test
date: '2024-12-06'
categories: Processing
tags: [DNA, Pocillopora, LCM, Library Prep]
---

## LCM Zymo Trio WGBS Library Prep

Protocol link [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Zymo-Trio-WGBS-Library-Prep/)

## Samples: Test extraction of LCM Pilot Samples #32 & 33 (12/12/24)

- Eluted DNA in 20 uL Tris-HCl, used 3 uL for Qubit and 1 uL for gDNA tapestation
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-12-LCM-WGBS-Trio-Test_32_gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-12-LCM-WGBS-Trio-Test_33_gDNA.png?raw=true" height="450">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-12-test-extraction-gDNA.pdf) (did not QC RNA)

## Library Prep

- Split samples in half:
  - 1: 8 uL of each sample processed using EZ Methylation Gold Kit for Bisulfite Conversion, cleaned according to protocol and eluted in 19 uL DNA elution buffer
  - 2: Same as above, but using the "Alternative 2" protocol of the EZ Gold Kit.
    - 4 hours at 54 ºC instead of 2.5 hours at 63 ºC

- Based on assessment of the cleaned Bisulfite-converted DNA, the first reaction conditions worked better for sample 33 and the second one worked better for sample 32. That is frustrating. (see the end of this post for the details on this)
- Combined both reaction versions of the Bisulfite-converted DNA samples back together and used Zymo clean & concentrate kit to concentrate each sample to 19 uL. 
- Followed Sections 2-3 as written for the FFPE protocol for all both samples (32 (UI04), 33 (UI05)
  - used 14 cycles for all samples in Section 3

| Sample       | Qubit (HS dsDNA) | Tapestation DIN | Tapestation Concentration | DNA in tube ng (*16uL) | Sonication  | Post-Sonication Concentration | ng input (by tapestation value) | PCR Cycles  |
|--------------|------------------|-----------------|---------------------------|----------------|-------------|----------------|---------------------------------|-------------|
| #32 - EZ Gold | 0.06643333333      | 2.3      | 4.86              | 77.76     | NA             | NA          | 77.76            | 14          |
| #33 - EZ Gold  | nd               | 3.2       | 4.56              | 72.96     | NA             | NA          | 72.96         | 14          |

### QC

Run to visualize libraries. Here's an example of what the **library should look like** on a Tapestation: 

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_QC.png?raw=true" height="400">

"If adapter dimers are present, they will form an approximately 130-180 bp band. Yields will vary depending on the total quantity and quality of sample input DNA.

## Results

- Bleh, even though double the DNA went in, these reactions produced libraries of lower concentration than in my first test. 
- Going to try a reamplification protocol

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_libraries.png?raw=true" height="500">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_32_library.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_32_library.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-14-WGBS-Trio-Test.pdf)

## Re-Amplification

1. Combine 30 uL PCR Pre-Mix, 12 uL primer, and 18 uL of the original library. Cycle with same conditions above, for 8 cycles.

THIS WORKED!!! WOAH! Almost too good!!! Will maybe do another cleanup to remove some of the larger fragments. So happy!!!!!

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_libraries-ReAmp.png?raw=true" height="500">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_32_library-ReAmp.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_32_library-ReAmp.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-14-WGBS-Trio-Test-ReAmp.pdf)


## Notes on EZ Gold Reaction conditions

1. Motivation: The libraries I prepped on 12/8 are of longer lengths than we want. Therefore, this protocol is not really fragmenting our DNA the way we want it to.
2. Method: Try a longer incubation with the Bisulfite Conversion reagent at a slighlty lower temperature, "Alternative 2" in the EZ Gold protocol:
   1. Standard method (A):
      1. 98°C for 10 minutes
      2. 64°C for 2.5 hours
      3. 4°C storage for up to 20 hours
   2. Alternative 2 (B):
      1. 98°C for 10 minutes
      2. 53°C for 4 hours
      3. 4°C storage

Did this on both my samples. Split the 16 uL from each sample so 8 uL went into each reaction. Made up volume with 12 uL tris buffer, and added 130 uL of the CT Reagent from the EZ Gold Kit (prepared 12/6/24)

### Results

- There is no clear winner. First of all, the DNA is not getting fragmented as much as we want. The DNA barely shows up on a D5000 tapestation. Had to run a gDNA tapestation.
