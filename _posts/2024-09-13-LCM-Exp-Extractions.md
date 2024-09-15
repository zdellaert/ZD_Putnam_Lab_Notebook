---
layout: post
title: 2024-09-13 LCM Experiment Extractions
date: '2024-09-13'
categories: Processing
tags: [Pocillopora, LCM, LCM-Pilot, RNA, DNA]
---

## Extracting RNA and DNA from LCM-d Pocillopora for LCM Experiment

### Extraction protocol:

**Zoe write up exact extraction method from notebook**

#### RNA Quality Check: Tapestation

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


#### DNA Quantity Check: Qubit

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


#### DNA Quality Check: Tapestation

Nothing detected on Qubit. Likely nothing will be on a gel, so trying gDNA tapestation.

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
