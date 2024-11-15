---
layout: post
title: 2024-09-13 LCM Experiment Extractions
date: '2024-09-13'
categories: Processing, Protocols
tags: [Pocillopora, LCM, LCM-Pilot, RNA, DNA, Protocol]
---

## Extracting RNA and DNA from LCM-d Pocillopora for LCM Experiment

## Extraction protocol:

This protocol uses the Zymo Quick-DNA/RNA Microprep Plus kit with several adjustments, and is based off of many months of troubleshooting different extraction methods of LCM tissues. See the base Zymo DNA/RNA Microprep protocol [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Base_Zymo_Quick_DNA_RNA_Microprep_Plus_Booklet.pdf).

### Materials and Equipment

- Zymo Quick-DNA/RNA Microprep Plus [kit](https://www.zymoresearch.com/products/quick-dna-rna-microprep-plus-kit) 
- Zymo 2X Digestion [buffer](https://www.zymoresearch.com/products/2x-digestion-buffer?srsltid=AfmBOop0gp6GyCtXs4Qi-pCuDoVlobNYvJYh_SltuvPrhrdoHUBYU2dV)
- Tris-EDTA (TE) [1X buffer, pH 8.0](https://www.fishersci.com/shop/products/tris-edta-1x-solution-ph-8-0-molecular-biology-fisher-bioreagents-3/bp24731#?keyword=BP24731) for DNA elution
- Heating block capable of heating to 60ºC
- Centrifuge and rotor capable of spinning at 15,000 rcf
- Plastics: 5 1.5 mL microcentrifuge tubes per sample, several 1000 uL, 200 uL, and 20 uL pipette tips per sample.
- Agilent Tapestation Instrument and [High Sensitivity RNA](https://www.agilent.com/en/product/automated-electrophoresis/tapestation-systems/tapestation-rna-screentape-reagents/high-sensitivity-rna-screentape-analysis-228267) and  [Genomic DNA](https://www.agilent.com/en/product/automated-electrophoresis/tapestation-systems/tapestation-dna-screentape-reagents/genomic-dna-screentape-analysis-228261) Screentapes and reagents.
  - Or equivalent: Bioanalyzer, for example.

### First time opening kit: Reagent Preparation

1. Add 96 mL 100% ethanol to the 24 mL DNA/RNA Wash Buffer concentrate before use. Mark **clearly** on the bottle that Ethanol was added. Check kit contents and instructions to confirm prep steps.  
2. Reconstitute the lyophilized (freeze-dried) DNase I as indicated on the vial prior to use. For 250U of DNAse I, add 275 uL of DNAse/RNAse free water (provided). For 50U of DNAse I, add 55 uL of DNAse/RNAse free water (provided). Mix by **gentle** inversion. Check kit contents and instructions to confirm prep steps. Separate into 3-4 aliquots to minimize freeze-thaw and store at -20 ºC.
3. Reconstitute the lyophilized (freeze-dried) Proteinase K as indicated on the vial prior to use. For 5 mg Proteinase K, add 260 uL Proteinase K Storage Buffer. For 5 mg Proteinase K, add 260 uL Proteinase K Storage Buffer. Mix by vortexing. Check kit contents and instructions to confirm prep steps. Store tube at -20 ºC.

### Sterilizing working area to maintain an RNAse-free environment

Clean bench with clean paper towels (spray solution, wipe down) in the following order:

  1. 10% bleach solution  
  2. DI water  
  3. 70% ethanol
  4. RNase cleaner (spray bottle)

Clean pipettes, tip boxes, and the controls on the heating block and centrifuge by squirting 70% ethanol on a paper towel and wiping them down. Repeat with RNAse cleaner. Wipe down gloves with 70% ethanol and RNAse cleaner. Do not spray solutions directly on the equipment.

### Extraction

**For all steps where flow-through was discarded, I pipetted the flow-through from the collection tube into a beaker instead of pouring it out to minimize any contamination of the filter or carryover of wash buffers**

1. Thaw LCM-dissection tubes from -80 ºC on ice.
2. As samples thaw, prepare Zymo Proteinase K Digestion mix, 60 uL per sample (based on FFPE Section of protocol):
   1. 95 uL DNAse/RNAse free water
   2. 95 uL Zymo 2X Digestion Buffer
   3. 10 uL Proteinase K
   - ***Note:*** this is the same buffer mix the dissected tissues were collected in
3. Once samples are thawed, add 60 uL of the digestion buffer and pipette up and down to mix
4. Incubate at room temperature for 15 mins
5. Transfer entire volume to a 1.5 mL tube
6. Spin at 9,000 rcf for 3.5 mins to pellet any debris, then move 95 uL of supernatant to new 1.5 mL tube.
7. Add 190 uL lysis buffer and mix well until clear, then move whole volume into IC-XM column.
8. ***All spins, unless noted, were performed at 15,000 rcf for 30s***
9.  Spin IC-XM column, move column to a new collection tube and move flow-though to a labelled 1.5 mL tube
10. While proceeding with RNA extraction, place DNA (IC-XM) columns in collection tubes at 4 ºC

#### RNA Extraction

11. Thaw an aliquot of DNase I from -20 ºC on ice
12. Combine the flow-through from step 9 with an equal volume of 100% ethanol (285 uL) and mix well
    1.  do not spin down or allow a precipitate to from
13. Transfer entire volume into RNA (IC) column and spin down, discard flow through
14. Wash column with 400 uL wash buffer and spin down, discard flow through
15. Prepare DNase treatment (5 uL DNase I with 35 uL DNA Digestion Buffer per sample) on ice
    1.  perform DNAse treatment (40 uL) as written:
        1.  apply 40 uL of the mixture directly to each filter
        2.  incubate at room temperature for 15 minutes
16. Add 400 uL DNA/RNA prep buffer and spin down, discard flow through
17. Add 700 uL wash buffer and spin down, discard flow through
18. Add 400 uL wash buffer and spin for 2 minutes at 15,000 rcf
19. Transfer column to labelled 1.5 mL tube and elute in 15 uL RNase/DNase-free water.
20. Allow filter to saturate by spinning at 100 rcf for 2 minutes and then elute by spinning down at 12,000 rcf for 1 minute. 
21. Confirm all liquid has been eluted from the filter into the tube, and discard the filter column.
22. Immediately transfer RNA tubes to ice and perform QC (hsRNA tapestation using 2 uL RNA) as soon as possible.
    1.  I recommend doing the RNA tapestation before continuing with the DNA extraction
23. Store RNA at -80 ºC as quickly after the extraction as possible and limit freeze-thaw cycles.

#### DNA Extraction

**I have tested an on-column proteinase K digestion based on the DNase I digestions used in the RNA extraction. This method is not supported by Zymo, but has worked for me to increase yield of DNA while not over-digesting and degrading the RNA. This was inspired by the PAXgene RNA/DNA concurrent extraction protocol [here]()**

22. Remove DNA columns from 4 ºC and allow to equilibrate to room temperature for 5-10 minutes
23. Thaw Proteinase K from -20 ºC 
24. Wash column with 400 uL wash buffer and spin down, discard flow through
25. Prepare Proteinase K treatment (15 uL Proteinase K with 30 uL PK Digestion Buffer per sample)
    1.  Apply 45 uL of the mixture directly to each filter
    2.  Incubate at room temperature for 30 minutes
26. Warm RNase/DNase-free Tris-EDTA to 60 ºC on heating block.
27. Add 400 uL DNA/RNA prep buffer and spin down, discard flow through
28. Add 700 uL wash buffer and spin down, discard flow through
29. Add 400 uL wash buffer and spin for 2 minutes at 15,000 rcf
30. Transfer column to labelled 1.5 mL tube and apply 20 uL warmed Tris-EDTA to filter
31. Let sit for 3 minutes at room temperature.
32. Allow filter to saturate by spinning at 100 rcf for 2 minutes and then elute by spinning down at 12,000 rcf for 1 minute. 
33. Confirm all liquid has been eluted from the filter into the tube, and discard the filter column.
34. Immediately transfer DNA to ice and perform QC (gDNA tapestation using 1 uL DNA) as soon as possible.
35. Store DNA at -20 ºC as quickly after the extraction as possible and limit freeze-thaw cycles.

### Quality Control (QC)

Typically, my LCM extractions have not been detectable with high sensitivity RNA or dsDNA Qubit. Therefore, to preserve as much material as possible, I recommend only running Tape Stations to assess quality and quantity of DNA and RNA. Follow the Tape Station [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/RNA-TapeStation-Protocol/).

- For RNA, I have been using the High Sensitvity RNA kit to determine RNA quantity, quality, RNA Integrity Number (RIN), and DV200.
  - The RNA is going to be at least a little degraded, and will be difficult to detect simply because of the low volume. 
  - However, I have had success with achieving faint 16S/18S bands and concentrations generally around 0.3 ng/uL, which has been good enough for the low-input RNA library prep kit I am using.
  - [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination) are a metric of RNA integrity for degraded RNA, and a DV200 of ~60% or higher is generally a good sign that there is RNA in the sample that is usable.
- For DNA, I have been using the gDNA kit to determine DNA quantity, quality, DNA Integrity Number (DIN). 
  - The gDNA is also degraded most of the time from these samples, but a faint gDNA band is present around 10,000bp. I have usually been getting a DIN around 2-3, which is low, but hopefully usable.

## Extraction Results, QC

### RNA Quality Check: Tapestation

Have not been runnning RNA Qubit's because I never detect anything from these super low concentrations.

![2024-09-13-rna](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-13-rna.png?raw=true)

Tapestation concentrations and [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination):

| sample_id      | concentration             | RIN | DV200  | 
|----------------|---------------------------|-----|--------|
| #4 (Frag A)    |  333 pg/uL (0.333 ng/uL)  |   - | 59.70% |
| #5 (Frag A)    |  271 pg/uL (0.271 ng/uL)  |   - | 61.63% |
| #8 (Frag B)    |  246 pg/uL (0.246 ng/uL)  |   - | 67.53% |
| #9 (Frag B)    |  288 pg/uL (0.288 ng/uL)  |   - | 63.35% |
| #15 (Frag C)   |  275 pg/uL (0.275 ng/uL)  |   - | 59.40% |
| #16 (Frag C)   |  263 pg/uL (0.263 ng/uL)  |   - | 66.72% |
| #20 (Frag D)   |  272 pg/uL (0.272 ng/uL)  |   - | 66.19% |
| #21 (Frag D)   |  339 pg/uL (0.339 ng/uL)  |   - | 60.31% |
| #26 (Frag E)   |  283 pg/uL (0.283 ng/uL)  |   - | 61.44% |
| #27 (Frag E)   |  211 pg/uL (0.211 ng/uL)  |   - | 72.20% |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-13-rna.pdf) and [here (with manually annotated peaks and dv200 values)](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-13-rna-editpeaks-dv200.pdf)

Traces per sample:

![TS_RNA_4](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_4.png?raw=true)

![TS_RNA_5](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_5.png?raw=true)

![TS_RNA_8](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_8.png?raw=true)

![TS_RNA_9](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_9.png?raw=true)

![TS_RNA_15](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_15.png?raw=true)

![TS_RNA_16](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_16.png?raw=true)

![TS_RNA_20](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_20.png?raw=true)

![TS_RNA_21](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_21.png?raw=true)

![TS_RNA_26](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_26.png?raw=true)

![TS_RNA_27](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/LCM_Pilot_Extractions/TS_RNA_27.png?raw=true)


### DNA Quantity Check: Qubit

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards:  (S1) &  (S2)

| colony_id                      | DNA_QBIT_1 | DNA_QBIT_2 |   DNA_QBIT_3      | DNA_QBIT_AVG |
|--------------------------------|------------|------------|-------------------|--------------|
| #4 (Frag A)    | nd  | nd | nd |  nd |
| #5 (Frag A)    | nd  | nd | nd |  nd |
| #8 (Frag B)    | nd  | nd | nd |  nd |
| #9 (Frag B)    |  nd  | nd | nd |  nd |
| #15 (Frag C)   |   nd  | nd | nd |  nd |
| #16 (Frag C)   |  nd  | nd | nd |  nd |
| #20 (Frag D)   |   nd  | nd | nd |  nd |
| #21 (Frag D)   | nd  | nd | nd |  nd |
| #26 (Frag E)   | nd  | nd | nd |  nd |
| #27 (Frag E)   |  nd  | nd | nd |  nd |

Hmm.

### DNA Quality Check: Tapestation

Nothing detected on Qubit. Likely nothing will be on a gel, so trying gDNA tapestation. The gDNA is degraded , but a faint gDNA band is present around 10,000bp. DIN is low, but hopefully usable. Not sure how much stake to put in these concentrations.

![2024-09-13-gDNA.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-13-gDNA.png?raw=true)

Tapestation concentrations:

| sample_id      | concentration | DIN | 
|----------------|------------|------------|
| #4 (Frag A)    |  4.86 ng/uL  | 2.8 | 
| #5 (Frag A)    |  5.01 ng/uL  | 2.8 | 
| #8 (Frag B)    |  4.46 ng/uL  | 3.3 | 
| #9 (Frag B)    |  4.37 ng/uL  | 3.1 | 
| #15 (Frag C)   |  3.80 ng/uL  | 2.4 | 
| #16 (Frag C)   |  3.43 ng/uL  | 2.5 | 
| #20 (Frag D)   |  3.37 ng/uL  | 2.3 | 
| #21 (Frag D)   |  4.41 ng/uL  | 2.8 | 
| #26 (Frag E)   |  2.75 ng/uL  | - | 
| #27 (Frag E)   |  1.96 ng/uL  | - | 


Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-09-13-gDNA.pdf)

### DNA Quantity Check: Qubit, Again, using 5 uL input of DNA instead of 2 uL

- Used High Sensitivity DNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 69.09 (S1) & 23183.35 (S2)

| colony_id                      | DNA_QBIT_1 | DNA_QBIT_2 |   DNA_QBIT_3      | DNA_QBIT_AVG |
|--------------------------------|------------|------------|-------------------|--------------|
| #4 (Frag A)    | nd  | nd | nd |  nd |
| #5 (Frag A)    | nd  | nd | nd |  nd |
| #8 (Frag B)    | nd  | nd | nd |  nd |
| #9 (Frag B)    |  nd  | nd | nd |  nd |
| #15 (Frag C)   |   0.0284  | 0.0292 | 0.0288 |  0.0288 |
| #16 (Frag C)   |  nd  | nd | nd |  nd |
| #20 (Frag D)   |   0.0296  | 0.0332 | 0.0256 |  0.0295 |
| #21 (Frag D)   | 0.0228  | nd | nd |  0.0228 |
| #26 (Frag E)   | nd  | nd | nd |  nd |
| #27 (Frag E)   |  nd  | nd | nd |  nd |

Still not great. Will use tapestation values for Library Prep calculations.
