---
layout: post
title: LCM Pilot Zymo Trio WGBS Library Prep Round 1
date: '2024-12-06'
categories: Processing
tags: [DNA, Pocillopora, LCM, Library Prep]
---

## LCM Zymo Trio WGBS Library Prep

Protocol link [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Zymo-Trio-WGBS-Library-Prep/)

## Samples: Test extraction of LCM Pilot Samples #17 & 18 (12/6/24)

- Eluted DNA in 20 uL Tris-HCl, used 3 uL for Qubit and 1 uL for gDNA tapestation
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_17_gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_gDNA.png?raw=true" height="450">

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

| Sample       | Qubit (HS dsDNA) | Tapestation DIN | Tapestation Concentration | DNA in tube ng (*16uL) | Sonication  | Post-Sonication Concentration | ng input (by tapestation value) | PCR Cycles  |
|--------------|------------------|-----------------|---------------------------|----------------|-------------|-------------------------------|---------------------------------|-------------|
| #17 - EZ Gold | nd               | 1.9             | 3.7                       | 59.2           | NA          | NA                            | 29.6                            | 14          |
| #18 - EZ Gold  | nd               | 2.9             | 3.18                      | 50.88          | NA          | NA                            | 25.44                           | 14          |
| #18 - Sonicated | nd               | 2.9             | 3.18                      | 50.88          | 20 min, 50% | 0.16                          | 1.44                            | 14          |

### QC

Run to visualize libraries. Here's an example of what the **library should look like** on a Tapestation: 

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_QC.png?raw=true" height="400">

"If adapter dimers are present, they will form an approximately 130-180 bp band. Yields will vary depending on the total quantity and quality of sample input DNA.

## Results

- Quite a bit of primer dimer or adapter dimer, and also very low concentration. However, Zymo does not give an estimated ng output.
- It seems that the main issue here is our input amount. 
  - The samples prepped with the EZ Methylation Gold kit instead of sonication seemed to perform better. This is good to know. 
- However, it is worth noting that the bp-size of the library is longer than the expected size. 
- Questions to ask Zymo:
  - What are the expected final library concentrations?
  - Explanation behind the differences in the bead cleanups between FFPE and non-FFPE samples
  - Is the longer library size expected for FFPE samples?
    - Could this be due to the lower bead:sample ratio used in the FFPE preps?
  - Reduction of adapter dimers/primer dimers
- Moving forward:
  - Talk to Zymo
  - This is promising to use on our samples, with optimization. Worst case, we can pool the DNA across samples (within tissue type) to increase the input amount. And then sonicate or process with EZ Gold. 


<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_libraries.png?raw=true" height="500">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_17_library.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_library.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_sonicated_library.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-08-WGBS-Trio-Test.pdf)

## 12/12/24, Bead cleanup test:

- Double sided size selection protocol based on Zymo Magbead Select-a-Size clean and concentrate [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manual_select-a-size_dna_magbead_kit.pdf).

- Tried a double-sided bead cleanup on sample 18_sonicated to see if I can get a library of the right size:
  1. Add 31 uL DNA elution buffer (EB) to bring volume to 50 uL
  2. Bind larger fragments (> 900 bp) to beads to remove from sample:
     1. **0.52X ratio**: Add 26 uL beads
        1. total volume = 76 uL
     2. Mix thoroughly by pipetting until homogenous and incubate for 10 minutes at room temperature
     3. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
     4. Move 70 uL of supernatant to new tube *KEEP SUPERNATANT*. Discard the beads.
        1. 70/76 = 0.92 ; so new "initial volume" is 0.92*50 = 46 uL
  3. Add second volume of beads to supernatant tube to clean up all the fragments < 900 bp
     1. **1.28X ratio** = 1.28 * 46 uL = 59 uL
     2. Add 59 uL beads to the supernatant that was transferred into the new tube
     3. Mix thoroughly by pipetting until homogenous and incubate for 10 minutes at room temperature
     4. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
     5. Without removing from the magnetic stand, add 200 μL of **DNA Wash Buffer** to the tube, incubate for at least 30 seconds, and then remove the supernatant completely without disturbing the magnetized bead pellet. _**Repeat this wash step**_ for two washes total.
     6. Remove the tube from the magnetic stand and centrifuge very briefly. Then return the tube to the magnetic stand, wait for the beads to pellet, and remove any residual **DNA Wash Buffer** with a 10 μL pipette tip.
     7. Dry on magnetic stand for 2-3 minutes with cap open, do not over-dry beads
     8. Elute in 50 uL DNA EB. Fully resuspend beads and incubate for 5 minutes at room temperature.
     9. Place the tube back on the magnetic stand for 2 minutes or until the supernatant is clear.
     10. Transfer the indicated volume of eluate to a new tube. Discard the beads.
 4. Deplete small fragments with another volume of beads
     1.  **0.76X ratio** = 0.76 * 46 uL = 35 uL beads
         1.  honestly unclear if this should be *50 uL or *46 uL (38 uL beads vs 35 uL beads)
     2. Mix thoroughly by pipetting until homogenous and incubate for 10 minutes at room temperature
     4. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
     5. Without removing from the magnetic stand, add 200 μL of **DNA Wash Buffer** to the tube, incubate for at least 30 seconds, and then remove the supernatant completely without disturbing the magnetized bead pellet. _**Repeat this wash step**_ for two washes total.
     6. Remove the tube from the magnetic stand and centrifuge very briefly. Then return the tube to the magnetic stand, wait for the beads to pellet, and remove any residual **DNA Wash Buffer** with a 10 μL pipette tip.
     7. Dry on magnetic stand for 2-3 minutes with cap open, do not over-dry beads
     8. Elute in **15 uL DNA EB**. Fully resuspend beads and incubate for 5 minutes at room temperature.
     9. Place the tube back on the magnetic stand for 2 minutes or until the supernatant is clear.
     10. Transfer the indicated volume of eluate to a new tube. Discard the beads.
 5.  Honestly I feel that the second and third steps can be combined? This is how KAPA and other bead clean up protocols do it.

BUT! This was successful. Concentration low. But library looking much better:

**Original:**
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_sonicated_library.png?raw=true" height="400">

**Cleaned:**
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-08-LCM-WGBS-Trio-Test_18_sonicated_cleaned.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-12-WGBS-Trio-Cleaned.pdf)
