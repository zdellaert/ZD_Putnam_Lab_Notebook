---
layout: post
title: 2026-05-08 LCM RNA Extraction Protocol
date: '2026-05-08'
categories: Protocols
tags: [Pocillopora, Porites, LCM, RNA, Protocol]
---

## Extracting RNA from LCM-d Porites or Pocillopora

## Extraction protocol:

This is an RNA-only version of my previously developed [LCM DNA/RNA extraction protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2024-09-13-LCM-Exp-Extractions.md). This protocol uses the Zymo Quick-RNA Microprep kit with several adjustments, and is based off of many months of troubleshooting different extraction methods of LCM tissues. See the base Zymo DNA/RNA Microprep protocol [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Base_Zymo_Quick_DNA_RNA_Microprep_Plus_Booklet.pdf). I used the protocol of the PAXgene Tissue AllPrep RNA/DNA extraction [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Simultaneous_DNA_RNA.pdf) as inspiration for adjustments to the Zymo protocol.

### Materials and Equipment

- Zymo Quick-RNA Microprep [kit](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf?_gl=1*z4zz5q*_gcl_au*MTY5MDg1ODAwNi4xNzcxMjc1NDY5) 
- Zymo 2X Digestion [buffer](https://www.zymoresearch.com/products/2x-digestion-buffer?srsltid=AfmBOop0gp6GyCtXs4Qi-pCuDoVlobNYvJYh_SltuvPrhrdoHUBYU2dV)
- Centrifuge and rotor capable of spinning at 15,000 rcf
- Plastics: 3 1.5 mL microcentrifuge tubes per sample, several 1000 uL, 200 uL, and 20 uL pipette tips per sample.
- Agilent Tapestation Instrument and [High Sensitivity RNA](https://www.agilent.com/en/product/automated-electrophoresis/tapestation-systems/tapestation-rna-screentape-reagents/high-sensitivity-rna-screentape-analysis-228267) Screentapes and reagents.
  - Or equivalent: Bioanalyzer, for example.

### First time opening kit: Reagent Preparation

1. Add 96 mL 100% ethanol to the 24 mL RNA Wash Buffer concentrate before use. Mark **clearly** on the bottle that Ethanol was added. Check kit contents and instructions to confirm prep steps.  
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
5. **Thaw an aliquot of DNase I from -20 ºC on ice**
6. Transfer entire volume to a 1.5 mL tube
7. Spin at 9,000 rcf for 3.5 mins to pellet any debris, then move 95 uL of supernatant to new 1.5 mL tube.
8. Add 190 uL RNA lysis buffer and mix well until clear
9. Add an equal volume of 100% ethanol (285 uL) and mix well
    1.  do not spin down or allow a precipitate to form
10. Transfer entire volume into RNA (IC) column
11. Spin column at 15,000 rcf for 30s, discard flow-through
    1.  ***All spins, unless noted, were performed at 15,000 rcf for 30s***
12. Wash column with _400 uL wash buffer_ and spin down, discard flow through
13. Prepare DNase treatment (5 uL DNase I with 35 uL DNA Digestion Buffer per sample) on ice
    1.  perform DNAse treatment (40 uL) as written:
        1.  _apply 40 uL_ of the mixture directly to each filter
        2.  incubate at room temperature for 15 minutes
14. Add _400 uL prep buffer_ and spin down, discard flow through
15. Add _700 uL wash buffer_ and spin down, discard flow through
16. Add _400 uL wash buffer_ and spin for 2 minutes at 15,000 rcf
17. Transfer column to labelled 1.5 mL tube and elute in 15 uL RNase/DNase-free water.
18. Allow filter to saturate by spinning at 100 rcf for 1 minute and then elute by spinning down at 12,000 rcf for 1 minute. 
19. Confirm all liquid has been eluted from the filter into the tube, and discard the filter column.
20. Immediately transfer RNA tubes to ice and perform QC (hsRNA tapestation using 2 uL RNA) as soon as possible.
    1.  I recommend doing the RNA tapestation before continuing with the DNA extraction
21. Store RNA at -80 ºC as quickly after the extraction as possible and limit freeze-thaw cycles.

### Quality Control (QC)

Typically, my LCM extractions have not been detectable with high sensitivity RNA Qubit. Therefore, to preserve as much material as possible, I recommend only running the High Sensitvity RNA Tapestation and not qubit or gel. Follow the Tape Station [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/RNA-TapeStation-Protocol/).

Quick reference: 
1. For each sample, pipette **1 µL High Sensitivity RNA Sample Buffer** and **2 µL RNA sample** in a tube strip
2. Apply caps to tube strips.
3. Mix liquids using the IKA MS3 vortexer at 2000 rpm for 1 min.
4. Spin down samples and ladder for 1 min.
5. Samples and ladder denaturation:
   1. Heat samples and ladder at 72 °C (162 °F) for 3 min.
   2. Place samples and ladder on ice for 2 min.
   3. Spin down sample and ladder for 1 min.

- For RNA, I have been using the High Sensitvity RNA kit to determine RNA quantity, quality, RNA Integrity Number (RIN), and DV200.
  - The RNA is going to be at least a little degraded, and will be difficult to detect simply because of the low volume. 
  - However, I have had success with achieving faint 16S/18S bands and concentrations generally around 0.3 ng/uL, which has been good enough for the low-input RNA library prep kit I am using.
  - [DV200 values](https://www.agilent.com/en/promotions/tapestation-dv200-determination) are a metric of RNA integrity for degraded RNA, and a DV200 of ~60% or higher is generally a good sign that there is RNA in the sample that is usable.