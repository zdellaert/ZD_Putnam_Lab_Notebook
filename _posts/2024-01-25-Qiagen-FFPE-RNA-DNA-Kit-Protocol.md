---
layout: post
title: Qiagen AllPrep DNA/RNA FFPE Kit Protocol
date: '2024-01-25'
categories: Protocols
tags: [DNA, RNA, PAXgene, Protocol, LCM]
---

## Goal: to extract *high-quality* gDNA and total RNA from PAXgene-fixed cryosectioned tissue.

## Materials and Equipment

- Qiagen AllPrep DNA/RNA FFPE [Kit](https://www.qiagen.com/us/products/discovery-and-translational-research/dna-rna-purification/multianalyte-and-virus/allprep-dnarna-ffpe-kit), [manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Qiagen_AllPrep_DNA_RNA_FFPE.pdf)
- Heating block capable of heating to 90ºC
- Centrifuge and rotor capable of spinning at 15,000 rcf
- 100% Ethanol
- 100% Isopropanol
- Plastics: Several 1000 uL, 200 uL, and 20 uL pipette tips per sample.

## First time opening kit: Reagent Preparation

- Check all buffers for precipitates. Make sure to warm and reconstitute any precipitates as directed in the [manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Qiagen_AllPrep_DNA_RNA_FFPE.pdf).
- Add 42 ml isopropanol to Buffer FRN (14 ml). Mix by shaking. Tick the check box on the bottle label to indicate that isopropanol has been added.
- Prep DNAse I stock solution as directed
- Add 44 ml ethanol to Buffer RPE (11 ml). Mix by shaking. Tick the check box on the bottle label to indicate that ethanol has been added.
- Add 25 ml ethanol to Buffer AW1 (19 ml). Mix by shaking. Tick the check box on the bottle label to indicate that ethanol has been added.
- Add 30 ml ethanol to Buffer AW2 (13 ml). Mix by shaking. Tick the check box on the bottle label to indicate that ethanol has been added.

## Sterilizing working area to maintain an RNAse-free environment

Clean bench with clean paper towels (spray solution, wipe down) in the following order:

  1. 10% bleach solution  
  2. DI water  
  3. 70% ethanol
  4. RNAse cleaner (spray bottle)

Clean pipettes, tip boxes, and the controls on the heating block and centrifuge by squirting 70% ethanol on a paper towel and wiping them down. Repeat with RNAse cleaner. Wipe down gloves with 70% ethanol and RNAse cleaner. Do not spray solutions directly on the equipment.

## Alternative starting material: Sample prep from cyrosectioned, slides Paxgene Fixed, Cryo-Embedded tissue (coral)

- Remove a cryosectioned slide from -80 ºC (same sample/sectioning round as used for LCM), transfer to -20 ºC for 30 minutes, then transfer slide to cooler with dry ice
    - Rinse slide in 70% Ethanol for 5 minutes on dry ice
    - Replace ethanol with RNAse/DNAse-free water to rinse
    - Remove slide to dark background over PCR rack (over dry ice, though be careful to not freeze the water once the volume on the slide is low, if that's freezing move to regular ice) and use sterile razor blade, cleaned with RNAse cleaner, to scrape off tissue sections into a tube filled with prepared RD2 digestion buffer.
- Or, place cryosectioned sections straight into 1.5 mL tube at cryostat

## Protocol Steps, Starting from after deparrafinization steps (step 5)(trying to adapt for cryoembedded samples, no paraffin embedding)

5. Adding 150 μl Buffer PKD and flicking the tube to loosen the pellet. Add 10 μl proteinase K and mix by vortexing.
   - **Alternatively, prep this mixture ahead of time and add sectioned tissue to this mixture, adapted from notes [here](https://www.preanalytix.com/storage/download/_ProductResources_/SuppProtocols/HB-0164-S02-001_PX22_SP_RNA_including_miRNA_from_PFCE_sections_0716_WW.pdf)**
6. Incubate at 56°C for 15 mins
   - Depending on the sample material, the sample may not be completely lysed. This does not affect the procedure. Proceed to step 7.
7. Incubate on ice for 3 min.
   - Complete cooling is important for efficient precipitation in step 8.
8. Centrifuge for 15 min at 20,000 x g.
9. Carefully transfer the supernatant, without disturbing the pellet, to a new 1.5 ml tube for RNA purification in steps 10–24. Keep the pellet for DNA purification in steps 25–35.
    - The DNA-containing pellet can be stored for 2 h at room temperature, for up to 1 day at 2–8°C or for longer periods at –30 to –15°C.

### Purification of total RNA
10. Incubate the supernatant from step 9 at 80°C for 15 min.
    - This incubation step partially reverses formaldehyde modification of nucleic acids. Longer incubation times or higher incubation temperatures may result in more fragmented RNA.
      - **May not be necessary for paxgene fixed samples? unclear**, look more into the protocol [here](https://www.preanalytix.com/storage/download/_ProductResources_/SuppProtocols/HB-0164-S02-001_PX22_SP_RNA_including_miRNA_from_PFCE_sections_0716_WW.pdf)
    - If using only one heating block, keep the supernatant at room temperature until the heating block has reached 80°C. To ensure maximum RNA yields, the supernatant must be incubated at 80°C only for exactly 15 min.
11. Briefly centrifuge the tube to remove drops from the inside of the lid.
12. Add 320 μl Buffer RLT to adjust binding conditions, and mix by vortexing or pipetting.
13. Add 720 μl ethanol and mix well by vortexing or pipetting. Proceed immediately to step 14.
    - Precipitates may be visible after addition of ethanol. This does not affect the procedure.
14. Transfer 700 μl of the sample, including any precipitate that may have formed, to an RNeasy MinElute spin column placed in a 2 ml collection tube (supplied). Close the lid gently, and centrifuge for 15 s at ≥8000 x g (≥10,000 rpm). Discard the flow-through.*
    - Reuse the collection tube in step 15.
15. Repeat step 14 until the entire sample has passed through the RNeasy MinElute spin column.
    - Reuse the collection tube in step 16.
16. Add 350 μl Buffer FRN to the RNeasy MinElute spin column. Close the lid gently, and centrifuge for 15 s at ≥8000 x g (≥10,000 rpm). Discard the flow-through.*
    - Reuse the collection tube in step 17.
17. Add 10 μl DNase I stock solution to 70 μl Buffer RDD. Mix by gently inverting the tube, and centrifuge briefly to collect residual liquid from the sides of the tube.
    - **Note:** DNase I is supplied lyophilized and should be reconstituted as described in “Preparing DNase I stock solution” (page 17).
    - **Note:** DNase I is especially sensitive to physical denaturation. Mixing should only be carried out by gently inverting the tube. Do not vortex.
18. Add the DNase I incubation mix (80 μl) directly to the RNeasy MinElute spin column membrane, and place on the benchtop (20–30°C) for 15 min.
    - Note: Be sure to add the DNase I incubation mix directly to the membrane. DNase digestion will be incomplete if part of the mix sticks to the walls or the O-ring of the spin column.
19. Add 500 μl Buffer FRN to the RNeasy MinElute spin column. Close the lid gently, and centrifuge for 15 s. **Save the flow-through for use in step 20.**
20. Place the spin column in a new 2 ml collection tube (supplied). Apply the flow-through from step 19 to the spin column. Close the lid gently, and centrifuge for 15 s. Discard the flow-through.
    - Reuse the collection tube in step 21.
21. Add 500 μl Buffer RPE to the spin column. Close the lid gently, and centrifuge for 15 s. Discard the flow-through.
    - Reuse the collection tube in step 22.
22. Add 500 μl Buffer RPE to the spin column. Close the lid gently, and centrifuge for 15 s. Discard the collection tube with the flow-through.
23. Place the spin column in a new 2 ml collection tube (supplied). Open the lid, and centrifuge at **full speed for 5 min**. Discard the collection tube with the flow- through.
    - To avoid damage to their lids, place the spin columns into the centrifuge with at least one empty position between columns. Orient the lids so that they point in a direction opposite to the rotation of the rotor (e.g., if the rotor rotates clockwise, orient the lids counterclockwise).
    - It is important to dry the spin column membrane, since residual ethanol may interfere with downstream reactions. Centrifugation with the lids open ensures that no ethanol is carried over during RNA elution.
24. Place the spin column in a new 1.5 ml collection tube (supplied). Add 14–30 μl RNase-free water directly to the spin column membrane. Close the lid gently, and incubate for 1 min at room temperature. Centrifuge at full speed for 1 min to elute the RNA.
    - Elution with smaller volumes of RNase-free water leads to higher total RNA concentrations, but lower RNA yields.
    - The dead volume of the spin column is 2 μl: elution with 14 μl RNase- free water results in a 12 μl eluate.
    - **I eluted with 30 μl RNase-free water**

### Purification of genomic DNA
25. Resuspend the pellet from step 9 in 180 μl Buffer ATL, add 40 μl proteinase K, and mix by vortexing.
    - The pellet should be *equilibrated to room temperature* prior to resuspension.
26. Incubate at 56°C for 1 h.
27. Incubate at 90°C for 2 h without agitation.
28. Briefly centrifuge the microcentrifuge tube to remove drops from the inside of the lid.
29. Add 200 μl Buffer AL, and mix thoroughly by vortexing. Then add 200 μl ethanol, and mix thoroughly again by vortexing or pipetting.
    - It is essential that the sample, Buffer AL, and ethanol are mixed immediately and thoroughly by vortexing or pipetting to yield a homogeneous solution. Buffer AL and ethanol can be premixed and added together in one step to save time when processing multiple samples.
    - A white precipitate may form on addition of Buffer AL and ethanol. This precipitate does not interfere with the AllPrep procedure.
30. Transfer the entire sample to a QIAamp MinElute spin column placed in a 2 ml collection tube (supplied). Close the lid gently, and centrifuge for 1 min at ≥8000 x g (≥10,000 rpm). Discard the collection tube with the flow-through.
    - If the sample has not completely passed through the membrane after centrifugation, centrifuge again at a higher speed until the spin column is empty.
31. Place the spin column in a new 2 ml collection tube (supplied). Add 700 μl Buffer AW1 to the spin column. Close the lid gently, and centrifuge for 15 s. Discard the flow- through. *
    - Reuse the collection tube in step 32.
32. Add 700 μl Buffer AW2 to the spin column. Close the lid gently, and centrifuge for 15 s. Discard the flow-through.
    - Reuse the collection tube in step 33.
33. Add 700 μl ethanol (96–100%) to the spin column. Close the lid gently, and centrifuge for 15 s. Discard the collection tube with the flow-through.
34. Place the spin column in a new 2 ml collection tube (supplied). Open the lid of the spin column, and centrifuge at **full speed for 5 min**. Discard the collection tube with the flow-through.
35. Place the spin column in a new 1.5 ml collection tube (supplied). Add 30–100 μl Buffer ATE directly to the spin column membrane. Close the lid gently, and incubate for 1 min at room temperature. Centrifuge at full speed for 1 min to elute the DNA.
    - Incubating the spin column loaded with Buffer ATE for 5 min at room temperature before centrifugation can increase DNA yield.

## Quality Control (QC)

These steps analyze the quantity and quality of the DNA/RNA extracted.

### RNA/DNA Quantity  

Follow Broad Range dsDNA and RNA Qubit [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/) to analyze sample **quantity**. Read standards once and record values, read all samples twice.

## RNA Quality

Proceed to this step if RNA does not appear clean on the gel. If RNA quantity is sufficient follow the Tape Station [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/RNA-TapeStation-Protocol/) to determine RNA quality and obtain a RNA Integrity Number (RIN). "Good" RNA should have a RIN above 8.0 and form two distinct peaks at the 18S and 28S locations.

### DNA Quality  

If DNA quantity is sufficient (typically >10 ng/µL) follow the PPP Agarose Gel [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Gel-Protocol/) to determine DNA quality. "Good" DNA should form a distinct band a the very top of the gel. You can also run a DNA Tapestation, following roughly the same protocol as above.

## Test 1/25/24

### Sectioning performed on 10/23/23 and LCM on 10/24/23. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-LCM/)

#### Qubit Results

- Used Broad range RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

RNA Standards: 370.23 (S1) & 9494.15 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| Qiagen_Low_Input   |  nd   |  nd    |   nd       |
| Qiagen_High_Input  |  10.4   |  10.6     |   10.5       |

DNA Standards: 190.84 (S1) & 19325.18 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| Qiagen_Low_Input   |  nd   |  nd    |   nd       |
| Qiagen_High_Input  |  nd   |  nd    |   nd       |

#### RNA Quality Check: Tapestation

![2024-01-25_Qiagen.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-01-25_Qiagen.JPG?raw=true)

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-01-25.pdf)

### This didn't work at all!