---
layout: post
title: 2026-02-13 Qiagen RNeasy Extraction Tests, PAXgene fixed tissue vs. Embedded tissue vs. Fresh Tissue
date: '2026-02-13'
categories: Processing, Protocols
tags: [Pocillopora, Porites, RNA, Protocol]
---

## Extracting RNA from PAXgene fixed tissue, PAXgene fixed & Embedded Tissue, and Fresh Tissue

### Protocol: Qiagen RNeasy Kit

Notes:
- β-Mercaptoethanol (β-ME) must be added to Buffer RLT before use. Add 10 µl β-ME per 1 ml Buffer RLT. Dispense in a fume hood and wear appropriate protective clothing.
- Buffer RPE is supplied as a concentrate. Before using for the first time, add 4 volumes of ethanol (96–100%) as indicated on the bottle to obtain a working solution.

Procedure:

1. Make sure all buffers are prepared appropriately
2. Label tubes + clean bench
3. Tissue prep steps
   1. **For fresh or fresh-frozen tissue**
      1. Place tissue in up to 600 µl Buffer RLT with BME added (600 + 6 uL)
      2. Disrupt the tissue and homogenize the lysate in Buffer RLT
         1. I am going to try normal bead-beating like we do for the DNA/RNA shield samples
         2. Alternatives: tissue lyser, rotor-star homogenizer
   2. **For [cryosections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_RNA_PFCE_sections.pdf):**
      1. Pre-cool tube with 150 uL buffer RLT (with BME = 150 + 1.5 uL) + 290 uL water + 10 uL ProK
         1. Final vol = 450
      2. Add 1-3 cryosections + vortex to mix
      3. Incubate at 56 ºC for 15 min at 1400 rpm
      4. Proceed to step 4
         1. potential use of **qiashredder** here or other method such as bead-beating to **homogenize** completely
   3. **For [PAXgene-fixed tissues in PAXgene stabilizer](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Tissue_RNA_miRNA_Kit.pdf):**
      1. Place tissue in 250 µl Buffer RLT with BME added (250 + 1.5 uL)
      2. Disrupt the tissue and homogenize the lysate in Buffer RLT
         1. I am going to try normal bead-beating like we do for the DNA/RNA shield samples
         2. Alternatives: tissue lyser, rotor-star homogenizer
      3. Add 480 µl RNase-free water to cell lysate suspension. Then add 20 µl Proteinase K and mix by vortexing for 5 s.
         1. Final vol = 750
      4. Incubate at 45 ºC for 15 min at 1400 rpm
      4. Proceed to step 4
4. **Centrifuge the lysate for 3 min at full speed**.
   1. Carefully *remove the supernatant* by pipetting, and transfer it to a new microcentrifuge tube (not supplied). Use only this supernatant (lysate) in subsequent steps.
5. Add **1 volume of 70% ethanol*** to the cleared lysate, and mix immediately by pipetting.
6. Transfer up to 700 µl of the sample to an **RNeasy spin column** placed in a 2 ml collection tube (supplied).
   1. Close the lid gently, and centrifuge for **15 s at ≥8000 x g** (≥10,000 rpm). Discard the flow-through.
   2. Reuse the collection tube in step 7.
   3. If the sample volume exceeds 700 µl, centrifuge successive aliquots in the same RNeasy spin column. Discard the flow-through after each centrifugation.
7. Add **700 µl Buffer RW1** to the RNeasy spin column.
   1. Close the lid gently, and centrifuge for **15 s at ≥8000 x g (≥10,000 rpm)** to wash the spin column membrane. Discard the flow-through.
   2. Reuse the collection tube in step 8.
8. Add **500 µl Buffer RPE** to the RNeasy spin column.
   1. Close the lid gently, and centrifuge for **15 s at ≥8000 x g (≥10,000 rpm)** to wash the spin column membrane. Discard the flow-through.
   2. Reuse the collection tube in step 9.
   3. *Note: Buffer RPE is supplied as a concentrate. Ensure that ethanol is added to Buffer RPE before use (see “Things to do before starting”).*
9.  Add **500 µl Buffer RPE** to the RNeasy spin column.
    1.  Close the lid gently, and centrifuge for **2 min at ≥8000 x g** (≥10,000 rpm) to wash + dry the spin column membrane.
10. Place the RNeasy spin column in a new 2 ml collection **tube** (supplied), and discard the old collection tube with the flow-through.
    1.  Close the lid gently, and centrifuge at **full speed for 1 min**.
11. Place the RNeasy spin column in a new 1.5 ml collection tube (supplied). Add **30–50 µl RNAse-free** water directly to the spin column membrane. Close the lid gently, and centrifuge for **1 min at ≥8000 x g** (≥10,000 rpm) to elute the RNA.

### RNA Quality Check: Tapestation

Have not been runnning RNA Qubit's because I never detect anything from these super low concentrations.

![2024-09-13-rna](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-13.png?raw=true)

| sample_id      | concentration             | RIN |
|----------------|---------------------------|-----|
| POC - PAXgene Fixed, Decalcified, Cryoembedded   |  275 ng/uL         | 3.6 |
| POR - PAXgene Fixed, Decalcified, Cryoembedded   |  208 ng/uL         | 3.9 |
| POC - PAXgene Fixed, Not Decalcified             |  362 ng/uL         | 6.5 |
| POR - PAXgene Fixed, Not Decalcified             |  112 ng/uL         | 8.3 |
| POC - Fresh tissue                               |  120 ng/uL         | 9.5 |
| POR - Fresh tissue                               |  86.7 ng/uL        | 9.6 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-13.pdf)