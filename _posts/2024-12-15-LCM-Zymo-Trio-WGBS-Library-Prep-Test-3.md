---
layout: post
title: LCM Pilot Zymo Trio WGBS Library Prep Round 3
date: '2024-12-15'
categories: Processing
tags: [DNA, Pocillopora, LCM, Library Prep]
---

## LCM Zymo Trio WGBS Library Prep

Protocol link [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Zymo-Trio-WGBS-Library-Prep/)

## Samples: 12/15/24 Extraction of LCM Pilot Samples

| frag | sample_id      | concentration (ng/uL) | DIN | 
|---|----|------|-----|
| A | 1  | 4.35 | 3.4 |
| A | 3  | 4.08 | 3.4 |
| B | 11 | 3.41 | 3   |
| B | 12 | 3.61 | 3   |
| D | 24 | 3.63 | 3.1 |
| D | 25 | 3    | 1.8 |

- Eluted DNA in 20 uL Tris-HCl, used 2 uL for Qubit and 1 uL for gDNA tapestation
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-1-gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-3-gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-11-gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-12-gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-24-gDNA.png?raw=true" height="450">
- <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-25-gDNA.png?raw=true" height="450">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-15-WGBS-extraction-gDNA.pdf) (did not QC RNA)

## Library Prep

- 17 uL (brought up to 20 uL with 3uL Tris) processed using EZ Methylation Gold Kit for Bisulfite Conversion, cleaned according to protocol and eluted in 19 uL DNA elution buffer

### QC

Run to visualize libraries. Here's an example of what the **library should look like** on a Tapestation: 

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_QC.png?raw=true" height="400">

"If adapter dimers are present, they will form an approximately 130-180 bp band. Yields will vary depending on the total quantity and quality of sample input DNA.

## Results

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-libraries.png?raw=true" height="500">

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-1.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-3.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-11.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-12.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-24.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-25.png?raw=true" height="400">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-15-WGBS-Trio-Round3.pdf)

## Second Bead cleanup to remove Dimers and fragments > 1000bp:

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
- 31 left over to be re-cleaned up

## Results

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-16-WGBS-Cleaned-Libraries.png?raw=true" height="500">

YAY! these look good but need a final clean-up to remove dimers.

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-12-16-WGBS-Cleaned-Libraries.pdf)

## Final (Third) Bead cleanup to remove Dimers 

- Right sided size selection protocol based on Zymo Magbead Select-a-Size clean and concentrate [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manual_select-a-size_dna_magbead_kit.pdf).

1. Add 19 uL DNA elution buffer (EB) to bring volume to 50 uL
2. Deplete small fragments (< 200 bp) with another volume of beads
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