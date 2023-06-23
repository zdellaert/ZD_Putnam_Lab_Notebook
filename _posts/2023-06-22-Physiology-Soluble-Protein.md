---
layout: post
title: Putnam Lab Physiology Soluble Protein Protocol
date: '2023-06-22'
categories: Protocols
tags: [Physiology, Protocol]
---

# Soluble Protein Protocol from Coral Tissue Homogenate, Separated into Host and Holobiont Fractions

#### This protocol was adapted from the protocol written by [Hollie Putnam](https://github.com/urol-e5/protocols/blob/master/2020-01-01-Total-Protein-Protocol.md) (and [here](https://github.com/Putnam-Lab/Lab_Management/blob/master/Lab_Resources/Physiology_Protocols/Protein-Content-Protocol.md)) for the Putnam Lab and collaborators in the [E5 project](https://e5coral.org/).

Contents  
- [**Materials**](#Materials)    
- [**Protocol**](#Protocol)  
- [**Standard Table**](#Table)  
- [**References**](#References)  
 
1. <a name="Materials"></a> **Materials**
    - 	[Pierce BCA Protein Assay Kit from Thermo Scientific](https://www.thermofisher.com/order/catalog/product/23225?SID=srch-srp-23225).  
    - 	Clear 96 Well plate
    - 	Incubator or Waterbath with range from 37°C to 50°C.
    - 	Plate reader 
    -  P10, P200, P1000 Pipettes and tips
    -  1.5ml microfuge tubes
    -  DI water


2. <a name="Protocol"></a> **Protocol** 

    Reference protocol: [Pierce BCA Protein Assay Kit](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Pierce_BCA_Protein.pdf)


    **Adult Tissue Sample Preparation for Soluble Protein from Host and Holobiont Fractions**  

    Using this protocol, we are splitting samples into two fractions and will run two replicates per fraction. Therefore, we can fit 19 samples onto each 96-well plate
    
    (19 * 2 fractions * 2 replicates) + (9 standards * 2 replicates)= 76 + 18 = 94 wells)

    So, plan to run ~19 samples per plate and prepare as many samples and plates as you have time for.

    1. Thaw the 1 mL aliquot of homogenate.  
    2. Centrifuge the microcentrifuge tube at 13,000 x rcf for 3 minutes.
        - Move the supernatant to a labelled "Host Protein" tube
        - Resuspend pellet in 1 mL PBS, relable tube as "Holobiont Protein"

    **Preparation of Diluted Albumin (BSA) Standards**    
    1. Dilute the contents of one Albumin Standard (BSA) ampule into several clean vials, preferably using the same diluent as the samples.
    2. Use the following table as a guide to prepare a set of protein standards. For this project we will use the microplate procedure. Diluent is DI water Type II. Each vial will be a sterile 1.5 mL microcentrifuge tube. Label the cap of the microcentrifuge tube with the Vial ID ("A", "B", etc.).  

    <a name="Table"></a> **Standard Table**

    | Vial | Volume of Diluent (μL) | Volume of Source of BSA (μL) | Final BSA Concentration (μg/mL) |
    |------|------------------------|------------------------------|---------------------------------|
    | A    | 0                      | 300 of Stock                 | 2000                            |
    | B    | 125                    | 375 of Stock                 | 1500                            |
    | C    | 325                    | 325 of Stock                 | 1000                            |
    | D    | 175                    | 175 of vial B dilution       | 750                             |
    | E    | 325                    | 325 of vial C dilution       | 500                             |
    | F    | 325                    | 325 of vial E dilution       | 250                             |
    | G    | 325                    | 325 of vial F dilution       | 125                             |
    | H    | 400                    | 100 of vial G dilution       | 25                              |
    | I    | 400                    | 0 (Blank)                    | 0                               |

    **Preparation of the BCA Working Reagent (WR)**   
    1. Use the following formula to determine the total volume of WR required:  
    (# standards + # unknowns) x (# replicates) x (volume of WR per sample) = total volume WR required  

        For this project, we will use 9 standards and 200 μL of WR is required for each sample in the microplate procedure.   

        > *(9 standards + # samples) x (2 replicates) x (200 μL of WR) = total volume WR required*  
        > (9 standards + 10 samples) x (2 replicates) x (200 μL of WR) = 7,600 μL WR  
        > (9 standards + 20 samples) x (2 replicates) x (200 μL of WR) = 11,600 μL WR  
        > **19 samples split into two fractions =~ 1 96-well plate**: (9 standards + 38 samples) x (2 replicates) x (200 μL of WR) = 18,800 μL WR  

    2. Prepare WR by mixing 50 parts of BCA Reagent A with 1 part of BCA Reagent B (50:1, Reagent A:B) in a clean protein-free container of the appropriate size, based on how many samples are going to be run.  *Working reagent will be green and can be kept at room temperature for several days.*

    **Microplate Procedure (Sample to WR ratio = 1:8) from Pierce BCA Protein Assay Kit:**  
    1. Make Plate map for all 9 standards and 2x replicates per sample
    2. Pipette 25 μL of each standard or sample replicate into a microplate well (working range = 20–2000 μg/mL). (For example,Thermo ScientificTM PierceTM 96–Well Plates, Product No. 15041).
    2. Add 200 μL of the WR to each well and mix plate thoroughly on a plate shaker for 30 seconds.
    3. Cover plate and incubate at 37°C for 30 minutes.
    4. Cool plate to RT. Measure the absorbance at or near 562 nm on a plate reader.
    - Wavelengths from 540–590 nm have been used successfully with this method.
    5. Subtract the average 562 nm absorbance measurement of the Blank standard replicates from the 562 nm measurements of all other individual standard and unknown sample replicates.
    6. Prepare a standard curve by plotting the average Blank–corrected 562 nm measurement for each BSA standard vs. its concentration in μg/mL. Use the standard curve to determine the protein concentration of each unknown sample.

3. <a name="References"></a> **References**  
Reference protocol: [Pierce BCA Protein Assay Kit](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Pierce_BCA_Protein.pdf)