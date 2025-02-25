---
layout: post
title: LCM Pilot Zymo Trio WGBS Library Prep Testing
date: '2025-02-22'
categories: Processing
tags: [DNA, Pocillopora, LCM, Library Prep]
---

## LCM Zymo Trio WGBS Library Prep

Protocol link [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/LCM-Zymo-Trio-WGBS-Library-Prep/)

## Samples: Testing 2 of the 10 extracted on 9/13

[Zoe metadata link](https://docs.google.com/spreadsheets/d/1b1TPzleqo81ZLjrh_UIpXEftsjxhxqaMHd7ldFU9oLU/edit?gid=722422936#gid=722422936)

Tapestation concentrations:

| sample_id      | concentration | DIN | 
|----------------|------------|------------|
| #9 (Frag B)    |  4.37 ng/uL  | 3.1 | 
| #15 (Frag C)   |  3.80 ng/uL  | 2.4 | 

## Library Prep

- Rest of DNA (~9.5 uL for each sample) brought up to 20 uL with Tris buffer, with non-methylated DNA (*E. coli* DNA) spike-in
  - 100 pg of non-fragmented *E. coli* DNA was added to each sample, 0.4 uL of a 0.25 ng/uL dilution of the provided *E. coli* DNA
- Processed using EZ Methylation Gold Kit for Bisulfite Conversion (standard thermocycler settings), cleaned according to protocol and eluted in 19 uL DNA elution buffer
- Did 20 PCR cycles during Index PCR
- Adjusted protocol from Zymo Rep:
  - Following index PCR, please follow the below steps for bead cleanup before the written Appendix A protocol:
    - Add 60 µL of Select-a-Size MagBeads and mix thoroughly. Incubate for 5 minutes at room temperature.
    - Pellet on a magnetic stand for 3 minutes or until the supernatant is clear. Carefully remove and discard the supernatant.
    - Remove the sample from the magnetic stand and add 50 µL of DNA Elution Buffer, mixing thoroughly by pipetting. 
    - Add 60 µL Library Binding Solution to the resuspended sample+bead and mix thoroughly. Incubate for 5 minutes at room temperature.
    - Proceed to the Appendix A cleanup protocol beginning with Step 2 (placing tube on magnetic stand), and carry out the remaining steps as usual.

### QC

Run to visualize libraries. Here's an example of what the **library should look like** on a Tapestation: 

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/zymo_trio/manual_trio_wgbs_QC.png?raw=true" height="400">

"If adapter dimers are present, they will form an approximately 130-180 bp band. Yields will vary depending on the total quantity and quality of sample input DNA.

## Results

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2025-02-24-LCM-WGBS-Trio-libraries.png?raw=true" height="500">

This is really interesting. There seems to be better concentration, but more adapter dimer. Will write Zymo.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2025-02-24-LCM-WGBS-Trio-library-9.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2025-02-24-LCM-WGBS-Trio-library-15.png?raw=true" height="400">

Compare to sequenced libraries (pre extra cleanup):

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-1.png?raw=true" height="400">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_WGBS/2024-12-15-LCM-WGBS-Trio-library-24.png?raw=true" height="400">


Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2025-02-22-Trio-LB-test.pdf)

