---
layout: post
title: 2026-04-29 LCM RNA Microprep Extraction Tests, Cryosectioned tissue
date: '2026-04-29'
categories: Processing, Protocols
tags: [Pocillopora, Porites, Montipora, RNA, Protocol]
---

- [Extracting RNA from PAXgene fixed tissue - cryosectioned scrolls](#extracting-rna-from-paxgene-fixed-tissue---cryosectioned-scrolls)
  - [Materials and Equipment](#materials-and-equipment)
  - [First time opening kit: Reagent Preparation](#first-time-opening-kit-reagent-preparation)
  - [Sterilizing working area to maintain an RNAse-free environment](#sterilizing-working-area-to-maintain-an-rnase-free-environment)
  - [Extraction](#extraction)
- [Extraction Results, QC](#extraction-results-qc)
  - [RNA Quality Check: Tapestation](#rna-quality-check-tapestation)

## Extracting RNA from PAXgene fixed tissue - cryosectioned scrolls

Continued testing from first test of this kit for RNA QC [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qiagen-RNeasy-Test/) and [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qiagen-RNeasy-Test/), and [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qiagen-RNeasy-Decalc-Take2/), but now the the Zymo RNA Microprep instead of the Qiagen.

Procedure:

- Extraction protocol was modified from the standard RNeasy protocol for paxgene-fixed tissue sections in OCT
  - Modifications based on the protocol of the [Qiagen PAXgene Tissue RNA/miRNA Kit](https://www.qiagen.com/us/products/discovery-and-translational-research/dna-rna-purification/rna-purification/mirna/paxgene-tissue-rna-mirna-kit?catno=766134) ([handbook](https://www.qiagen.com/us/resources/resourcedetail?id=dfb265d3-a517-455c-92c5-b575aefded0f&lang=en) and [cryo-embedding specific modifications]([file:///Users/zoedellaert/Downloads/PX18%20Purification%20of%20total%20RNA%20from%20sections%20of%20PAXgene%20Tissue%20fixed%20cryo-embedded%20PFCE%20tissue.pdf](https://www.qiagen.com/us/resources/resourcedetail?id=b25bb5ef-dd86-4cb8-a0f3-ab54b1bf5d35&lang=en))) 
  - This protocol uses the Zymo Quick-DNA/RNA Microprep Plus kit with several adjustments, and is based off of many months of troubleshooting different extraction methods of LCM tissues. See the base Zymo DNA/RNA Microprep protocol [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Base_Zymo_Quick_DNA_RNA_Microprep_Plus_Booklet.pdf). I used the protocol of the PAXgene Tissue AllPrep RNA/DNA extraction [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Simultaneous_DNA_RNA.pdf) as inspiration for adjustments to the Zymo protocol.

### Materials and Equipment

- Zymo Quick-RNA Microprep [kit](https://files.zymoresearch.com/protocols/_r1050_r1051_quick-rna_microprep_kit.pdf?_gl=1*z4zz5q*_gcl_au*MTY5MDg1ODAwNi4xNzcxMjc1NDY5) 
- Zymo 2X Digestion [buffer](https://www.zymoresearch.com/products/2x-digestion-buffer?srsltid=AfmBOop0gp6GyCtXs4Qi-pCuDoVlobNYvJYh_SltuvPrhrdoHUBYU2dV)
- Tris-EDTA (TE) [1X buffer, pH 8.0](https://www.fishersci.com/shop/products/tris-edta-1x-solution-ph-8-0-molecular-biology-fisher-bioreagents-3/bp24731#?keyword=BP24731) for DNA elution
- Heating block capable of heating to 60ºC
- Centrifuge and rotor capable of spinning at 15,000 rcf
- Plastics: 3 1.5 mL microcentrifuge tubes per sample, several 1000 uL, 200 uL, and 20 uL pipette tips per sample.
- Agilent Tapestation Instrument and [High Sensitivity RNA](https://www.agilent.com/en/product/automated-electrophoresis/tapestation-systems/tapestation-rna-screentape-reagents/high-sensitivity-rna-screentape-analysis-228267) and  [Genomic DNA](https://www.agilent.com/en/product/automated-electrophoresis/tapestation-systems/tapestation-dna-screentape-reagents/genomic-dna-screentape-analysis-228261) Screentapes and reagents.
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

1. Make sure all buffers are prepared appropriately
2. Label tubes + clean bench
3. Prepare Zymo Proteinase K Digestion mix, 100 uL per sample (based on FFPE Section of protocol):
   1. 95 uL DNAse/RNAse free water
   2. 95 uL Zymo 2X Digestion Buffer
   3. 10 uL Proteinase K
4. Tissue prep steps (tissue scroll extraction protocol)
   1. Tubes were taken out of freezer on dry ice
   2. Using sterile, ice-cold forceps and a razor blade, carefully cut away excess OCT surrounding the tissue scroll
   so that mainly tissue (with minimal OCT) remains.
   3. With a wide-bore tip, add 100 uL of the Proteinase K digestion mix and gently mix tissue + OCT into the buffer
5. Incubate the tissue on a shaker–incubator for 15 min at 56°C and 1400 rpm
6. **Thaw an aliquot of DNase I from -20 ºC on ice**
7. Transfer entire volume to a 1.5 mL tube
8.  Spin at 9,000 rcf for 3.5 mins to pellet any debris, then move 95 uL of supernatant to new 1.5 mL tube.
9.  Add 190 uL RNA lysis buffer and mix well until clear
10. Add an equal volume of 100% ethanol (285 uL) and mix well
    1.  do not spin down or allow a precipitate to form
11. Transfer entire volume into RNA (IC) column and spin down, discard flow through
12. Wash column with 400 uL wash buffer and spin down, discard flow through
13. Prepare DNase treatment (5 uL DNase I with 35 uL DNA Digestion Buffer per sample) on ice
    1.  perform DNAse treatment (40 uL) as written:
        1.  apply 40 uL of the mixture directly to each filter
        2.  incubate at room temperature for 15 minutes
14. Add 400 uL RNA prep buffer and spin down, discard flow through
15. Add 700 uL RNA wash buffer and spin down, discard flow through
16. Add 400 uL RNA wash buffer and spin for 2 minutes at 15,000 rcf
17. Transfer column to labelled 1.5 mL tube and elute in 15 uL RNase/DNase-free water.
18. Allow filter to saturate by spinning at 100 rcf for 1 minute and then elute by spinning down at 12,000 rcf for 1 minute. 
19. Confirm all liquid has been eluted from the filter into the tube, and discard the filter column.
20. Immediately transfer RNA tubes to ice and perform QC (hsRNA tapestation using 2 uL RNA) as soon as possible.
    1.  I recommend doing the RNA tapestation before continuing with the DNA extraction
21. Store RNA at -80 ºC as quickly after the extraction as possible and limit freeze-thaw cycles.

## Extraction Results, QC

### RNA Quality Check: Tapestation
