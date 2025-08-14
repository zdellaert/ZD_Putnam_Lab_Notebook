---
layout: post
title: SwitchFree library prep
date: '2025-08-13 7:00:00'
categories: Protocols, Processing
tags: [Pocillopora, RNA, Library Prep]
---

## "TagSeq" Zymo Switch-Free RNA Library Prep Test/Protocol

Using product: [Zymo-Seq SwitchFree 3' mRNA Library Kit](https://www.zymoresearch.com/products/zymo-seq-switchfree-3-mrna-library-kit). See Zymo's protocol [here](https://files.zymoresearch.com/protocols/_r3008_r3009__zymo_seq_switchfree_3_mrna_library_kit.pdf). Basing this protocol directly off of [Jill Ashey's](https://github.com/JillAshey/JillAshey_Putnam_Lab_Notebook/blob/master/_posts/2024-03-29-Zymo-SwitchFree.md) successful testing of the kit for *Pocillopora* larval samples.

### Goal for today

Today, Natalie and I will test the library prep on three adult samples from my [Time Series project](https://github.com/zdellaert/TimeSeries). We will do all three with two versions of the protocol: one per sample as written and one prep per sample with 3 uL of Poly A reagent instead of 5 uL.

The kit needs a minimum of 10 ng of total RNA or a maximum of 500 ng of total RNA. We will be using **20 ng of total RNA** as input. Here's a breakdown of input RNA volumes for each sample: 


| TubeID       | Qubit RNA (ng/uL) | Strip tube # | RNA (uL) | RNAse/DNase-Free water (uL) | Total starting volume (ul) | PolyA R1 volume (ul) | Primer |
| ------------ | ----------------- | ------------ | -------- | --------------------------- | --------------------|------------- | ------ |
| POC_R12_C3   | 28.6             | 1            | 0.70     | 4.30                        | 5.0        | 5.0            | X    |
| POC_R1_H1    | 24.6              | 2            | 0.81 | 4.19                  | 5.0           | 5.0        | X    |
| POC_R3_C3    | 17.7              | 3            | 1.13 | 3.87                  | 5.0         | 5.0              | X   |
| POC_R12_C3   | 28.6             | 4            | 0.70 | 4.30                  | 5.0           | 3.0              | X    |
| POC_R1_H1    | 24.6             | 5            | 0.81 | 4.19                  | 5.0           | 3.0               | X   |
| POC_R3_C3    | 17.7              | 6            | 1.13 | 3.87                  | 5.0        | 3.0                  | X   |

Here's the SwitchFree library prep workflow: 

![](https://raw.githubusercontent.com/JillAshey/JillAshey_Putnam_Lab_Notebook/master/images/switchfree_lib_prep_workflow.png)

### Materials 

- [Zymo-Seq SwitchFree 3' mRNA Library Kit](https://www.zymoresearch.com/products/zymo-seq-switchfree-3-mrna-library-kit)
- PCR tubes 
- Thermocycler 
- Mini centrifuge
- Aluminum beads (to keep things on ice)
- Magnetic stand for PCR tubes 
- Kit contents 

![](https://raw.githubusercontent.com/JillAshey/JillAshey_Putnam_Lab_Notebook/master/images/switchfree_lib_prep_contents.png)

### Buffer preperation 

Once buffers are prepared for a kit, they do not need to be prepared again. 

- Add 300 uL of the Select-a-Size MagBead concentrate to 10 mL of Select-a-Size MagBead Buffer. 
	- These should be prepared at least 5 days ahead of library prep. 
- Add 24 mL of 100% ethanol to the DNA Wash Buffer concentrate. Store at room temperature. 

### Best practices 

- Avoid multiple freeze thaws of all components, and aliquot components as necessary
- Remove enzymes from cold storage just before use and return to cold storage immediately after use
- Thaw and maintain all components on ice unless noted otherwise 
- Flick to mix thawed components and briefly centrifuge prior to use 
- After adding each component, mix by pipetting up and down 15-20 times. Briefly centrifuge after 
- Pre-program thermal cycler with lid heating ON set to >100-105°C 
- Turn on thermocycler day-of to preheat 
- Pre-calculate how much to dilute RNA samples 

### Protocol 

#### Section 1: cDNA Synthesis 

Thermocycler settings: 

![](https://raw.githubusercontent.com/JillAshey/JillAshey_Putnam_Lab_Notebook/master/images/switchfree_lib_prep_section1_thermocycler.png)

- Thaw PolyA R1 Reagent and R2 Reagent on ice 
- Prepare samples to correct volume in strip tubes 
- Add 5 uL of PolyA R1 Reagent to each sample
  - **AS A TEST: FOR HALF OF SAMPLES, ADD 3 uL PolyA R1 and 2 uL RNAse/DNAse-free water** 
- Mix by pipetting and centrifuge briefly 
- Run Steps 1-2 in thermocycler 
	- SKIP this step if RNA is degraded/low quality 
- While in the thermocycler on the 4°C hold, add 10 uL of R2 Reagent to each sample 
- Mix by pipetting 
- Run Steps 3-4
- While Steps 3-4 are running, allow Reaction Clean-up Solution to equilibrate to room temperature 
- While in the thermocycler on the 42°C hold, add 4 uL of Reaction Clean-up Solution to each sample 
- Mix by pipetting and centrifuge briefly 
- Immediately return to thermocycler 
- Run Steps 5-7
- Remove tubes from thermocycler 
- Add 26 uL of 95% ethanol to each sample 
- Do bead clean-up with Select-a-Size MagBeads 
	- Allow beads to equilibrate to room temperature >30 minutes before use 
	- Resuspend beads immediately before use by shaking or vortexing until homogenous 
	- Add 110 uL of Select-a-Size MagBeads to each sample 
	- Pipette to mix until homogenous
	- Incubate for 5 minutes at room temperature 
	- Put samples on magnetic stand for 5 mins or until beads have fully separated from solution 
	- Aspirate slowly and discard supernatent 
	- While the sample is still on the magnetic stand, add 200 uL of DNA Wash Buffer without disturbing the pellet 
	- Aspirate slowly and discard supernatent 
	- Repeat this wash step again 
	- Keep the caps open to air-dry bead for 1 minute 
	-  Aspirate any residual wash buffer
	-  Continue to air dry pellet until it appears matte without cracking (see picture below)
		- ![](https://raw.githubusercontent.com/JillAshey/JillAshey_Putnam_Lab_Notebook/master/images/DT_mcap2023/ribofree_beads.png)
	- Remove sample from magnetic stand 
	- Add 10 uL of DNA Elution Buffer to each sample 
	- Pipette to mix until homogenous
	- Put samples on magnetic stand for 1-2 minutes or until elute is clear
	- Move elute to new PCR tubes 
	
#### Section 2: Adapter Ligation 

Thermocycler settings: 

Step 1: 95°C for 3 minutes, 4°C for 2 minutes, 4°C hold 

Step 2: 25°C for 45 minutes (lid temperature at 40°C), 4°C hold 

- Thaw 3'mRNA L Reagent on ice 
- Put samples in thermocycler and run Step 1 
- Remove samples from thermocycler and put on ice 
- Add 15 uL of 3'mRNA L Reagent to each sample 
- Mix by pipetting and centrifuge briefly 
- Run Step 2 
- Remove samples from thermocycler 
- Add 25 uL of DNase/RNase free water to each sample 
- Do bead clean-up with Select-a-Size MagBeads 
	- Allow beads to equilibrate to room temperature >30 minutes before use 
	- Resuspend beads immediately before use by shaking or vortexing until homogenous 
	- Add 100 uL of Select-a-Size MagBeads to each sample 
	- Pipette to mix until homogenous
	- Incubate for 5 minutes at room temperature 
	- Put samples on magnetic stand for 5 mins or until beads have fully separated from solution 
	- Aspirate slowly and discard supernatent 
	- While the sample is still on the magnetic stand, add 200 uL of DNA Wash Buffer without disturbing the pellet 
	- Aspirate slowly and discard supernatent 
	- Repeat this wash step again 
	- Keep the caps open to air-dry bead for 1 minute 
	-  Aspirate any residual wash buffer
	-  Continue to air dry pellet until it appears matte without cracking (see picture above)
	- Remove sample from magnetic stand 
	- Add 15 uL of DNA Elution Buffer to each sample 
	- Pipette to mix until homogenous
	- Put samples on magnetic stand for 1-2 minutes or until elute is clear
	- Move elute to new PCR tubes 

#### Section 3: Library amplification 

Thermocycler settings: 

![](https://raw.githubusercontent.com/JillAshey/JillAshey_Putnam_Lab_Notebook/master/images/switchfree_lib_prep_section2_thermocycler.png) 

Given the low input for these preps and my previous experience with other Zymo kits, we are going to do 21 PCR amplification cycles. 

- Thaw Index Primers and ZymoTaq Premix on ice 
- Allow Library Binding Solution to equilibrate to room temperature >30 minutes before use 
- Add 10 uL of unique Index Primer to each sample
- Mix by pipetting 
- Add 25 uL of Zymo TaqPremix to each sample 
- Mix by pipetting and centrifuge briefly 
- Run thermocycler program above 
- Remove samples from thermocycler 
- Add 50 uL of DNase/RNase free water to each sample 
- Add 80 uL of Select-a-Size MagBeads to each sample 
- Pipette until homogenous 
- Incubate for 5 minutes at room temperature 
- Place samples on magnetic stand for 5 minutes or until beads have separated from solution 
- Aspirate slowly and discard supernatent 
- Remove samples from magnetic stand 
- Add 100 uL of DNA Elution Buffer to beads 
- Pipette until homogenous 
- Add 80 uL of Library Binding Solution to each sample 
- Pipette until homogenous 
- Incubate for 5 minutes at room temperature 
- Do bead clean-up with Select-a-Size MagBeads (beads already added to samples)
	- Put samples on magnetic stand for 5 mins or until beads have fully separated from solution 
	- Aspirate slowly and discard supernatent 
	- While the sample is still on the magnetic stand, add 200 uL of DNA Wash Buffer without disturbing the pellet 
	- Aspirate slowly and discard supernatent 
	- Repeat this wash step again 
	- Keep the caps open to air-dry bead for 1 minute 
	-  Aspirate any residual wash buffer
	-  Continue to air dry pellet until it appears matte without cracking (see picture above)
	- Remove sample from magnetic stand 
	- Add 15-20 uL of DNA Elution Buffer to each sample 
	- Pipette to mix until homogenous
	- Put samples on magnetic stand for 1-2 minutes or until elute is clear
	- Move elute to new PCR tubes 

THIS IS THE FINAL 3' mRNA-seq LIBRARY. STORE AT -20°C. 

#### QC

Run [DNA Tapestation](https://github.com/meschedl/MESPutnam_Open_Lab_Notebook/blob/master/_posts/2019-07-30-DNA-Tapestation.md) to visualize libraries. Here's an example of what the library should look like on a Tapestation: 

![](https://raw.githubusercontent.com/JillAshey/JillAshey_Putnam_Lab_Notebook/master/images/switchfree_lib_prep_library_example.png)

- Used Broad range DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 182.07 (S1) & 23026.07 (S2)

| TubeID       | PolyA R1 volume (ul) | Primer | Library_QBIT_1 | Library_QBIT_2 | Library_QBIT_AVG |
| ------------ |--------------------- | ------ |------------|------------|--------------|
| POC_R12_C3   |  5.0                  | 1      | 4.14   |  4.10     |  4.12       |
| POC_R1_H1    |  5.0                 | 2      | 3.22   |  3.16    |   3.19       |
| POC_R3_C3    | 5.0                   | 3      | 3.94   |  4.00     |   3.96      |
| POC_R12_C3   |  3.0                 | 8      | 6.00  |  6.00    |   6.00      |
| POC_R1_H1    | 3.0                  | 7      | 3.62  |  3.60     |   3.61      |
| POC_R3_C3    |  3.0                 | 6      | 4.96 | 5.02    |   4.98     |

<img width="400" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.10.png?raw=true">

<img width="400" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.20.png?raw=true">

| TubeID       | 5 ul PolyA reagent | 3 ul PolyA | 
| ------------| ------------ |--------- | 
| POC_R12_C3 | <img width="600" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.30.png?raw=true"> | <img width="600" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.44.png?raw=true">| 
| POC_R1_H1  | <img width="600" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.35.png?raw=true"> | <img width="600" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.50.png?raw=true"> | 
| POC_R3_C3 | <img width="600" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.40.png?raw=true"> | <img width="600" alt="2025-08-13-SwitchFree" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation//SwitchFree/Screenshot 2025-08-14 at 07.10.56.png?raw=true"> | 


Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2025-08-13.pdf) and [here (not scaled by sample)](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2025-08-13-scaled.pdf). 


### Thoughts

- Did 21 cycles when I meant to do 19 - could be the cause of the dimers. However, concentration is lower than ideal. I wonder if increasing or **decreasing** the RNA input amount could help...

### Convert library concentration from ng/μL to nM 

First, library concentrations were converted from ng/μL to nM using the [equation](https://knowledge.illumina.com/library-preparation/dna-library-prep/library-preparation-dna-library-prep-reference_material-list/000001240):

(concentration in ng/μL)/(660g/mol * average library size in bp) * 10^6 = concentration in nM

<img width="600" alt="Molarity_formula" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/Molarity.jpeg?raw=true">

| Library_Tube | Library_QBIT_1 | Library_QBIT_2 | Primer | TubeID     | PolyA R1 volume (ul) | Qubit_Conc | TS_Conc | TS_Peak_Size | Molarity_nM_Qubit | Molarity_nM_TS_Calculated | Molarity_nM_TS_Peak |
|--------------|----------------|----------------|--------|------------|----------------------|------------|---------|--------------|-------------------|---------------------------|---------------------|
| 1            | 4.14           | 4.1            | 1      | POC_R12_C3 | 5                    | 4.12       | 4.63    | 381          | 16.38             | 18.41                     | 17.50               |
| 2            | 3.22           | 3.16           | 2      | POC_R1_H1  | 5                    | 3.19       | 4.7     | 406          | 12.69             | 18.69                     | 17.10               |
| 3            | 3.94           | 4              | 3      | POC_R3_C3  | 5                    | 3.96       | 4.72    | 408          | 15.75             | 18.77                     | 16.90               |
| 4            | 6              | 6              | 8      | POC_R12_C3 | 3                    | 6          | 6.31    | 399          | 23.86             | 25.09                     | 24.30               |
| 5            | 3.62           | 3.6            | 7      | POC_R1_H1  | 3                    | 3.61       | 4.32    | 407          | 14.36             | 17.18                     | 16.30               |
| 6            | 4.96           | 5.02           | 6      | POC_R3_C3  | 3                    | 4.98       | 5.23    | 409          | 19.80             | 20.80                     | 19.20               |

### Normalize

- Normalize library: Dilute to 4nM in a volume of 6-10μL with molecular grade water using the calculation C1V1=C2V2.
- Combined into pool (n=XX libraries per pool) for sequencing
- Quantified with Qubit dsDNA HS Assay Kit (Invitrogen #Q33231) and tapestation analysis with the D5000 ScreenTape

| Library_Tube | Amount_Library_4nM | Amount_H20_4nM |
|--------------|--------------------|----------------|
|      1       | 2.44               | 7.56           |
|      2       | 3.15               | 6.85           |
|      3       | 2.54               | 7.46           |
|      4       | 1.68               | 8.32           |
|      5       | 2.79               | 7.21           |
|      6       | 2.02               | 7.98           |