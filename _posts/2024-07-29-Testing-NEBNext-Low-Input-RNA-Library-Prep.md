---
layout: post
title: Testing NEBNext Low Input RNA Library Prep
date: '2024-07-29'
categories: Protocols
tags: [RNA, Pocillopora, Porites, LCM, Library Prep]
---

## Testing NEBNext Low Input RNA Library Prep

Product: [NEBNext® Single Cell/Low Input RNA Library Prep Kit for Illumina](https://www.neb.com/en-us/products/e6420-nebnext-single-cell-low-input-rna-library-prep-kit-for-illumina)

Protocol: [Link here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/manualE6420_NEBNext_Low_Input_RNA_Library_Prep.pdf). Most of the text here is taken directly from this protocol. I will only be using (and detailing the steps below) for one of the workflows in this protocol: "**Section 2: Protocol for Low Input RNA: cDNA Synthesis, Amplification and Library Generation**". 

I have a sample kit of 6 preps. Detailing the steps of the protocol below, and will have a separate post where I will detail the samples and exact steps or modifications taken.

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
- Agilent® Bioanalyzer® or similar fragment analyzer and associated consumables
  - I will be using an Agilent Tapestation instead
- [NEBNext Oligos](https://www.neb.com/en-us/products/next-generation-sequencing-library-preparation/multiplex-oligos-adaptors-and-primers/multiplex-oligos-adaptors-and-primers)
  - See also: [Can I use this NEBNext kit with adaptors and primers from other vendors than NEB?](https://www.neb.com/en-us/faqs/2019/03/08/can-i-use-this-nebnext-kit-with-adaptors-and-primers-from-other-vendors-than-neb)

#### Kit contents

*All reagents should be stored at –20°C*. Colored bullets indicate the cap color of the reagent to be added to a reaction. 

- ⚪️ Murine RNase Inhibitor
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
- ⚪️ Nuclease-free Buffer

### Best practices (thanks, [Jill](https://github.com/JillAshey/JillAshey_Putnam_Lab_Notebook/blob/master/_posts/2024-06-13-Zymo-Pico-Methyl-Seq-Library-Prep.md))

- Preset the thermocycler programs 
- Thaw and keep all components on ice unless instructed otherwise. Flick to mix and centrifuge before use
	- Avoid multiple freeze-thaws, make aliquots if needed
- Allow beads to equilibrate to room temperature >30 mins before use
- Resuspend beads immediately before each use by gently inverting until homogenous

### Protocol for Low Input RNA: cDNA Synthesis, Amplification and Library Generation

#### Sample Recommendations

- The RNA sample should be free of salts (e.g., Mg2+, or guanidinium salts), divalent cation chelating agents (e.g. EDTA, EGTA, citrate), or organics (e.g., phenol and ethanol). If an excess amount of genomic DNA is present in RNA samples, an optional DNase I treatment could be performed. Inactivate/remove DNase I after treatment.
- Assess quality of the input RNA by running input RNA on an Agilent Bioanalyzer to determine the RNA Integrity Number (RIN).
- **Starting Material**: 2 pg–200 ng poly(A) tail-containing total RNA (DNA free), RIN score ≥ 8.0.
  - Our RNA is definitely not RIN score > 8.0, but we will see what we can do.

#### 2.1 Sample and Reagent preperation

- Prepare fresh 80% Ethanol with nucelase-free water
- Thaw total RNA on ice prior to starting the protocol
- Briefly centrifuge the tubes containing NEBNext Single Cell RT Enzyme Mix to collect solutions to the bottom of the tubes, then **place on ice**.
- Thaw all other frozen components at **room temperature** (if the 10X NEBNext Cell Lysis Buffer appears cloudy after thawing, incubate briefly at 37°C to clear up the solution).
- Mix each component thoroughly, centrifuge briefly to collect solutions to the bottom of the tube, and **then place on ice**. Leave the NEBNext Cell Lysis Buffer bottle at 4°C or at room temperature for storage.

#### 2.2. Primer Annealing for First Strand Synthesis

2.2.1. To anneal cDNA Primer with total RNA samples, prepare the reaction as follows (on ice):

**Note, this is for each RNA sample individually in an individual PCR tube**

- for an input of 4 ng RNA, at  8µl volume, the sample would have a minimum concentration of 0.5 ng/µl
- if you have > 7 µl of an RNA of concentration greater than 0.714 ng/µl (5 ng / 7 µl), you should use the ≥ 5 ng RNA VOLUME (µl) mixture.

| COMPONENT                        | < 5 ng RNA VOLUME (µl) | ≥ 5 ng RNA VOLUME (µl) |
|----------------------------------|------------------------|------------------------|
| Total RNA                        | Up to 8 µl             | Up to 7 µl             |
| 🟣 NEBNext Single Cell RT Primer | 1 µl                    | 2 µl                  |
| Nuclease-free Water              | Variable               | Variable               |
| Total Volume                     | 9 µl                   |  9 µl                  |

2.2.2. Mix well by pipetting up and down gently at least 10 times, then centrifuge briefly to collect solution to the bottom of the tubes.

2.2.3. Incubate for 5 minutes at 70°C in a thermal cycler with the heated lid set to 105°C, then hold at 4ºC until next step.

During the above annealing step, prepare the components for the following step.