---
layout: post
title: LCM Low Input RNA Library Prep
date: '2026-04-24 7:00:00'
categories: Protocols, Processing
tags: [RNA, Pocillopora, Porites, LCM, Library Prep]
---

## Planning for: LCM Low Input RNA Library Prep

I am planning a 48-sample project where I will be performing low-input RNA library prep using this kit.

Using product: [NEBNext® Single Cell/Low Input RNA Library Prep Kit for Illumina](https://www.neb.com/en-us/products/e6420-nebnext-single-cell-low-input-rna-library-prep-kit-for-illumina)

Protocol: [Link here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manualE6420_NEBNext_Low_Input_RNA_Library_Prep.pdf). Most of the text here is taken directly from this protocol. I will only be using (and detailing the steps below) for one of the workflows in this protocol: "**Section 2: Protocol for Low Input RNA: cDNA Synthesis, Amplification and Library Generation**". I successfully tested this on [7/30/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-NEBNext-Low-Input-RNA-Library-Prep/) and on [9/18/24](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Low-Input-RNA-Library-Prep/)

### URI Inventory + Ordering plans

- As of 4/24/26, we have 30 preps of this kit:
  - 12 preps: 2 6-prep sample kits
  - 18 preps: 1 24 prep full size kit (E6420S) which I have used only 6 preps of
    - *(but this was opened in 2024 so maybe a lil expired?)*

- On 4/24/26, I asked for a quote for:
  - 1 24 prep full size kit (E6420S)
  - 1 set of 96 Unique Dual Index oligos (E6440S)
  
- If we order these, in total for this project we will have:
  - 36 preps from unopened kits
  - 18 preps from the 2024 kit
  - 54 preps total
    - So for the 48-sample project we have 6 extra preps to test with
    - And 12 of the preps we use will be from an old kit, is that okay?

#### What about beads?

- total volume of beads per sample = 162 uL/sample 
  - 60 uL (step 2.5.2)
  - 57 uL (step 2.9.2)
  - 45 uL (step 2.11.2)
  - **162 uL/sample * 48 samples = 7776 uL = *8 mL of beads***

- they recommend SPRIselect® Reagent (Beckman Coulter®, Inc. #B23317) or AMPure® XP Beads (Beckman Coulter, Inc. #A63881)
  - SPRI select
    - Total cost = $943.20
      - SPRIselect DNA Size Selection Reagent, 5 mL (#B23317, $471.60)
        - for 10 mL = $471.60*2 = $943.2
        - Alt: 60 mL bottle (#B23318, $1762.00)
  - AMPure XP
    - Total cost = $830.20
      - AMPure XP Beads for DNA Cleanup, 5 mL (#A63880, $415.10)
        - for 10 mL = $415.10*2 = $830.2
        - Alt: 60 mL bottle (#A63881, $1,539.00)
- We typically have bought KAPA Pure Beads (Used these for my previous preps with this kit)
  - Total cost = $394.46
    - KAPA Pure Beads, 5 mL (#07983271001, $197.23)
      - for 10 mL = $197.23*2 = $394.46

#### And then primers and adaptors

See section at very bottom for research, we are just going to order the NEB oligos again.

## Protocol for Low Input RNA: cDNA Synthesis, Amplification and Library Generation

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

### Sample Recommendations

- The RNA sample should be free of salts (e.g., Mg2+, or guanidinium salts), divalent cation chelating agents (e.g. EDTA, EGTA, citrate), or organics (e.g., phenol and ethanol). If an excess amount of genomic DNA is present in RNA samples, an optional DNase I treatment could be performed. Inactivate/remove DNase I after treatment.
- Assess quality of the input RNA by running input RNA on an Agilent Bioanalyzer to determine the RNA Integrity Number (RIN).
- **Starting Material**: 2 pg–200 ng poly(A) tail-containing total RNA (DNA free), RIN score ≥ 8.0.
  - Our RNA is definitely not RIN score > 8.0, but we will see what we can do.

## Day 1

### 2.1 Sample and Reagent preperation

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

### 2.2. Primer Annealing for First Strand Synthesis

**Note, this is for each RNA sample individually in an individual PCR tube**

- [ ] 2.2.1. To anneal cDNA Primer with total RNA samples, prepare the reaction as follows (on ice):

- for an input of 4.99 ng RNA, at 8µl volume, the sample would have a minimum concentration of 0.62 ng/µl
  - Most of our high quality RNA is below this concentration, so we will use the < 5 ng mixture
  - for a low-concentration sample (like LCM RNA), of lets say, 0.280 ng/µl, 8 µl of input would be 2.24 ng. So we would put in 8 µl of the thawed RNA and use the < 5 ng mixture.
- if you have > 7 µl of an RNA of concentration greater than 0.714 ng/µl (5 ng / 7 µl), you should use the ≥ 5 ng RNA workflow.

| COMPONENT                        | *< 5 ng RNA*: VOLUME (µl) | *≥ 5 ng RNA*: VOLUME (µl) |
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

- **Based on looking at other Putnam lab Library Prep protocols, we almost always have to increase the number of cycles for our input.**
- I have tested 15 cycles (July 2024) and 17 cycles (September 2024), and both worked well. For very degraded RNA input, I recommend 17 cycles.

For the various inputs listed above, the recommended PCR cycles will typically result in cDNA yields between 1–20 ng (in most cases 5–15 ng). We recommend quantifying cDNA after the cleanup (Step 2.5) before proceeding to the library preparation (Sections 2.7–2.12). 

### 🛑 Safe Stopping Point: Samples can be safely stored overnight at 4°C or –20°C.

--- 

### 2.5. Cleanup of Amplified cDNA

#### This should be done at post-PCR bench

- [ ] 2.5.1. Allow the ⚪️ [NEBNext Bead Reconstitution Buffer](https://www.neb.com/en-us/tools-and-resources/video-library/quick-tips---bead-reconstitution-buffer-for-nebnext-single-cell-low-input-rna-library-prep) and the SPRI® beads (if stored at 4°C) to warm to room temperature for at least 30 minutes before use.
  - [ ] Shake SPRI Beads to resuspend well
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

### 2.1 Sample and Reagent preperation

1. Day 2 (Fragmentation/End Prep, Adaptor Ligation, Cleanup of Adaptor-ligated DNA, PCR enrichment, cleanup, and final library QC):
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
  - [ ] Shake SPRI beads to resuspend well
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

From NEB: *If your cDNA input is outside the input range of 1 ng–20 ng, adjust the PCR cycle numbers accordingly. We recommend a minimum of 3 PCR cycles for all of the original molecules to make it into the final library. For cDNA yield of 100 pg we recommend testing 12 PCR cycles. For cDNA input of 1 ng–20 ng, the typical Illumina library yield, using 8 PCR cycles, is 100 ng–1 μg.*

From Zoe: I have tested this kit with 9 and 11 cycles at this step, using 9 cycles for an input of 3 ng cDNA and 11 for an input of < 3 ng (as low as 0.6ng). Based on this experience, **any cDNA concentration of less than 5 ng could probably benefit from 11 cycles**

| CYCLE STEP           | TEMP  | TIME       | CYCLES | 
|----------------------|-------|------------|--------|
| Initial Denaturation | 98°C  | 30 seconds | 1      |
|   | | | 
| Denaturation         | 98°C  | 10 seconds | 8 *dependent on cDNA input* *See Note Above |
| Annealing/Extension   | 65°C  | 75 seconds |^        |
|   | | | 
| Final Extension      | 65°C  | 5 minutes  | 1       |
| Hold                 | 4°C   | ∞          |         |


### 2.11. Cleanup of PCR Reaction

- [ ] 2.11.1. If stored at 4°C allow the SPRI beads to warm to room temperature for at least 30 minutes before use.
  - [ ] Shake SPRI beads to resuspend well
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

#### Typical Yield of Illumina Library from a Reaction

Actual yields will depend on the quality and quantity of the input cDNA. Typical library yields range between 100 ng–1 μg based on the PCR cycle recommendations provided in Section 2.10.

## Notes 

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
  - 7-21 cycles (likely 15-17) of
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

### NEBNext Adaptor for Illumina Overview

NEBNext Adaptor for Illumina sequence:

5´-/5Phos/GAT CGG AAG AGC ACA CGT CTG AAC TCC AGT CdUA CAC TCT TTC CCT ACA CGA CGC TCT TCC GAT C-s-T-3´

5´-/5Phos/GATCGGAAGAGCACACGTCTGAACTCCAGTC dU ACACTCTTTCCCTACACGACGCTCTTCCGATC-s-T-3´

The following sequences are used for adaptor trimming of NEBNext adaptors for Illumina:
Read 1 AGATCGGAAGAGCACACGTCTGAACTCCAGTCA
Read 2 AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGT

| PRODUCT | INDEX PRIMER SEQUENCE | EXPECTED INDEX PRIMER SEQUENCE READ      |
|----------|----------------------|-------------------------------|
| NEBNext Index 1 Primer for Illumina (10 µM) | 5´- CAAGCAGAAGACGGCATACGAGATCGTGATGTGACTGGAGTTCAGACGTGTGCTCTTCCGA TC-s-T-3´  | ATCACG |
| NEBNext Index 2 Primer for Illumina (10 µM) | 5´- CAAGCAGAAGACGGCATACGAGATACATCGGTGACTGGAGTTCAGACGTGTGCTCTTCCGA TC-s-T-3´  | CGATGT |

### Research about adaptors and if we can use custom ones or not

#### Breakdown of info below:

Overall cost summary: 

- Option A – NEB adaptor + existing UDIs + buy USER:
  - Extra cost: $267
  - Pros: Kit‑recommended adaptor chemistry, no need to order UDIs, but protocol stays very close to recommendations
- Option B – Puritz adapters + existing UDIs (no USER):
  - Extra cost: $0
  - Pros: Cheapest
  - Cons: requires protocol testing and maybe test sequencing.
- Option C – NEB 96 UDI kit (includes USER) + NEB adaptor:
  - Extra cost: $606
  - Pros: Fully “by the book” NEB solution; new standardized UDI set.

#### Options A/B: Can we use our WGBS custom indeces (UDIs) with this kit?

Yes.

- The index primers we have in lab are listed [here](https://github.com/Putnam-Lab/Lab_Management/blob/master/Lab_Resources/DNA_RNA-protocols/Indexes_and_Barcodes/UDI_Index_Primer_Pairs_for_Pico_WGBS.csv) (and I downloaded a version 9/15/2024 [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/resources/UDI_Index_Primer_Pairs_for_Pico_WGBS.csv))
  - these were designed for WGBS with the Zymo Pico Kit
  - Each of the 60 pairs has a unique i7 and unique i5 sequence, for example:
  
| UDIndexName | i7_      | i7Bases (Sample Sheet) | i5Bases (sample sheet) | i7_   | i7_UDI Sequence | i5        | i5_UDI      |
|-------------|----------|------------------------|------------------------|-------|-----------------|-----------|-------------|
| UDI0001    | AACCGCGG | CCGCGGTT | AGCGCTAG  | i7_UDI0001 | CAAGCAGAAGACGGCATACGAGATAACCGCGGGTGACTGGAGTTCAGACGTGT | i5UDI0001 | AATGATACGGCGACCACCGAGATCTACACAGCGCTAGACACTCTTTCCCTACACGAC |
| UDI0002    | GGTTATAA | TTATAACC | GATATCGA  | i7_UDI0002 | CAAGCAGAAGACGGCATACGAGATGGTTATAAGTGACTGGAGTTCAGACGTGT | i5UDI0002 | AATGATACGGCGACCACCGAGATCTACACGATATCGAACACTCTTTCCCTACACGAC |

  - the i7_UDI Sequence contains:
    - CAAGCAGAAGACGGCATACGAGAT
      - Illumina P7 adaptor: 5'- CAAGCAGAAGACGGCATACGAGA**T** -3'
        - **T overhang**
    - unique i7_ sequence (UDI0001: AACCGCGG, UDI0002: GGTTATAA)
    - GTGACTGGAGTTCAGACGTGT
      - Reverse completment: ACACGTCTGAACTCCAGTCA
  - the i5_UDI Sequence contains:
    - AATGATACGGCGACCACCGAGATCTACAC
      - Illumina P5 adaptor: 5'- AATGATACGGCGACCACCGAGATCTACAC -3'
    - unique i5_ sequence (UDI0001: AGCGCTAG, UDI0002: GATATCGA)
    - ACACTCTTTCCCTACACGAC
      - reverse complement: GTCGTGTAGGGAAAGAGTGT

[Helpful resource here](https://teichlab.github.io/scg_lib_structs/methods_html/Illumina.html)

These index primers are compatible with our library prep kit, but we need to order/find adaptors that will work with these primers.

#### Option A: Maybe I have enough NEBNext adaptor already in lab, order more USER enzyme

I had a kit of single index oligos from NEB - used for the LCM pilot.

Contents:
- E7337A NEBNext Adaptor for Illumina 0.24 ml = 240 uL
- E7338A USER Enzyme 0.072 ml

What did I use:
- 2.5 uL * 10 = 25 uL of diluted adaptor
  - 1 uL of undiluted adaptor 
  - 240 uL - 239 uL = 238 uL left
    - so I should have more than enough, would need ~5 uL of undiluted adaptor
- 3 uL * 10 = 30 uL USER Enzyme
  - 72 uL - 30 uL = 42 uL
    - That is enough USER enzyme for 14 samples
    - I need 102 uL more (102 units)

- ordering information for USER enzyme
  - 1,000 units/ml	50 units	$89.00 * 3 = $267 for 150 units
  - 1,000 units/ml	250 units	$362.00

#### Option B: Puritz Lab adaptors - could we use these?

| Sequence Name | Sequence                                       | INLINE BARCODE | ENZYME COMPATABILITY | BarcodeIndex_2500 | BarcodeIndex_4000 | Library Prep            | Notes | Type    |
|---------------|------------------------------------------------|----------------|----------------------|-------------------|-------------------|-------------------------|-------|---------|
| Y-inline-1a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTATCACG*T       | ATCACG         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-2a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTCGATGT*T       | CGATGT         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-3a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTTTAGGC*T       | TTAGGC         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-4a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTTGGCCA*T       | TGGCCA         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-5a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTACAGTG*T       | ACAGTG         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-6a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTGCCAAT*T       | GCCAAT         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-7a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTCAGATC*T       | CAGATC         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-9a   | CACTCTTTCCCTACACGACGCTCTTCCGATCTGATCAG*T       | GATCAG         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-10a  | CACTCTTTCCCTACACGACGCTCTTCCGATCTTAGCTT*T       | TAGCTT         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-11a  | CACTCTTTCCCTACACGACGCTCTTCCGATCTGGCTAC*T       | GGCTAC         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-12a  | CACTCTTTCCCTACACGACGCTCTTCCGATCTCTTGCA*T       | CTTGCA         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-1b   | /5Phos/C*GTGATAGATCGGAAGAGCACACGTCTGAACTCCAGTC | ATCACG         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-2b   | /5Phos/A*CATCGAGATCGGAAGAGCACACGTCTGAACTCCAGTC | CGATGT         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-3b   | /5Phos/G*CCTAAAGATCGGAAGAGCACACGTCTGAACTCCAGTC | TTAGGC         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-4b   | /5Phos/T*GGCCAAGATCGGAAGAGCACACGTCTGAACTCCAGTC | TGGCCA         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-5b   | /5Phos/C*ACTGTAGATCGGAAGAGCACACGTCTGAACTCCAGTC | ACAGTG         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-6b   | /5Phos/A*TTGGCAGATCGGAAGAGCACACGTCTGAACTCCAGTC | GCCAAT         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-7b   | /5Phos/G*ATCTGAGATCGGAAGAGCACACGTCTGAACTCCAGTC | CAGATC         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-8b   | /5Phos/T*CAAGTAGATCGGAAGAGCACACGTCTGAACTCCAGTC | ACTTGA         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-9b   | /5Phos/C*TGATCAGATCGGAAGAGCACACGTCTGAACTCCAGTC | GATCAG         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-10b  | /5Phos/A*AGCTAAGATCGGAAGAGCACACGTCTGAACTCCAGTC | TAGCTT         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-11b  | /5Phos/G*TAGCCAGATCGGAAGAGCACACGTCTGAACTCCAGTC | GGCTAC         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |
| Y-inline-12b  | /5Phos/T*GCAAGAGATCGGAAGAGCACACGTCTGAACTCCAGTC | CTTGCA         | NA                   |                   |                   | EecSeq, Genomic, RNAseq |       | Adapter |

#### What do I need to know about these?

1. Can I use them? (Jon)
2. Are they annealed or signle stranded?
3. What concentration are they in right now


##### Protocol modification for Puritz Lab adaptors

There are no exact instructions on how to modify the protocol with use of custom adapters/primers, but this is how the general NEBNext Ultra II FS DNA library prep protocol (which this kit post-cDNA is based on) is modified for the NEB UMI Adaptors for Illumina (instead of the universal NEBNext Adaptor): [Original Protocol](https://www.neb.com/en-us/-/media/nebus/files/manuals/manuale6177-e7805.pdf?rev=cfd70057c01446f7bbdeea0efc8d70d9&hash=633520E477BEFF793DD3D25971E69207) --> [Modified protocol](https://www.neb.com/en-us/-/media/nebus/files/manuals/manuale6177_e7805-w-umi-adaptors-dna.pdf?rev=3a5b771761b849fa815e17d4fcf53b0a&hash=09513A246A7D406D74DC6C90EC3B3807)

However, I should note that the adaptors I would use do not have UMIs so I think I would still need to use the 10 uL total of the i5/i7 WGBS primers.

1. 2.5 uL of the NEBNext UMI Adaptors for Illumina is used instead of 2.5 uL of the NEBNext Adaptor
   1. For cDNA input < 5ng, Adaptors are diluted as follows:
      1. NEBNext Adaptor (normal protocol, exactly like the Low Input RNA kit)
         1. 25-Fold (1:25) --> 0.6 µM
      2. NEBNext UMI Adaptor (special protocol)
         1. 1 ng to < 5 ng:
            1. 50-Fold (1:50) 0.4 µM
         2. < 1 ng:
            1. 100-Fold (1:100) 0.2 µM
2. Safe stopping point after the 15 minute incubation instead of adding the USER enzyme continued by another incubation.
3. In the bead cleanup, a ratio of 0.6X of beads is used instead of 0.8X. And then, the elution is 20 uL instead of 15 uL.
4. In PCR enrichment, the 5uL of the NEBNext primer mix is used instead of 10 uL sample-specific i5/i7 index primers. 
5. The primer-dimer and adaptor-dimer peaks will be at different expected bps depending on which adaptor/primer set was used

#### Option C: Just order the NEB Oligo 

NEBNext® Multiplex Oligos for Illumina® (96 Unique Dual Index Primer Pairs)	606.00	96	preps
