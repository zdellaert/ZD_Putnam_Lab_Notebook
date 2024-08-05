---
layout: post
title: Testing NEBNext Low Input RNA Library Prep
date: '2024-08-01 17:00:00'
categories: Protocols
tags: [RNA, Pocillopora, Porites, LCM, Library Prep]
---

## Testing NEBNext Low Input RNA Library Prep

Product: [NEBNext® Single Cell/Low Input RNA Library Prep Kit for Illumina](https://www.neb.com/en-us/products/e6420-nebnext-single-cell-low-input-rna-library-prep-kit-for-illumina)

Protocol: [Link here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manualE6420_NEBNext_Low_Input_RNA_Library_Prep.pdf). Most of the text here is taken directly from this protocol. I will only be using (and detailing the steps below) for one of the workflows in this protocol: "**Section 2: Protocol for Low Input RNA: cDNA Synthesis, Amplification and Library Generation**". 

I have a sample kit of 6 preps.

### Overview image of workflow:

![E6420_NEBNextSingleCell_kit_workflow.png](https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/master/images/protocols/E6420_NEBNextSingleCell_kit_workflow.png)

### Materials 

- [NEBNext® Single Cell/Low Input RNA Library Prep Kit for Illumina](https://www.neb.com/en-us/products/e6420-nebnext-single-cell-low-input-rna-library-prep-kit-for-illumina)
  - **Store entire kit at -20 ºC**
    - except NEBNext Cell Lysis Buffer, which, once prepared, should be stored at 4 ºC
- DNase RNase free PCR strip tubes (USA Scientific 1402-1708)
- 80% Ethanol (freshly prepared)
- Nuclease-free water
- DNA LoBind Tubes (Eppendorf® #022431021)
- Magnetic rack or plate (e.g., [NEBNext® Magnetic Separation Rack](https://www.neb.com/en-us/products/s1515-nebnext-magnetic-separation-rack) or equivalent)
- Thermocycler
- Vortex
- Microcentrifuge
- SPRIselect Reagent Kit (Beckman Coulter®, Inc. #B23317) or AMPure® XP Beads (Beckman Coulter, Inc. #A63881)
  - we only have KAPA Pure beads
  - Based on some research the recommended ratios seem really similar
- Agilent® Bioanalyzer® or similar fragment analyzer and associated consumables
  - I will be using an Agilent Tapestation instead
- [NEBNext Oligos](https://www.neb.com/en-us/products/next-generation-sequencing-library-preparation/multiplex-oligos-adaptors-and-primers/multiplex-oligos-adaptors-and-primers)
  - See also: [Can I use this NEBNext kit with adaptors and primers from other vendors than NEB?](https://www.neb.com/en-us/faqs/2019/03/08/can-i-use-this-nebnext-kit-with-adaptors-and-primers-from-other-vendors-than-neb)

#### Kit contents

*All reagents should be stored at –20°C*. Colored bullets indicate the cap color of the reagent to be added to a reaction. 

- ⚪️ *Murine RNase Inhibitor* (not used in the RNA-input kit)
- ⚪️ NEBNext Cell Lysis Buffer (once prepared, store at 4 ºC)
- 🟣 NEBNext Single Cell RT Primer Mix
- 🟣 NEBNext Single Cell RT Buffer
- 🟣 NEBNext Template Switching Oligo
- 🟣 NEBNext Single Cell RT Enzyme Mix
- 🟠 (or ⚪️) NEBNext Single Cell cDNA PCR Master Mix
- 🟠 NEBNext Single Cell cDNA PCR Primer
- 🟡 NEBNext Ultra II FS Enzyme Mix
- 🟡 NEBNext Ultra II FS Reaction Buffer
- 🔴 NEBNext Ultra II Ligation Master Mix
- 🔴 NEBNext Ligation Enhancer
- 🔵 NEBNext Ultra II Q5® Master Mix
- ⚪️ NEBNext Bead Reconstitution Buffer
- ⚪️ NEBNext Adaptor Dilution Buffer
- ⚪️ TE Buffer
- ⚪️ Nuclease-free Water

### Best practices (thanks, [Jill](https://github.com/JillAshey/JillAshey_Putnam_Lab_Notebook/blob/master/_posts/2024-06-13-Zymo-Pico-Methyl-Seq-Library-Prep.md))

- Preset the thermocycler programs 
- Thaw and keep all components on ice unless instructed otherwise. Flick to mix (or vortex if indicated) and centrifuge before use
	- Avoid multiple freeze-thaws, make aliquots if needed
- Allow beads to equilibrate to room temperature >30 mins before use
- Resuspend beads immediately before each use by gently inverting until homogenous

## Protocol for Low Input RNA: cDNA Synthesis, Amplification and Library Generation

### Sample Recommendations

- The RNA sample should be free of salts (e.g., Mg2+, or guanidinium salts), divalent cation chelating agents (e.g. EDTA, EGTA, citrate), or organics (e.g., phenol and ethanol). If an excess amount of genomic DNA is present in RNA samples, an optional DNase I treatment could be performed. Inactivate/remove DNase I after treatment.
- Assess quality of the input RNA by running input RNA on an Agilent Bioanalyzer to determine the RNA Integrity Number (RIN).
- **Starting Material**: 2 pg–200 ng poly(A) tail-containing total RNA (DNA free), RIN score ≥ 8.0.
  - Our RNA is definitely not RIN score > 8.0, but we will see what we can do.

### 2.1 Sample and Reagent preperation

#### If doing in 1 day:

- [ ] Prepare fresh 80% Ethanol with nucelase-free water
- [ ] Thaw total RNA on ice prior to starting the protocol
- [ ] The **⚪️ Murine RNase Inhibitor** is not needed for this protocol, so it should be kept at -20 ºC
- [ ] Briefly centrifuge the tubes containing 🟣 **NEBNext Single Cell RT Enzyme Mix** to collect solutions to the bottom of the tubes, then **place on ice**.
- [ ] Thaw all other frozen components at **room temperature**
  - if the ⚪️ 10X NEBNext Cell Lysis Buffer appears cloudy after thawing, incubate briefly at 37°C to clear up the solution.
- [ ] Mix each component thoroughly, centrifuge briefly to collect solutions to the bottom of the tube, and **then place on ice**.
- [ ] Leave the NEBNext Cell Lysis Buffer bottle at 4°C or at room temperature for storage.

#### If doing in 2 days:

1. Day 1 (Annealing, RT, cDNA PCR, cleanup, cDNA QC):
   - [ ] Prepare fresh 80% Ethanol with nucelase-free water
   - [ ] Thaw total RNA on ice prior to starting the protocol
   - [ ] Briefly centrifuge the tubes containing 🟣 **NEBNext Single Cell RT Enzyme Mix** to collect solutions to the bottom of the tubes, then **place on ice**.
   - [ ] Thaw the following frozen components at **room temperature**
     - [ ] ⚪️ NEBNext Cell Lysis Buffer (once prepared, store at 4 ºC)
       - [ ] if the ⚪️ 10X NEBNext Cell Lysis Buffer appears cloudy after thawing, incubate briefly at 37°C to clear up the solution.
     - [ ] 🟣 NEBNext Single Cell RT Primer Mix
     - [ ] 🟣 NEBNext Single Cell RT Buffer
     - [ ] 🟣 NEBNext Template Switching Oligo
     - [ ] 🟠 (or ⚪️) NEBNext Single Cell cDNA PCR Master Mix
     - [ ] 🟠 NEBNext Single Cell cDNA PCR Primer
     - [ ] ⚪️ NEBNext Bead Reconstitution Buffer
     - [ ] ⚪️ TE Buffer
     - [ ] ⚪️ Nuclease-free Water
   - [ ] Mix each component thoroughly, centrifuge briefly to collect solutions to the bottom of the tube, and **then place on ice**.
   - [ ] Leave the NEBNext Cell Lysis Buffer bottle at 4°C or at room temperature for storage.

2. Day 2 (Fragmentation/End Prep, Adaptor Ligation, Cleanup of Adaptor-ligated DNA, PCR enrichment, cleanup, and final library QC):
   - [ ] Prepare fresh 80% Ethanol with nucelase-free water
   - [ ] Thaw the following frozen components at **room temperature**
     - [ ] 🟡 NEBNext Ultra II FS Enzyme Mix
     - [ ] 🟡 NEBNext Ultra II FS Reaction Buffer
     - [ ] 🔴 NEBNext Ultra II Ligation Master Mix
     - [ ] 🔴 NEBNext Ligation Enhancer
     - [ ] 🔵 NEBNext Ultra II Q5® Master Mix
     - [ ] ⚪️ NEBNext Adaptor Dilution Buffer
     - [ ] ⚪️ TE Buffer
     - [ ] ⚪️ Nuclease-free Water
   - [ ] Mix each component thoroughly, centrifuge briefly to collect solutions to the bottom of the tube, and **then place on ice**.

## Day 1

### 2.2. Primer Annealing for First Strand Synthesis

**Note, this is for each RNA sample individually in an individual PCR tube**

- [ ] 2.2.1. To anneal cDNA Primer with total RNA samples, prepare the reaction as follows (on ice):

- for an input of 4.99 ng RNA, at 8µl volume, the sample would have a minimum concentration of 0.62 ng/µl
  - Most of our high quality RNA is below this concentration, so we will use the < 5 ng mixture
  - for a low-concentration sample (like LCM RNA), of lets say, 0.280 ng/µl, 8 µl of input would be 2.24 ng. So we would put in 8 µl of the thawed RNA and use the < 5 ng mixture.
- if you have > 7 µl of an RNA of concentration greater than 0.714 ng/µl (5 ng / 7 µl), you should use the ≥ 5 ng RNA workflow.

| COMPONENT               | *< 5 ng RNA*: VOLUME (µl) | *≥ 5 ng RNA*: VOLUME (µl) |
|----------------------------------|------------------------|------------------------|
| Total RNA                        | Up to 8 µl             | Up to 7 µl             |
| 🟣 NEBNext Single Cell RT Primer | 1 µl                    | 2 µl                  |
| Nuclease-free Water              | Variable               | Variable               |
| Total Volume                     | 9 µl                   |  9 µl                  |

- [ ] 2.2.2. Mix well by pipetting up and down gently at least 10 times, then centrifuge briefly to collect solution to the bottom of the tubes.
- [ ] 2.2.3. Incubate for 5 minutes at 70°C in a thermal cycler with the heated lid set to 105°C, then hold at 4ºC until next step.

During the above annealing step, prepare the components for the following step.

### 2.3. Reverse Transcription (RT) and Template Switching

- [ ] 2.3.1. Vortex the NEBNext Single Cell RT Buffer briefly
  - **Note: It is important to vortex the buffer prior to use for optimal performance** (they even have a [video about this](https://www.neb.com/en-us/tools-and-resources/video-library/quick-tips---vortexing-the-nebnext-single-cell-low-input-rna-library-prep-kit-rt-buffer))
- [ ] Then, prepare the RT mix in a separate tube as follows (adding NEBNext Single Cell RT Enzyme Mix last)
  
| COMPONENT                              | VOLUME (µl) PER REACTION |
|----------------------------------------|--------------------------|
| 🟣 NEBNext Single Cell RT Buffer (VORTEXED) |       5 µl          |
| 🟣 NEBNext Template Switching Oligo    |       1 µl               |
| 🟣 NEBNext Single Cell RT Enzyme Mix  |       2 µl               |
| Nuclease-free Water                    |       3 µl               |
| | |
| **Total Volume**                      | 11 µl                    |

- [ ] 2.3.2. Mix thoroughly by pipetting up and down several times, then centrifuge briefly to collect solutions to the bottom of tubes.
- [ ] 2.3.3. Combine 11 μl of the RT mix (above) with 9 μl of the annealed sample (Step 2.2.3.). 
- [ ] Mix well by pipetting up and down at least 10 times and centrifuge briefly.
- [ ] 2.3.4. Incubate the reaction mix in a thermal cycler with the following steps and the heated lid set to 105°C:
  - 90 minutes at 42°C
  - 10 minutes at 70°C
  - Hold at 4°C

### 🛑 Safe Stopping Point: Samples can be safely stored overnight at 4°C or –20°C.

--- 

### 2.4. cDNA Amplification by PCR

- [ ] 2.4.1. Prepare cDNA amplification mix as follows:
  - [ ] ⚪️ NEBNext Cell Lysis Buffer (10X) needs to be homogenous with no precipitates (should be clear, if not, warm to 37 ºC). [Vortex thoroughly and spin down before adding.](https://www.neb.com/en-us/tools-and-resources/video-library/quick-tip-adding-the-lysis-buffer-for-the-pcr-in-the-nebnext-rna-workflow)

| COMPONENT                              | VOLUME (µl) PER REACTION |
|----------------------------------------|--------------------------|
| 🟠 (or ⚪️) NEBNext Single Cell cDNA PCR Master Mix |        50 µl  |
| 🟠 NEBNext Single Cell cDNA PCR Primer | 2 µl                      |
| ⚪️ NEBNext Cell Lysis Buffer (10X)     | 0.5 µl                    |
| Nuclease-free Water                    | 27.5 µl                  |
|   | |
| **Total Volume**                       | 80 µl                     |

- [ ] 2.4.2. Add 80 µl cDNA amplification mix to 20 µl of the sample from Step 2.3.4.
- [ ] Mix by pipetting up and down at least 10 times.
- [ ] 2.4.3. Incubate the reaction in a thermal cycler with the following PCR cycling conditions and the heated lid set to 105°C:

| CYCLE STEP           | TEMP  | TIME       | CYCLES | 
|----------------------|-------|------------|--------|
| Initial Denaturation | 98°C  | 45 seconds | 1      |
|   | | | 
| Denaturation         | 98°C  | 10 seconds | 7–21 depending on RNA input (see manual) |
| Annealing            | 62°C  | 15 seconds |^        |
| Extension            | 72°C  | 3 minutes  |^       |
|   | | | 
| Final Extension      | 72°C  | 5 minutes  | 1       |
| Hold                 | 4°C   | ∞          |         |

This step should take about an hour depending on # of cycles.

For 1-10 ng of RNA, they recommend 10-11 cycles.

**Based on looking at other Putnam lab Library Prep protocols, we almost always have to increase the number of cycles for our input. And mine is extra degraded. I will increase cycles to 15.**

For the various inputs listed above, the recommended PCR cycles will typically result in cDNA yields between 1–20 ng (in most cases 5–15 ng). We recommend quantifying cDNA after the cleanup (Step 2.5) before proceeding to the library preparation (Sections 2.7–2.12). 

### 🛑 Safe Stopping Point: Samples can be safely stored overnight at 4°C or –20°C.

--- 

### 2.5. Cleanup of Amplified cDNA

#### This should be done at post-PCR bench

- [ ] 2.5.1. Allow the ⚪️ [NEBNext Bead Reconstitution Buffer](https://www.neb.com/en-us/tools-and-resources/video-library/quick-tips---bead-reconstitution-buffer-for-nebnext-single-cell-low-input-rna-library-prep) and the SPRI® beads (if stored at 4°C) to warm to room temperature for at least 30 minutes before use.
  - [ ] Vortex SPRI Beads to resuspend well
  - [ ] Prepare fresh 80% ethanol
    - 800 uL per sample
  - [ ] Prepare 0.1X TE (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water)
    - 50 uL per sample
- [ ] 2.5.2. Add 60 μl (0.6X of sample volume) resuspended beads to the PCR reaction.
  - [ ] Mix well by pipetting up and down at least 10 times.
  - [ ] Be careful to expel all of the liquid out of the tip during the last mix
- [ ] 2.5.3. Incubate samples on the bench top for at least **5 minutes at room temperature**.
- [ ] 2.5.4. Place the tube/plate on an appropriate magnetic stand to separate the beads from the supernatant. If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells before placing on the magnetic stand.
- [ ] 2.5.5. After **5 minutes** (or when the solution is clear), carefully remove and **discard the supernatant**. Be careful not to disturb the beads that contain cDNA (**Caution: do not discard the beads**).
- [ ] 2.5.6. Add **200 μl of 80% freshly prepared ethanol** to the tube/plate while in the magnetic stand. Incubate at room temperature for 30 seconds, and then carefully remove and discard the supernatant. Be careful not to disturb the beads that contain cDNA.
- [ ] 2.5.7. Repeat Step 2.5.6. once for a total of **two washes**. Be sure to remove all visible liquid after the second wash. If necessary, briefly spin the tube/plate, place back on the magnet and **remove traces of ethanol with a p10 pipette tip**.
- [ ] 2.5.8. Air dry the beads for *up to 5 minutes* while the tube/plate is on the magnetic stand with the lid open.
  - **Caution: Do not over-dry the beads.** This may result in lower recovery of cDNA. Elute the samples when the beads are **still dark brown and glossy looking**, but when all visible liquid has evaporated. When the beads turn lighter brown and start to crack, they are too dry.
- [ ] 2.5.9. Remove the tube/plate from the magnetic stand.
  - [ ] Elute the cDNA from the beads by adding 50 μl of 0.1X TE (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water).
- [ ] 2.5.10. Mix well by pipetting up and down 10 times, or on a vortex mixer. Incubate for at least **2 minutes at room temperature**.
  - [ ] If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells.
- [ ] 2.5.11. Add 45 μl of (room temperature) ⚪️ NEBNext Bead Reconstitution Buffer to the eluted cDNA + bead mixture from Step 2.5.10 for a second sample clean up.
  - [ ] Mix well by pipetting up and down at least 10 times
- [ ] 2.5.12. Incubate samples on the bench top for at least **5 minutes at room temperature**.
- [ ] 2.5.13. Place the tube/plate on an appropriate magnetic stand to separate the beads from the supernatant. If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells before placing on the magnetic stand.
- [ ] 2.5.14. After **5 minutes** (or when the solution is clear), carefully remove and discard the supernatant. Be careful not to disturb the beads that contain cDNA (**Caution: do not discard the beads**).
- [ ] 2.5.15. Add **200 μl of 80% freshly prepared ethanol** to the tube/plate while in the magnetic stand. Incubate at room temperature for 30 seconds, and then carefully remove and discard the supernatant. Be careful not to disturb the beads that contain cDNA.
- [ ] 2.5.16. Repeat Step 2.5.15 once for a total of **two washes**. Be sure to remove all visible liquid after the second wash. If necessary, briefly spin the tube/plate, place back on the magnet and **remove traces of ethanol**.
- [ ] 2.5.17. Air dry the beads for *up to 5 minutes* while the tube/plate is on the magnetic stand with the lid open.
  - **Caution: Do not over-dry the beads.** This may result in lower recovery of cDNA. Elute the samples when the beads are **still dark brown and glossy looking**, but when all visible liquid has evaporated. When the beads turn lighter brown and start to crack, they are too dry.
- [ ] 2.5.18. Remove the tube/plate from the magnetic stand.
  - [ ] Elute the cDNA from the beads by adding 33 μl of ⚪️ 1X TE (provided in kit).
- [ ] 2.5.19. Mix well by pipetting up and down 10 times, or on a vortex mixer. Incubate for **at least 2 minutes at room temperature**.
  - If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells before placing back on the magnetic stand.

**NOW WE KEEP SUPERNATANT**

- [ ] 2.5.20. Place the tube/plate on the magnetic stand. After 5 minutes (or when the solution is clear), **transfer 30 μl to a new PCR tube**. 

### 2.6. Assess Amplified cDNA Quality and Quantity on a Bioanalyzer

- [ ] 2.6.1. Run 1 µl of amplified cDNA from Step 2.5.20 on a DNA High Sensitivity Chip.
  - I will use DNA tapestation instead
  - 1 ng–20 ng cDNA yield is typical yield, with [broad peak around 2000 bp](https://www.neb.com/en-us/tools-and-resources/video-library/quick-tips---bead-reconstitution-buffer-for-nebnext-single-cell-low-input-rna-library-prep)
- See manual for recommendations based on QC results.
  - While 1 ng–20 ng cDNA yield is typical, 100 pg–20 ng purified cDNA can be used in the library construction protocol (Sections 2.7–2.12). If using cDNA outside the range of 1 ng–20 ng (as determined in Step 2.6), adjust the PCR cycles to amplify the adaptor ligated DNA. For details, see Step 2.10 in this protocol.
  - **If the cDNA yield is variable, the samples can be normalized to the same concentration prior to Step 2.7 in order to treat all of the samples with the same number of PCR cycles**.

### 🛑 Safe Stopping Point: Samples can be safely stored overnight at 4°C or –20°C.

--- 

## Day 2

### 2.7. Fragmentation/End Prep

- [ ] 2.7.1. Ensure that the 🟡 NEBNext Ultra II FS Reaction Buffer is completely thawed. If a precipitate is seen in the buffer, pipette up and down several times to break it up, and quickly vortex to mix. Place on ice until use.
- [ ] 2.7.2. Vortex the 🟡 NEBNext Ultra II FS Enzyme Mix 5–8 seconds prior to use and place on ice.
- [ ] 2.7.3. Add the following components to a 0.2 ml thin wall PCR tube on ice:

| COMPONENT              | VOLUME (µl) PER REACTION |
|------------------------|--------------------------|
| cDNA (Step 2.5.20)     |  26 µl                   |          
| 🟡 NEBNext Ultra II FS Reaction Buffer | 7 µl     |
| 🟡 NEBNext Ultra II FS Enzyme Mix |  2 µl     |
|   |   |
|Total Volume  | 35 µl                  |   

- [ ] 2.7.4. Vortex the reaction for 5 seconds and briefly spin in a microcentrifuge. 
- [ ] 2.7.5. In a thermal cycler, with the heated lid set to 75°C, run the following program:
  - 25 minutes at 37°C
  - 30 minutes at 65°C
  - Hold at 4°C

**If necessary, can stop here and put at -20ºC, but you should keep going with Adaptor Ligation if possible**

### 2.8. Adaptor Ligation

- [ ] From the **NEB Oligo Kit**, thaw adaptor for illumina NEBNext Adaptor for Illumina and USER® Enzyme
- [ ] 2.8.1. Dilute NEBNext Adaptor for Illumina by 25-fold (0.6 µM) in the NEBNext ⚪️ Adaptor Dilution Buffer.
- [ ] 2.8.2. Mix the 🔴 NEBNext Ultra II Ligation Master Mix by pipetting up and down several times.
- [ ] 2.8.3. Add the following components directly to the FS Reaction Mixture on ice:

**Note: Do not mix these components ahead of time. Add straight to strip tube (that just came out of thermocycler) on ice.** Caution: NEBNext Ultra II Ligation Master Mix is very viscous, pipette with care.

| COMPONENT              | VOLUME (µl) PER REACTION |
|------------------------|--------------------------|
| FS Reaction Mixture (Step 2.7.5)  | 35 µl         |
| 🔴 NEBNext Ultra II Ligation Master Mix  | 30 µl   |
| 🔴 NEBNext Ligation Enhancer            | 1 µl    |
| 🔴 NEBNext Adaptor for Illumina ***(diluted 1:25)*** | 2.5 µl |
|  |  | 
| Total Volume |  68.5 µl | 

- [ ] 2.8.4. Set a 100 μl or 200 μl pipette to 50 μl and then pipette the entire volume up and down at least **10 times to mix thoroughly**.
  - [ ] Perform a quick spin to collect all liquid from the sides of the tube. (Caution: The NEBNext Ultra II Ligation Master Mix is very **viscous**. Care should be taken to ensure adequate mixing of the ligation reaction, as incomplete mixing will result in reduced ligation efficiency. The presence of a small amount of bubbles will not interfere with performance).

- [ ] 2.8.5. Incubate at 20°C for 15 minutes in a thermal cycler with the heated lid off.
- [ ] 2.8.6. Add 3 μl of 🔴 USER® Enzyme to the ligation mixture from Step 2.8.5.
- [ ] 2.8.7. Mix well and incubate at 37°C for 15 minutes with the heated lid set to ≥ 47°C. 

### 🛑 Safe Stopping Point: Samples can be safely stored overnight at 4°C or –20°C.

--- 

### 2.9. Cleanup of Adaptor-ligated DNA

- [ ] 2.9.1. If stored at 4°C allow the SPRI beads to warm to room temperature for at least 30 minutes before use.
  - [ ] Vortex SPRI beads to resuspend well
  - [ ] Prepare fresh 80% ethanol
    - 400 uL per sample
  - [ ] Prepare 0.1X TE (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water)
    - 17 uL per sample
- [ ] 2.9.2. Add 57 μl (0.8X of sample volume) resuspended beads to the PCR reaction.
  - [ ] Mix well by pipetting up and down at least 10 times.
  - [ ] Be careful to expel all of the liquid out of the tip during the last mix.
- [ ] 2.9.3. Incubate samples on the bench top for at least **5 minutes at room temperature**.
- [ ] 2.9.4. Place the tube/plate on an appropriate magnetic stand to separate the beads from the supernatant. If necessary, quickly spin
the sample to collect the liquid from the sides of the tube or plate wells before placing on the magnetic stand.
- [ ] 2.9.5. After **5 minutes** (or when the solution is clear), carefully remove and **discard the supernatant**. Be careful not to disturb the beads that contain DNA targets (**Caution: do not discard the beads**).
- [ ] 2.9.6. Add **200 μl of 80% freshly prepared ethanol** to the tube/ plate while in the magnetic stand. Incubate at room temperature for
30 seconds, and then carefully remove and discard the supernatant. Be careful not to disturb the beads that contain DNA targets.
- [ ] 2.9.7. Repeat Step 2.9.6 once for a total of **two washes**. Be sure to remove all visible liquid after the second wash. If necessary, briefly spin the tube/plate, place back on the magnet and **remove traces of ethanol with a p10 pipette tip**.
- [ ] 2.9.8. Air dry the beads for *up to 5 minutes* while the tube/plate is on the magnetic stand with the lid open.
  - **Caution: Do not over-dry the beads.** This may result in lower recovery of DNA. Elute the samples when the beads are **still dark brown and glossy looking**, but when all visible liquid has evaporated. When the beads turn lighter brown and start to crack, they are too dry.
- [ ] 2.9.9. Remove the tube/plate from the magnetic stand.
  - [ ] Elute the DNA target from the beads by adding 17 μl of 0.1X TE (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water).
- [ ] 2.9.10. Mix well by pipetting up and down 10 times, or on a vortex mixer. Incubate for at least **2 minutes at room temperature**.
  - [ ] If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells before placing back on the magnetic stand.

**NOW WE KEEP SUPERNATANT**

- [ ] 2.9.11. Place the tube/plate on the magnetic stand. After 5 minutes (or when the solution is clear), **transfer 15 μl to a new PCR tube**. Proceed to PCR Enrichment of Adaptor-ligated DNA in Section 2.10.

### 🛑 Safe Stopping Point: Samples can be safely stored overnight at 4°C or –20°C.

--- 

### 2.10. PCR Enrichment of Adaptor-ligated DNA

- [ ] From the **NEB Oligo Kit**, thaw i7 and i5 primers according to instructions
- [ ] 2.10.1. Combine the following components in a sterile tube:
  - Using Option A, since my NEBNext oligo kit has index primers **supplied in tubes**. These kits have the forward and reverse primers supplied in separate tubes. Primers are supplied at 10 µM each.

* *Refer to the corresponding NEBNext Oligo kit manual for determining valid barcode combinations.
* **Use only one i7 primer/ index primer per sample. Use only one i5 primer (or the universal primer for single index kits) per sample

| COMPONENT              | VOLUME (µl) PER REACTION    |
|------------------------|-----------------------------|
| Adaptor Ligated DNA Fragments (Step 2.9.11.) | 15 µl |
| 🔵 NEBNext Ultra II Q5® Master Mix |  25 µl           |
| 🔵 Index Primer/i7 Primer*,**  | 5 µl       |
| 🔵 Universal PCR Primer/i5 Primer*, ** | 5 µl       |
| | | 
| Total Volume            | 50 µl |

- [ ] 2.10.2. Set a 100 µl or 200 μl pipette to 40 μl and then pipette the entire volume up and down at least **10 times to mix thoroughly**.
  - [ ] Perform a quick spin to collect all liquid from the sides of the tube.
- [ ] 2.10.3. Place the tube on a thermal cycler and perform PCR amplification using the following PCR cycling conditions:

*If your cDNA input is outside the input range of 1 ng–20 ng, adjust the PCR cycle numbers accordingly. We recommend a minimum of 3 PCR cycles for all of the original molecules to make it into the final library. For cDNA yield of 100 pg we recommend testing 12 PCR cycles. For cDNA input of 1 ng–20 ng, the typical Illumina library yield, using 8 PCR cycles, is 100 ng–1 μg.*

| CYCLE STEP           | TEMP  | TIME       | CYCLES | 
|----------------------|-------|------------|--------|
| Initial Denaturation | 98°C  | 30 seconds | 1      |
|   | | | 
| Denaturation         | 98°C  | 10 seconds | 8 *dependent on cDNA input |
| Annealing/Extension   | 65°C  | 75 seconds |^        |
|   | | | 
| Final Extension      | 65°C  | 5 minutes  | 1       |
| Hold                 | 4°C   | ∞          |         |

### 2.11. Cleanup of PCR Reaction

- [ ] 2.11.1. If stored at 4°C allow the SPRI beads to warm to room temperature for at least 30 minutes before use.
  - [ ] Vortex SPRI beads to resuspend well
  - [ ] Prepare fresh 80% ethanol
    - 400 uL per sample
  - [ ] Prepare 0.1X TE (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water)
    - 33 uL per sample
- [ ] 2.11.2. Add 45 μl (0.9X of sample volume) resuspended beads to the PCR reaction.
  - [ ] Mix well by pipetting up and down at least 10 times.
  - [ ] Be careful to expel all of the liquid out of the tip during the last mix. 
- [ ] 2.11.3. Incubate samples on bench top for at least **5 minutes at room temperature**.
- [ ] 2.11.4. Place the tube/plate on an appropriate magnetic stand to separate the beads from the supernatant. If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells before placing on the magnetic stand.
- [ ] 2.11.5. After **5 minutes** (or when the solution is clear), carefully remove and **discard the supernatant**.
  - [ ] Be careful not to disturb the beads that contain DNA targets (**Caution: do not discard the beads**).
- [ ] 2.11.6. Add **200 μl of 80% freshly prepared ethanol** to the tube/ plate while in the magnetic stand. Incubate at room temperature for 30 seconds, and then carefully remove and discard the supernatant. Be careful not to disturb the beads that contain DNA targets.
- [ ] 2.11.7. Repeat Step 2.11.6 once for a total of **two washes**. Be sure to remove all visible liquid after the second wash. If necessary,
briefly spin the tube/plate, place back on the magnet and **remove traces of ethanol with a p10 pipette tip**.
- [ ] 2.11.8. Air dry the beads for *up to 5 minutes* while the tube/plate is on the magnetic stand with the lid open.
  - **Caution: Do not over-dry the beads**. This may result in lower recovery of DNA. Elute the samples when the beads are **still dark brown and glossy looking**, but when all visible liquid has evaporated. When the beads turn lighter brown and start to crack, they are too dry.
- [ ] 2.11.9. Remove the tube/plate from the magnetic stand.
  - [ ] Elute the DNA target from the beads by adding 33 μl of 0.1X TE (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water).
- [ ] 2.11.10. Mix well by pipetting up and down 10 times, or on a vortex mixer. Incubate for at least **2 minutes at room temperature**.
  - [ ] If necessary, quickly spin the sample to collect the liquid from the sides of the tube or plate wells before placing back on the magnetic stand.

**NOW WE KEEP SUPERNATANT**

- [ ] 2.11.11. Place the tube/plate on the magnetic stand. After 5 minutes (or when the solution is clear), **transfer 30 μl to a new PCR tube**.

#### Libraries can be stored at –20°C.

### 2.12. Assess Library Quality and Quantity on a Bioanalyzer
- [ ] 2.12.1. Dilute library (from Step 2.11.11) 5-fold in 0.1X TE Buffer (dilute ⚪️ 1X TE Buffer 1:10 in nuclease free water)
  - Mix 1 uL library with 4 uL 0.1X TE
  - inputs ≤ 1 ng may not require dilution to run on a Bioanalyzer.
- [ ] 2.12.2. Run 1 μl on a DNA High Sensitivity Chip.
  - I am going to try with tapestation
- [ ] 2.12.3. Check that the electropherogram shows a **narrow distribution with a peak size of 300–350 bp**.
  - Note: If a peak ~80 bp (primers) or 128-140 bp (adaptor-dimer) is visible in the Bioanalyzer trace, bring up the sample volume (from Step 2.11.11.) to 50 μl with 0.1X TE Buffer and repeat the cleanup of PCR Reaction as described in Section 2.11. You may see adaptor-dimer when starting with inputs ≤ 1 ng.

----

### Thermocycler programs to program:

- Primer Annealing (2.2.3):
  - 5 minutes at 70°C (with heated lid set to 105°C)
  - hold at 4ºC until next step
- RT (2.3.4):
  - 90 minutes at 42°C (with heated lid set to 105°C)
  - 10 minutes at 70°C (with heated lid set to 105°C)
  - Hold at 4°C
- cDNA Amplification (2.4.3):
  - 98°C, 45 seconds (with heated lid set to 105°C)
  - 7-21 cycles (likely 10-11?) of
    - 98°C, 10 seconds (with heated lid set to 105°C)
    - 62°C, 15 seconds (with heated lid set to 105°C)
    - 72°C, 3 minutes (with heated lid set to 105°C)
  - 72°C, 5 minutes (with heated lid set to 105°C)
  - Hold at 4°C
- Fragmentation (2.7.5):
  - 25 minutes at 37°C (with heated lid set to 75°C)
  - 30 minutes at 65°C (with heated lid set to 75°C)
  - Hold at 4°C
- Adaptor Ligation 1 (2.8.5):
  - 15 minutes at 20°C (no heated lid - set OFF)
- Adaptor Ligation 2 (2.8.7):
  - 15 minutes at 37°C (with heated lid set to ≥ 47°C)
- PCR Enrichment (2.10.3):
  - *no info about heated lid*
  - 98°C, 30 seconds
  - 8 cycles (*dept. on cDNA*) of
    - 98°C, 10 seconds
    - 65°C, 75 seconds
  - 65°C, 5 minutes
  - Hold at 4°C

---

## Samples: Starting library prep 7/30/24

Just going to start with two, and then will try again and see if I need to pool RNA or anything.

- POC:
  -  #7, [6/13 Zymo Extraction](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240613-RNA-Extractions-Zymo/)
     - 1.240 ng/uL
     - 7 ul * 1.24 ng/ul = 8.68 ng
       - Using > 5 ng protocol
- POR:
  - #7, [7/24 Zymo Extraction](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-20240718-RNA-DNA-Extractions-Zymo-Try-2/)
    - 0.280 ng/uL
    - 8 ul * 0.28 ng/ul = 2.24 ng
       - Using < 5 ng protocol

Just a coincidence that they are the same number.

Tapestation traces for each:

![2024-07-30-RNA-Input.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-30-RNA-Input.JPG?raw=true)

### cDNA QC, step 2.6

![2024-07-31-POR.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-31-POR.JPG?raw=true)

![2024-07-31-POC.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-31-POC.JPG?raw=true)

These traces do not have the beautiful cDNA peak around 2000 bp as shown in the manual. However, this is likely expected since we had degraded RNA as our input. I reached out to NEB with the traces and they said they were not surprised by the traces, and recommended moving forward with the cDNA! Yay!

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-07-31.pdf)

#### Normalizing cDNA input to go into step 2.7 (Fragmentation/End Prep)

So, 26 uL of this cDNA goes into step 2.7. How many ng is this?

The amount of ng input into this step determines how many cycles to use in step 2.10.

Tapestation concentrations:

| sample_id | concentration | amount cDNA (conc * 26 uL) | range | recommended # of cycles  | 
|-----------|---------------|----------------------------|-------|------------------------|
| POR       |  0.109 ng/uL  |     2.834 ng               |    1 ng–20 ng  |  6–9        |   
| POC       |  19.2 ng/uL   |     499.2 ng               |     > 100ng    | NA - need to normalize   |


So, I need to normalize my POC cDNA. I want to bring it down to 100ng of input, because even though the concentration is so high, I am guessing that a lot of the cDNA in this is quite short, so I still want to maximize the amount of cDNA going into the reaction. I will have plenty left over and can try again if I want.

To input 100 ng of cDNA into the reaction, I want a final concentration of 100/26 = 3.846 ng/uL

(19.2 ng/uL)(X) = 100 ng

100 / 1.92 = 5.2 uL of cDNA input

So into step 2.7, I am adding 5.2 uL of POC cDNA and 20.8 uL of nuclease free water. 

### cDNA input

Tapestation concentrations:

| sample_id | cDNA input |    range     | recommended # of cycles | 
|-----------|------------|--------------|-------------------------|
|   POR     |  2.834 ng  | 1 ng–20 ng   |     6–9                 |   
|   POC     |  100 ng    | 20 ng–100 ng |     3–6                 |

Split over two thermocylcers and did 9 cycles for POR and 6 for POC.

### FINISHED LIBRARY PREP

![2024-08-01-POR.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-01-POR.JPG?raw=true)

![2024-08-01-POC.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-01-POC.JPG?raw=true)

YAY!! These look SO good! Eluted in 30 uL and 3 uL used for Qubit and Tapestation. Final volume 27 uL.

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-08-01.pdf)

| sample_id | tapestation concentration | ng Library  (conc * 27 uL) |
|-----------|---------------------------|----------------------------|
| POR       |  9.23 ng/uL               |     249.21 ng              |
| POC       |  6.21 ng/uL               |     167.67 ng              |

#### Qubit Values:

- Used dsDNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
  - I have been doing 2 uL of DNA product with 198 uL of DNA buffer, just to reduce any possible pipetting error. This is corrected for in the Qubit readings.
- All samples read twice, standard only read once

DNA Standards: 204.13 (S1) & 24677.72 (S2)

| colony_id | DNA_QBIT_1 | DNA_QBIT_2 | DNA_QBIT_AVG  | ng Library (Qubit * 27 uL) | 
|-----------|------------|------------|---------------|----------------------------|
| POR       |  7.36      |  7.44      |  7.40 ng/uL   |      199.8 ng              |
| POC       |  5.27      |  5.24      |  5.255 ng/uL  |     141.885 ng             |