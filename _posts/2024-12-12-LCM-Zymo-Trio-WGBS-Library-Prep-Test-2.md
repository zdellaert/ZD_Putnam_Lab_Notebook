---
layout: post
title: LCM Pilot Zymo Trio WGBS Library Prep Round 2
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
| #32 - EZ Gold | 0.066      | 2.3      | 4.86              | 77.76     | NA             | NA          | 77.76            | 14          |
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
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_33_library.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-14-WGBS-Trio-Test.pdf)

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

- There is no clear winner. First of all, the DNA is not getting fragmented as much as we want. The DNA barely shows up on a D5000 tapestation (results [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-13-EZ-Gold-D5000.pdf)). Had to run a gDNA tapestation (results [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-13-EZ-Gold-gDNA.pdf)).

**gDNA Comparisons (ORANGE = original extraction gDNA profile):**

Sample 32

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-13-Comparison-gDNA-32-all.png?raw=true" height="400">

Sample 33

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-13-Comparison-gDNA-33-all.png?raw=true" height="400">


**D5000 Comparisons:**

Sample 32

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-13-Comparison-d5000-32.png?raw=true" height="400">

Sample 33

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-13-Comparison-d5000-33.png?raw=true" height="400">


## Re-Amplification

1. Combine 30 uL PCR Pre-Mix, 12 uL primer, and 18 uL of the original library. Cycle with same conditions above, for 8 cycles.

THIS WORKED!!! WOAH! Almost too good!!! Will maybe do another cleanup to remove some of the larger fragments. So happy!!!!!

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_libraries-ReAmp.png?raw=true" height="500">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_32_library-ReAmp.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-14-LCM-WGBS-Trio-Test_33_library-ReAmp.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-14-WGBS-Trio-Test-ReAmp.pdf)


## Second Bead cleanup to remove fragments > 1100bp:

For the re-amped libraries (17, 18, 32, 33), there are not big dimers, but there are a lot of fragments > 1100. I will remove them as such:

- Double sided size selection protocol based on Zymo Magbead Select-a-Size clean and concentrate [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manual_select-a-size_dna_magbead_kit.pdf).

1. Add 32 uL DNA elution buffer (EB) to bring volume to 50 uL
2. Bind larger fragments (> 1100 bp) to beads to remove from sample:
   1. **0.48X ratio**: Add 24 uL beads
      1. total volume = 74 uL
   2. Mix thoroughly by pipetting until homogenous and incubate for 10 minutes at room temperature
   3. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
   4. Move 74 uL of supernatant to new tube *KEEP SUPERNATANT*. Discard the beads.
3. Add second volume of beads to supernatant tube to clean up all the fragments < 1000 bp
   1. **1.32X ratio** = 1.32 * 50 uL = 66 uL
   2. Add 66 uL beads to the supernatant that was transferred into the new tube
   3. Mix thoroughly by pipetting until homogenous and incubate for 10 minutes at room temperature
   4. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
   5. Carefully remove the supernatant without disturbing the magnetized bead pellet.
   6. Without removing from the magnetic stand, add 200 μL of **DNA Wash Buffer** to the tube, incubate for at least 30 seconds, and then remove the supernatant completely without disturbing the magnetized bead pellet. _**Repeat this wash step**_ for two washes total.
   7. Remove the tube from the magnetic stand and centrifuge very briefly. Then return the tube to the magnetic stand, wait for the beads to pellet, and remove any residual **DNA Wash Buffer** with a 10 μL pipette tip.
   8. Dry on magnetic stand for 2-3 minutes with cap open, do not over-dry beads
   9. Elute in 50 uL DNA EB. Fully resuspend beads and incubate for 5 minutes at room temperature.
   10. Place the tube back on the magnetic stand for 2 minutes or until the supernatant is clear.
   11. Transfer the indicated volume of eluate to a new tube. Discard the beads.
4. Deplete small fragments (< 200 bp) with another volume of beads
   1.  **0.8X ratio** = 0.8 * 50 uL = 40 uL beads
   2. Mix thoroughly by pipetting until homogenous and incubate for 10 minutes at room temperature
   3. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
   4. Carefully remove the supernatant without disturbing the magnetized bead pellet.
   5. Without removing from the magnetic stand, add 200 μL of **DNA Wash Buffer** to the tube, incubate for at least 30 seconds, and then remove the supernatant completely without disturbing the magnetized bead pellet. _**Repeat this wash step**_ for two washes total.
   6. Remove the tube from the magnetic stand and centrifuge very briefly. Then return the tube to the magnetic stand, wait for the beads to pellet, and remove any residual **DNA Wash Buffer** with a 10 μL pipette tip.
   7. Dry on magnetic stand for 2-3 minutes with cap open, do not over-dry beads
   8. Elute in **33 uL DNA EB**. Fully resuspend beads and incubate for 5 minutes at room temperature.
   9. Place the tube back on the magnetic stand for 2 minutes or until the supernatant is clear.
   10. Transfer 32 uL of eluate to a new tube. Discard the beads.

- 1 uL used for D5000 Tapestation
- 1 uL used for Qubit
- 30 uL final volume for Sequencing, move to LoBind tube.

## Results

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-16-WGBS-Cleaned-Libraries-ReAmps.png?raw=true" height="500">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-16-LCM-WGBS-Trio-library-17-ReAmp-clean.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-16-LCM-WGBS-Trio-library-18-ReAmp-clean.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-16-LCM-WGBS-Trio-library-32-ReAmp-clean.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-16-LCM-WGBS-Trio-library-33-ReAmp-clean.png?raw=true" height="500">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-16-WGBS-Cleaned-Libraries.pdf)

These are done.