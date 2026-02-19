---
layout: post
title: 2026-02-19 Qiagen RNeasy Extraction Tests, PAXgene fixed tissue at various stages of decalcification
date: '2026-02-19'
categories: Processing, Protocols
tags: [Pocillopora, Porites, RNA, Protocol]
---

## Extracting RNA from PAXgene fixed tissue at various stages of decalcification

### Protocol: Qiagen RNeasy Kit

Continued testing from first test of this kit for RNA QC [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qiagen-RNeasy-Test/)

Notes:
- β-Mercaptoethanol (β-ME) must be added to Buffer RLT before use. Add 10 µl β-ME per 1 ml Buffer RLT. Dispense in a fume hood and wear appropriate protective clothing.
- Buffer RPE is supplied as a concentrate. Before using for the first time, add 4 volumes of ethanol (96–100%) as indicated on the bottle to obtain a working solution.

Procedure:

1. Make sure all buffers are prepared appropriately
2. Label tubes + clean bench
3. Tissue prep steps
   1. **For [PAXgene-fixed tissues in PAXgene stabilizer](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Tissue_RNA_miRNA_Kit.pdf):**
      1. Place tissue in 500 µl Buffer RLT with BME added (500 + 5 uL) with 5 mm of beads
      2. Bead beat for 2 mins
      3. For **non-Pro-K digested samples** (testing 1/2 and 1/2)
         1. Spin down briefly on mini centrifuge and proceed to step 4
      4. For **Pro-K digested samples** (testing 1/2 and 1/2)
         1. Add 960 µl RNase-free water to cell lysate suspension. Then add 40 µl Proteinase K and mix by vortexing for 5 s.
         2. Incubate at 45 ºC for 15 min at 1400 rpm
      5. Proceed to step 4
4. Transfer 400 uL to a new 1.5 mL tube and **Centrifuge the lysate for 3 min at full speed**.
5. Carefully *remove **350 uL** of the supernatant* by pipetting, and transfer it to a new 1.5 mL tube
   1. Remove as much as you can without disturbing pellet, use same volume of ethanol in next step
6. Add **1 volume of 70% ethanol*** to the cleared lysate, and mix immediately by pipetting.
7. Transfer up to 700 µl of the sample to an **RNeasy spin column** placed in a 2 ml collection tube (supplied).
   1. Close the lid gently, and centrifuge for **30 s at 15,000 rcf**. Discard the flow-through.
   2. If the sample volume exceeds 700 µl, centrifuge successive aliquots in the same RNeasy spin column. Discard the flow-through after each centrifugation.
8. Add **700 µl Buffer RW1** to the RNeasy spin column.
   1. Close the lid gently, and centrifuge for **30 s at 15,000 rcf** to wash the spin column membrane. Discard the flow-through.
9.  Add **500 µl Buffer RPE** to the RNeasy spin column.
   1. Close the lid gently, and centrifuge for **30 s at 15,000 rcf** to wash the spin column membrane. Discard the flow-through.
10. Add **500 µl Buffer RPE** to the RNeasy spin column.
    1.  Close the lid gently, and centrifuge for **1 min at 15,000 rcf** to wash + dry the spin column membrane.
11. Place the RNeasy spin column in a new 2 ml collection **tube** (supplied), and discard the old collection tube with the flow-through.
    1.  Close the lid gently, and centrifuge at **full speed for 2 min**.
12. Place the RNeasy spin column in a new 1.5 ml collection tube (supplied)
13. Add **50 µl RNAse-free** water directly to the spin column membrane. Close the lid gently, and centrifuge for **1 min at 12,000 rcf** to elute the RNA.
14. If higher concentration is desired, re-apply this eluate to the filter membrane and repeat the centrifuge step.

### RNA Quality Check: Tapestation

![2024-09-13-rna](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-19.png?raw=true)

| sample_id      | concentration             | RIN |
|----------------|---------------------------|-----|
| POC_1          |  96.9 ng/uL         | 9.1 |
| POC_1_ProK     |  91.6 ng/uL         | 8.4 |
| POR_1          |  44.9 ng/uL         | 8.5 |
| POR_1_ProK     |  40.8 ng/uL         | 8.3 |
| MON_1          |  144 ng/uL         | 8.5 |
| MON_1_ProK     |  168 ng/uL         | 5.8 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-19.pdf)
