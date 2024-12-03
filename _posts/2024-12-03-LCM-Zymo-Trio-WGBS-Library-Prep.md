---
layout: post
title: LCM Zymo Trio WGBS Library Prep
date: '2024-12-03'
categories: Protocols
tags: [DNA, Pocillopora, LCM, Library Prep]
---

## LCM Zymo Trio WGBS Library Prep

Product: [Zymo-Seq™ Trio WGBS Library Kit](https://www.zymoresearch.com/products/zymo-seq-trio-wgbs-library-kit)

See [Zymo's protocol here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manual_trio_wgbs.pdf).

### Here's the Zymo Trio WGBS library prep workflow: 

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs.png?raw=true" height="500">

### Materials 

- [Kit contents](https://www.zymoresearch.com/products/zymo-seq-trio-wgbs-library-kit)
- PCR tubes, 1.5 mL tubes 
- Two thermocyclers
- Heating block 
- Mini centrifuge
- Vortex, shaker
- Aluminum beads (to keep things on ice)
- Magnetic stand for PCR tubes 
- Custom index primers for Illumina if you have more than 12 samples (Zymo kit provides 12)

#### Kit contents

| Zymo-Seq™ Trio WGBS Library Kit   | D5462 (25 preps) | Storage Temperature  |
|-----------------------------------|------------------|----------------------|
| Lightning Conversion Reagent      | 4.5 ml           | Room Temp.           |
| M-Binding Buffer                  | 20 ml            | Room Temp.           |
| M-Wash Buffer                     | 6 ml (conc.)     | Room Temp.           |
| L-Desulphonation Buffer           | 10 ml            | Room Temp.           |
| DNA Elution Buffer                |  4 ml            | Room Temp.           | 
| Zymo-Spin™ IC Columns             |  25              | Room Temp.           |
| Collection Tubes                  |  25              | Room Temp.           |
| DNA Wash Buffer                   |  6 ml (conc.)    | Room Temp.           |
| Select-a-Size MagBeads            |  10 mL           |  4 ºC                |
| *E coli* Non-Methylated gDNA      |  5 μg/20 μL      |       -20 °C         |
| Adapter Ligation Buffer 1         |  48 μL           |       -20 °C         |
| Adapter Ligation Buffer 2         |  48 μL           |       -20 °C         |
| Adapter Ligation Buffer 3         |  48 μL           |       -20 °C         |
| Adapter Ligation Master Mix       |  625 μL          |       -20 °C         |
| 2X Index PCR Premix               |  600 μL          |       -20 °C         |
| Zymo-Seq UDI Primer Set (1-12)    |  20 μL/Index     |       -20 °C         |

## Protocol

### Buffer preperation 

Once buffers are prepared for a kit, they do not need to be prepared again. 

- Add 300 uL of the Select-a-Size MagBead Concentrate to the 10 mL Select-a-Size MagBead Buffer bottle
  - Resuspend by vortexing and store at 4 ºC
- Add 24 mL of 100% EtOH to the M-Wash Buffer concentrate
- Add 24 mL of 100% EtOH to the DNA Wash Buffer concentrate

### Best practices 

- Preset the thermocycler programs 
- Thaw and keep -20°C components on ice unless instructed otherwise. Flick to mix and centrifuge before use
	- Avoid multiple freeze-thaws, make aliquots if needed
- Allow beads to equilibrate to room temperature >30 mins before use
- Resuspend magnetic particles immediately before each use by vortexing until homogenous

### I am following the modifications for FFPE DNA! (Appendix F)

1. In **Section 2, Step 11**: After the 1-hour adapter ligation reaction, add 85 μL of *DNA Elution Buffer* to the sample to bring the volume up to 135 μL and mix well by pipetting.
2. In **Section 2, Step 12**: Follow the clean-up protocol in **Appendix A** on pg. 13 using 50 μL of *Select-a-Size MagBeads*. Allow beads to equilibrate to room temperature for 30 minutes prior to use. For elution, resuspend the beads in 15 μL of *DNA Elution Buffer* and aspirate all 15 μL eluate into a new tube after separation from the beads.
3. In **Section 3, Step 3**: The recommended number of PCR cycles may be increased to the following depending on the FFPE DNA sample input amount and type used:

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_cycles.png?raw=true">

1. In **Section 3, Step 4**: Follow the clean-up protocol in **Appendix A** on pg. 13 using 40 μL of *Select-a-Size MagBeads*. Allow beads to equilibrate to room temperature for 30 minutes prior to use. For elution, resuspend the beads in 20 μL of *DNA Elution Buffer* and aspirate all 20 μL eluate after separation from the beads.

### Section 1: Bisulfite Conversion of DNA (same as Pico Kit)

- [ ] Thaw samples on ice 
- [ ] Prepare samples with Tris buffer to desired input amount (5-10ng) in 20 uL in strip tubes 
- [ ] Add 130 uL of Lightning Conversion Reagent to each tube and mix well by pipetting
- [ ] Centrifuge briefly 
- [ ] Run thermocycler program (lid temp 105°C):
  - <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_P1.png?raw=true">
- [ ] Store at 4°C for <20 hours (overnight)

### Section 1, continued

- [ ] Prepare buffers, if needed (see above)
- [ ] Prepare and label Zymo-SpinTM IC Columns in collection tubes and one 1.5 mL tube per sample
- [ ] Add 600 uL of M-Binding Buffer to each column
- [ ] Add the entire bisulfite-converted sample to column and invert several times to mix 
- [ ] Centrifuge at 16,000 g for 30 seconds + discard flow through 
- [ ] Add 100 uL M-Wash Buffer 
- [ ] Centrifuge at 16,000 g for 30 seconds + discard flow through 
- [ ] Add 200 uL L-Desulphonation Buffer to column and incubate at room temperature for 15 minutes 
  - [ ] Do not exceed 20 minutes.
  - [ ] Near end of incubation, **heat DNA Elution buffer to 56°C on thermoblock** 
- [ ] After 15 min, centrifuge at 16,000 g for 30 seconds + discard flow through
- [ ] Add 200 uL of M-Wash Buffer 
- [ ] Centrifuge at 16,000 g for 30 seconds + discard flow through 
- [ ] Repeat the wash step above 
- [ ] Move spin columns into their respective 1.5 mL tubes 
- [ ] Add 19 uL of warmed DNA Elution buffer to column
  - [ ] Sequential elutions of smaller volumes ≥ 6 μL (e.g., 9.5 μL x 2 for 19 μL total) can help ensure complete elution of all DNA from the column.
- [ ] Incubate at room temperature for **3** minutes (1-5 minutes)
- [ ] Centrifuge at 16,000 g for 30 seconds to elute bisulfite-converted DNA
- [ ] Check if all tubes have same volume (greater elution volume may cause library prep failure)
- [ ] Toss spin columns and keep 1.5 mL tubes on ice 

***This is a safe stopping point. Bisulfite-converted DNA can be safely stored at ≤ −20°C for up to one month.***

### Section 2: Adapter Ligation

- [ ] Thaw the following reagents on ice 
	- [ ] Adapter Ligation Buffer 1
	- [ ] Adapter Ligation Buffer 2
	- [ ] Adapter Ligation Buffer 3
	- [ ] **Buffers 2 & 3 should only be thawed 4 times maximum -- make aliquots upon first thawing**
- [ ] Thaw **Adapter Ligation Master Mix** to room temperature. Once thawed, vortex for at least 30 seconds and invert to mix well.
  - [ ] **This master Mix should only be thawed 4 times maximum -- make aliquots upon first thawing**
- [ ] Preheat two thermocyclers:
  - [ ] One to 98°C (lid temp 105°C)
  - [ ] One to 37°C (lid temp 45°C)
  - *Note: If only a single thermal cycler is available, set to 98°C (lid temp 105°C) initially and change the temperature to 37°C (lid temp 45°C) during the 2-minute return to ice incubation (Step 6). Leave the lid open to help cool.*
- [ ] On ice, add 18 uL of bisulfite converted sample to new PCR tubes 
- [ ] Add 2 uL of Adapter Ligation Buffer 1 to each tube 
- [ ] Vortex and centrifuge briefly
- [ ] **Incubate on ice for 2 minutes**
- [ ] Heat shock by immediately placing the tube at **98°C (lid temp 105°C) for 3 minutes**.
- [ ] Immediately return the tube to ice and incubate for at least **2 minutes on ice** to fully denature the DNA.
  - *If using only one thermal cycler, set the temperature to 37°C (lid temp 45°C) during this incubation so that the temperature is ready by Step 10. Leave the lid open to help cool it faster.*
- [ ] Thoroughly mix the Adapter Ligation Master Mix tube by vortexing for at least 30 seconds and inverting several times.
  - The Adapter Ligation Master Mix is **very viscous**. Mix well after thawing and **right before use**.
- [ ] Add the following on ice in the order defined below to the tube:
  - Denatured DNA: 20 μL (already in tube)
  - [ ] Adapter Ligation Buffer 2: 2 μL
  - [ ] Adapter Ligation Buffer 3: 2 μL
  - [ ] Adapter Ligation Master Mix: 26 μL
  - *Total Volume: 50 μL*
- [ ] Mix entire reaction thoroughly by **pipetting up and down 20-25 times**, **vortexing**, and **inverting** to ensure complete homogenization. Centrifuge ***very briefly*** to ensure there are no droplets in the cap or on the sides of the tube.
  - *vortexing and inversion is recommended for complete homogenization*
- [ ] Incubate the tube at **37°C (lid temp 45°C)** for **1 hour** in a thermal cycler.
  - *If using only one thermal cycler, ensure that the temperature has reached 37°C (lid temp 45°C) before starting the incubation. If it is still cooling down, **leave the samples on ice** until the thermal cycler is ready.*
- [ ] Equilibriate Select-a-Size MagBeads to equilibrate to room temperature for 30 minutes prior to use
- [ ] After the 1-hour adapter ligation reaction, add 85 μL (*60 μL* for non-FFPE) of **DNA Elution Buffer** to the sample to bring the volume up to 135 (*110*) μL
  - [ ] *mix well by pipetting*
- [ ] Follow the clean-up protocol in **Appendix A**, using 50 μL of *Select-a-Size MagBeads* (60 μL for non-FFPE).
  - [ ] For elution, resuspend the beads in 30 μL (*15 μL* for non-FFPE) of DNA Elution Buffer and aspirate all 15 μL eluate after separation from the beads into a new tube.

### Appendix A: Select-a-Size MagBead Clean-Up Protocol
Before Starting:
- [ ] Ensure that the indicated volume of ethanol has been added to the **DNA Wash Buffer**.
- [ ] Allow the **Select-a-Size MagBeads** to equilibrate to room temperature for **30 minutes** prior to use.
- [ ] **Resuspend** the magnetic particles immediately before use by vortexing the Select-a-Size MagBeads until homogenous.

1. Add 60 μL of the **Select-a-Size MagBeads** to the tube. Mix thoroughly by pipetting until homogenous and incubate for 5−10 minutes at room temperature.
2. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
3. Carefully remove the supernatant without disturbing the magnetized bead pellet.
   1. Avoid aspirating any beads when removing the supernatant.
4. Without removing from the magnetic stand, add 200 μL of **DNA Wash Buffer** to the tube, incubate for at least 30 seconds, and then remove the supernatant completely without disturbing the magnetized bead pellet. _**Repeat this wash step**_ for two washes total.
5. Remove the tube from the magnetic stand and centrifuge very briefly. Then return the tube to the magnetic stand, wait for the beads to pellet, and remove any residual **DNA Wash Buffer** with a 10 μL pipette tip.
6. Leave the tube on the magnetic stand and keep the cap open for 2−3 minutes to allow the beads to air dry.
   1. Do not over dry the beads as this may negatively impact recovery. Beads should remain a glossy brown color.
   2. When performing the clean-up in **Section 2: Adapter Ligation**, the beads are more likely to disperse around the tube and are more susceptible to drying faster than normal.
7. Cap and remove the tube from the magnetic stand. Add the indicated volume of **DNA Elution Buffer** and fully resuspend the beads by pipetting up and down. Incubate for 5 minutes at room temperature.
   1. *When performing the clean-up in Section 2: Adapter Ligation, the resuspended beads behave differently and will be more challenging to remove from the sides of the tube. Briefly centrifuge tubes if necessary. Take care to ensure the beads are still fully resuspended.*
   2. If performing clean-up in **Section 2: Adapter Ligation**, add 15 μL of **DNA Elution Buffer** to fully resuspend the beads.
8. Place the tube back on the magnetic stand for 2 minutes or until the supernatant is clear.
9.  Transfer the indicated volume of eluate to a new tube. Discard the beads.
   1.  If performing clean-up in **Section 2: Adapter Ligation**, aspirate all 15 μL eluate and transfer to a 0.2 mL PCR tube.

***This is a safe stopping point. The purified adapter-ligated DNA can be safely stored at ≤ −20°C for up to one month.***

### Section 3: Index PCR Amplification

- [ ] Combine the following on ice to a 0.2 mL PCR tube containing the purified adapter-ligated DNA:
  - [ ] Adapter-Ligated DNA: 15 μL
  - [ ] Zymo-SeqTM UDI Index Primers: 10 μL
  - [ ] 2X Index PCR Premix: 25 μL
  - *Total Volume: 50 μL*
- [ ] Mix entire reaction thoroughly by pipetting or gently vortexing then briefly centrifuge.
- [ ] If performing the clean-up same-day, equilibrate to room temperature for 30 minutes prior to use
- [ ] Perform the following steps in a thermal cycler (lid temp 105°C):
  - <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_P2.png?raw=true">
  - The recommended number of PCR cycles may be increased to the following depending on the FFPE DNA sample input amount and type used:
    - <img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_cycles.png?raw=true">

***This is a safe stopping point. Amplified DNA samples can be safely stored overnight at 4°C. Otherwise, continue directly to Step 4 on the next page.***

- [ ] Follow the clean-up protocol in **Appendix A** using 40 μL of *Select-a-Size MagBeads* (60 μL for non-FFPE)
  - [ ] For elution, resuspend the beads in 20 μL of DNA Elution Buffer and aspirate all 20 μL eluate after separation from the beads.

### Appendix A: Select-a-Size MagBead Clean-Up Protocol
Before Starting:
- [ ] Ensure that the indicated volume of ethanol has been added to the **DNA Wash Buffer**.
- [ ] Allow the **Select-a-Size MagBeads** to equilibrate to room temperature for **30 minutes** prior to use.
- [ ] **Resuspend** the magnetic particles immediately before use by vortexing the Select-a-Size MagBeads until homogenous.

1. Add 60 μL of the **Select-a-Size MagBeads** to the tube. Mix thoroughly by pipetting until homogenous and incubate for 5−10 minutes at room temperature.
2. Place the tube on a magnetic stand for 3 minutes, or until the supernatant is clear.
3. Carefully remove the supernatant without disturbing the magnetized bead pellet.
   1. Avoid aspirating any beads when removing the supernatant.
4. Without removing from the magnetic stand, add 200 μL of **DNA Wash Buffer** to the tube, incubate for at least 30 seconds, and then remove the supernatant completely without disturbing the magnetized bead pellet. _**Repeat this wash step**_ for two washes total.
5. Remove the tube from the magnetic stand and centrifuge very briefly. Then return the tube to the magnetic stand, wait for the beads to pellet, and remove any residual **DNA Wash Buffer** with a 10 μL pipette tip.
6. Leave the tube on the magnetic stand and keep the cap open for 2−3 minutes to allow the beads to air dry.
   1. Do not over dry the beads as this may negatively impact recovery. Beads should remain a glossy brown color.
7. Cap and remove the tube from the magnetic stand. Add the indicated volume of **DNA Elution Buffer** and fully resuspend the beads by pipetting up and down. Incubate for 5 minutes at room temperature.
   1. If performing clean-up in **Section 3: Index PCR Amplification**, add 20 μL of **DNA Elution Buffer** to fully resuspend the beads.
8. Place the tube back on the magnetic stand for 2 minutes or until the supernatant is clear.
9.  Transfer the indicated volume of eluate to a new tube. Discard the beads.
   1.  If performing clean-up in **Section 3: Index PCR Amplification**, aspirate all 20 μL eluate and transfer to a new 1.5 mL microcentrifuge tube.

THIS IS THE FINAL WGBS LIBRARY. **DNA libraries can be safely stored at ≤ −20°C for months.**

### QC

Run to visualize libraries. Here's an example of what the library should look like on a Tapestation: 

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_QC.png?raw=true" height="500">

"If adapter dimers are present, they will form an approximately 130-180 bp band. Yields will vary depending on the total quantity and quality of sample input DNA.