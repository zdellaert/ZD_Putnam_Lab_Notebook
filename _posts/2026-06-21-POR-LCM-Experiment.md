---
layout: post
title: 2026-06-10 Porites Time Series LCM Experiment
date: '2026-06-10'
categories: Processing
tags: [Porites, LCM, RNA]
---

## Porites Time Series LCM

**Goal:** *[Laser capture microdissection (LCM) RNA‑seq](https://www.biorxiv.org/content/10.64898/2026.03.13.711677v2)* of oral epidermis (OE) and oral gastrodermis (OG) across a heat stress time series in *Porites compressa* (2 time points x 2 treatments x 3 replicates × 2 tissues = 24 target LCM RNA‑seq libraries).

**Current status of project:** on hold until August 2026

- Sectioning + LCM dissections for the 12 *Porites* samples is done.
- RNA extraction and library prep are **partially complete** and currently paused due to low RNA integrity for majority of samples extracted so far and low cDNA yield compared to pilot tests
- I will revisit extractions and library prep at a future date (August 2026)

---

## Sectioning + LCM Protocol

### Core protocols

- Tissue processing: [Fixing + cryoembedding tissue Protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2025-09-10-PFCE-Protocol.md)
- Sectioning + Microdissection: [LCM Protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-25-LCM-Protocol.md)
- RNA Extraction: [Zymo RNA Microprep Protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-05-08-LCM-RNA-Microprep.md)
- Library Prep: [NEBNext® Single Cell/Low Input RNA Library Prep Kit](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-24-LCM-TS-Low-Input-RNA-Library-Prep.md)

#### For log of all recent (2026) troubleshooting and protocol optimization for this project, see this post: [Troubleshooting Laser Capture Microdissection of *Porites compressa*](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-27-LCM-Porites-Troubleshooting.md)

See older github posts for 2023-2024 LCM protocol development (e.g. [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2023-10-16-Testing-LCM.md)).

### Exact slide prep staining protocol:

I followed a modified LCM slide prep protocol for the time series samples based on [troubleshooting](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-27-LCM-Porites-Troubleshooting.md). I had a lot of issues getting the *Porites* tissue, especially the most delicate oral epidermis layer (which we really cared about for this project) to stick to the PEN membrane slides. Therefore, for these samples we decided to not use a cresyl violet stain to minimize risk of delicate tissue layers (less washing = less loss). However, we still need to remove some of the OCT embedding material from the slide.

1. Bring slide up to room temperature, slowly to avoid formation of water condensation inside the container.
   1. 30 minutes at -20 ºC
   2. 30 minutes at 4°C
   3. 15 minutes at room temp
2. Balance slide on rim of glass petri dish; on tube rack over dry ice (not immediately on the dry ice otherwise the 70% ethanol can freeze)
3. Cover with ice-cold 75% ethanol to remove excess OCT, 2 minutes
4. Replace with fresh ice-cold 75% ethanol, 2 minutes
5. Cover with ice-cold 96% ethanol, 10 s
6. Cover with ice-cold 100% ethanol, 10 s
7. Rinse back of slide with 100% ethanol, 10s
8. Then cover slide with ice-cold 100% ethanol for 1 minute to fully dry tissue and remove any excess water
9. Air dry sample 4 mins in drying chamber with desiccant and then transport slide in falcon tube with silica packet

---

## LCM summary for time‑series slides (June 2026)

- Species: *Porites compressa*
- Time series experiment fragments:
  - 3 hours heat: POR_R3_H1, POR_R3_H2, POR_R3_H3
  - 3 hours control: POR_R3_C1, POR_R3_C2, POR_R3_C3
  - 72 hours heat: POR_R72_H1, POR_R72_H2, POR_R72_H3
  - 72 hours control: POR_R72_C1, POR_R72_C2, POR_R72_C3
- Target LCM dissections:
  - Oral epidermis (OE) and oral gastrodermis (OG) from each fragment (12 fragments × 2 tissues = 24 planned libraries).
  - Additional “bulk host” and “bulk sym” dissections of "chunky" bits of tissue were performed for some slides, mainly for RNA extraction testing backups

Full metadata and log are in my [POR Time Series LCM spreadsheet](https://docs.google.com/spreadsheets/d/1GEzJbSuiYyj9dCYJHMrmUE7KyFpycERAgJ84FO_ysR8/edit?usp=sharing)

| LCM Date | Sample     | Tube | Section | Number dissections | Tissue            | Number of Real OE/OG Sets per Sample | Notes | Total Dissection Area | Approx Tissue Area, quick measurements -- in progress | Approx Tissue Area / 40 (approx # cells) |
|----------|------------|------|---------|--------------------|-------------------|--------------------------------------|-------------------------|-----------------------|-------------------------------------------------------|------------------------------------------|
| 20260616 | POR_R72_C3 | 310  | 5       | 1 | oral epidermis    | 1 | kinda abandoned these   | 56,998                | |      |
| 20260616 | POR_R72_C3 | 311  | 5       | 1 | oral gastrodermis | 1 | kinda abandoned these   | 48,587                | |      |
| 20260616 | POR_R72_C3 | 312  | 6       | 7| oral epidermis    | 1 |       | 315,056               | |      |
| 20260616 | POR_R72_C3 | 313  | 6       | 7| oral gastrodermis | 1 |       | 302,037               | |      |
| 20260616 | POR_R72_C3 | 314  | 1       | 7| bulk_host         | 1 |       | 189,141               | |      |
| 20260616 | POR_R72_C3 | 315  | 1       | 7| bulk_sym          | 1 |       | 84,036                | |      |
| 20260616 | POR_R3_C2  | 317  | 6       | 6| oral epidermis    | 1 |       | 249,919               | |      |
| 20260616 | POR_R3_C2  | 318  | 6       | 5| oral gastrodermis | 1 |       | 109,213               | |      |
| 20260616 | POR_R3_C2  | 319  | 3       | 3 | bulk_host         | 1 |       | 194,779               | |      |
| 20260616 | POR_R3_C2  | 320  | 3       | 3 | bulk_sym          | 1 |       | 96,483                | |      |
| 20260617 | POR_R72_H3 | 321  | 4       | 7| oral epidermis    | 1 |       | 161,433               | |      |
| 20260617 | POR_R72_H3 | 322  | 4       | 6| oral gastrodermis | 1 |       | 138,936               | |      |
| 20260617 | POR_R72_H3 | 323  | 4       | 3 | bulk_host         | 1 |       | 175,607               | |      |
| 20260617 | POR_R72_H3 | 324  | 4       | 3 | bulk_sym          | 1 |       | 58,187                | |      |
| 20260617 | POR_R3_C1  | 325  | 3       | 6| oral epidermis    | 1 |       | 355,479               | 57,891            | 1447 |
| 20260617 | POR_R3_C1  | 326  | 3       | 6| oral gastrodermis | 1 |       | 245,932               | 53,541            | 1339 |
| 20260617 | POR_R3_C1  | 327  | 3       | 2 | bulk_host         | 1 |       | 111,548               | |      |
| 20260617 | POR_R3_C1  | 328  | 3       | 1 | bulk_sym          | 1 |       | 40,435                | |      |
| 20260617 | POR_R3_C1  | 329  | 1       | 1 | oral epidermis    | 1 | kinda abandoned these   | 41,684                | |      |
| 20260617 | POR_R3_C1  | 330  | 1       | 1 | oral gastrodermis | 1 | kinda abandoned these   | 45,039                | |      |
| 20260617 | POR_R72_C2 | 331  | 4       | 7| oral epidermis    | 1 |       | 318,655               | |      |
| 20260617 | POR_R72_C2 | 332  | 4       | 7| oral gastrodermis | 1 |       | 267,130               | |      |
| 20260617 | POR_R3_H2  | 335  | 3       | 4| oral epidermis    | 1 |       | 204,992               | |      |
| 20260617 | POR_R3_H2  | 336  | 3       | 5| oral gastrodermis | 1 |       | 213,183               | |      |
| 20260617 | POR_R3_H2  | 337  | 3       | 3 | bulk_host         | 1 |       | 94,479                | |      |
| 20260617 | POR_R3_H2  | 338  | 3       | 3 | bulk_sym          | 1 |       | 66,965                | |      |
| 20260618 | POR_R3_C3  | 340  | 5L      | 4| oral epidermis    | 1 |       | 172,111               | |      |
| 20260618 | POR_R3_C3  | 341  | 5L      | 6| oral gastrodermis | 1 |       | 250,054               | |      |
| 20260618 | POR_R3_C3  | 342  | 4       | 3 | bulk_host         | 1 | need to measure areas   | 0   | |      |
| 20260618 | POR_R3_C3  | 343  | 4       | 1 | bulk_sym          | 1 | need to measure areas   | 0   | |      |
| 20260618 | POR_R3_H1  | 345  | 4       | 3 | oral epidermis    | 2 |       | 336,329               | 27,317            | 683  |
| 20260618 | POR_R3_H1  | 346  | 4       | 3 | oral gastrodermis | 2 |       | 245,501               | 19,897            | 497  |
| 20260618 | POR_R3_H1  | 347  | 1       | 3 | oral epidermis    | 2 |       | 182,519               | 20,532            | 513  |
| 20260618 | POR_R3_H1  | 348  | 1       | 4| oral gastrodermis | 2 |       | 178,906               | 42,368            | 1059 |
| 20260619 | POR_R3_H3  | 350  | 2       | 6| oral epidermis    | 3 | slight spillage of tube | 387,562               | |      |
| 20260619 | POR_R3_H3  | 351  | 2       | 4| oral gastrodermis | 3 | slight spillage of tube | 102,395               | |      |
| 20260619 | POR_R3_H3  | 352  | 4       | 6| oral epidermis    | 3 | slight spillage of tube | 410,547               | 30,920            | 773  |
| 20260619 | POR_R3_H3  | 353  | 4       | 5| oral gastrodermis | 3 | slight spillage of tube | 130,068               | 31,320            | 783  |
| 20260619 | POR_R72_H1 | 354  | 5       | 7| oral epidermis    | 1 |       | 413,842               | |      |
| 20260619 | POR_R72_H1 | 355  | 5       | 5| oral gastrodermis | 1 |       | 211,616               | |      |
| 20260619 | POR_R72_H2 | 360  | 3       | 4| oral epidermis    | 1 |       | 321,680               | |      |
| 20260619 | POR_R72_H2 | 361  | 3       | 3 | oral gastrodermis | 1 |       | 168,902               | |      |
| 20260619 | POR_R72_C1 | 362  | 5       | 4| oral epidermis    | 1 |       | 397,983               | 43,355            | 1084 |
| 20260619 | POR_R72_C1 | 363  | 5       | 4| oral gastrodermis | 1 |       | 327,188               | 51,089            | 1277 |
| 20260619 | POR_R3_H3  | 370  | 3       | 6| oral epidermis    | 3 |       | 485,130               | 51,157            | 1279 |
| 20260619 | POR_R3_H3  | 371  | 3       | 4| oral gastrodermis | 3 |       | 173,825               | 39,433            | 986  |

---

## Extracting RNA from LCM-d Porites (on hold at this stage)

Full Extraction protocol: [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-05-08-LCM-RNA-Microprep.md)

### Short-hand protocol for reference

- changes to standard: 65 uL digestion buffer instead of 60 uL to account for cel collection in 35 uL instead of 40 uL

1. Thaw LCM-dissection tubes from -80 ºC for 5-10s at room temp.
2. Once thawed, immediately add 65 uL of the digestion buffer and pipette up and down to mix with wide bore tip
3. Incubate for 15 mins at RT (a few tested with 15 minis on thermomixer at 56 ºC shaking at 1400 rpm)
4. **Thaw an aliquot of DNase I from -20 ºC on ice**
5. Transfer entire volume to a 1.5 mL tube with wide-bore tip
6. Spin at 9,000 rcf for 3.5 mins to pellet any debris, then move 95 uL of supernatant to new 1.5 mL tube.
7. Add 190 uL RNA lysis buffer and mix well until clear
8. Add an equal volume of 100% ethanol (285 uL) and mix well
    1.  do not spin down or allow a precipitate to form
9.  Transfer entire volume into RNA (IC) column
10. Spin column at 15,000 rcf for 30s, discard flow-through
    1.  ***All spins, unless noted, were performed at 15,000 rcf for 30s***
11. Wash column with _400 uL wash buffer_ and spin down, discard flow through
12. Prepare DNase treatment (5 uL DNase I with 35 uL DNA Digestion Buffer per sample) on ice
    1.  perform DNAse treatment (40 uL) as written:
        1.  _apply 40 uL_ of the mixture directly to each filter
        2.  incubate at room temperature for 15 minutes
13. Add _400 uL prep buffer_ and spin down, discard flow through
14. Add _700 uL wash buffer_ and spin down, discard flow through
15. Add _400 uL wash buffer_ and spin for 2 minutes at 15,000 rcf
16. Transfer column to labelled 1.5 mL tube and elute in 15 uL RNase/DNase-free water.
17. Allow filter to saturate by spinning at 100 rcf for 1 minute and then elute by spinning down at 12,000 rcf for 1 minute. 
18. Confirm all liquid has been eluted from the filter into the tube, and discard the filter column.
19. Immediately transfer **RNA tubes to ice** and perform QC (hsRNA [tapestation](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/RNA-TapeStation-Protocol/) using 2 uL RNA) as soon as possible.
    1. For each sample, pipette **1 µL High Sensitivity RNA Sample Buffer** and **2 µL RNA sample** in a tube strip
    2. Mix using the IKA MS3 vortexer at 2000 rpm for 1 min, then spin down
    4. On thermocycler:
       1. Heat samples and ladder at 72 °C (162 °F) for **3 min**.
    5. Place samples and ladder on ice for **2 min**.
    6. Spin down again and run tapestation.
20. Store RNA at -80 ºC as quickly after the extraction as possible and **limit freeze-thaw cycles**.

---

## RNA QC for Time‑Series LCM Samples (June 2026)

Extraction results so far have not been promisng, so we are pausing this project for now. 

| LCM Date | Sample     | Tube | Section | Number dissections | Tissue            | Number of Real OE/OG Sets per Sample | Extraction Order | Extraction (planned) date | Digestion          | RNA Tapestation Concentration (pg/uL) | RNA dv200 | RNA Tapestation Peaks Visible | cDNA concentration (ng/uL) | cDNA notes      | Notes | Total Dissection Area | Total Dissection Area / 40 (approx # cells) | Approx Tissue Area, quick measurements -- will redo | Ratio Dissection/Tissue | Approx Tissue Area / 40 (approx # cells) | Fate |
|----------|------------|------|---------|--------------------|-------------------|--------------------------------------|------------------|---------------------------|--------------------|---------------------------------------|-----------|-------------------------------|----------------------------|-----------------|-------|-----------------------|---------------------------------------------|-----------------------------------------------------|-------------------------|------------------------------------------|------|
| 20260618 | POR_R3_H1  | 345  | 4       | 3   | oral epidermis    | 2      | 1 | 6/21/26    | 15 min 56C 1400rpm | 33.9    | 19.77     | No             | 0           | nothing visible |       | 336,329| 8,408         | 27,317 | 12.31    | 683        |      |
| 20260618 | POR_R3_H1  | 346  | 4       | 3   | oral gastrodermis | 2      | 1 | 6/21/26    | 15 min 56C 1400rpm | 22.6    | 10.37     | No             | not prepped | not prepped     |       | 245,501| 6,138         | 19,897 | 12.34    | 497        |      |
| 20260619 | POR_R3_H3  | 370  | 3       | 6   | oral epidermis    | 3      | 1 | 6/21/26    | 15 min 56C 1400rpm | 28.5    | 18.96     | No             | not prepped | not prepped     |       | 485,130| 12,128        | 51,157 | 9.48     | 1279       |      |
| 20260619 | POR_R3_H3  | 371  | 3       | 4   | oral gastrodermis | 3      | 1 | 6/21/26    | 15 min 56C 1400rpm | 24.5    | 19.29     | No             | not prepped | not prepped     |       | 173,825| 4,346         | 39,433 | 4.41     | 986        |      |
| 20260618 | POR_R3_H1  | 347  | 1       | 3   | oral epidermis    | 2      | 2 | 6/22/26    | 15 min RT          | 27.4    | 17.95     | No             | not prepped | not prepped     |       | 182,519| 4,563         | 20,532 | 8.89     | 513        |      |
| 20260618 | POR_R3_H1  | 348  | 1       | 4   | oral gastrodermis | 2      | 2 | 6/22/26    | 15 min RT          | 25.4    | 16.98     | No             | not prepped | not prepped     |       | 178,906| 4,473         | 42,368 | 4.22     | 1059       |      |
| 20260619 | POR_R72_C1 | 362  | 5       | 4   | oral epidermis    | 1      | 2 | 6/22/26    | 15 min RT          | 20.7    | 16.43     | No             | 0.465       | tiny tiny peak  |       | 397,983| 9,950         | 43,355 | 9.18     | 1084       |      |
| 20260619 | POR_R72_C1 | 363  | 5       | 4   | oral gastrodermis | 1      | 2 | 6/22/26    | 15 min RT          | 38.7    | 30.2      | Very small but yes            | 0.642       | tiny tiny peak  |       | 327,188| 8,180         | 51,089 | 6.40     | 1277       |      |

**Tapestation reports:**

|   |   |
|--|--|
| <img width="300" alt="2026-05-08-AM.png" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/tapestation/POR-TS-RNA/TS_1.png"> | 345, 346, 370, 371 |
| <img width="300" alt="2026-05-08-AM.png" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/tapestation/POR-TS-RNA/TS_2.png"> | 347, 348, 362, 363 |
| <img width="300" alt="2026-05-08-PM.png" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/tapestation/POR-TS-RNA/363_trace.png"> | 363 |

- [6/21 RNA Extractions](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-06-21-POR-TS-RNA-1.pdf)
- [6/22 RNA Extractions](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-06-22-POR-TS-RNA-2.pdf)
- [6/21 cDNA](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-06-22-POR-TS-cDNA-1.pdf)
- [6/22 cDNA](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-06-22-POR-TS-cDNA-2.pdf)

**Observations:**

- **Concentration per µL** is often comparable to but slightly lower than earlier [tests](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-27-LCM-Porites-Troubleshooting.md).
- The **limiting factor is RNA integrity**:
  - dv200 ~10–30%, often no visible peaks.
  - Compare to [POR_3/POR_4](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-27-LCM-Porites-Troubleshooting.md) extractions (in Troubleshooting post), where dv200 was >50–70 with clear peaks.
- cDNA synthesis using the NEB low‑input kit:
  - 362 and 363: most promising RNA, extremely low cDNA yields (≤1 ng/µL), but non‑zero. Would likely be enough to continue with library prep but likely low diversity, poor-quality libraries

---

## Comparison to Earlier Porites LCM Troubleshooting

For context, in May 2026 I optimized LCM on **POR_3** and **POR_4** (3/10/26 fixation), testing different digestion conditions and collection buffers. This is detailed in the separate troubleshooting [post](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/_posts/2026-04-27-LCM-Porites-Troubleshooting.md), but the key summary is:

- PK buffer generally outperformed DNA/RNA Shield and RNA lysis buffer for LCM collection.
- Digestion at 1 hr at 56 ºC, 1400 rpm gave the best RNA yield for LCM-d material in the tests, though validation with fresh bulk tissue later showed that extended digestion reduces dv200 so 15 minute digestion was chosen moving forward
- For POR_3 / POR_4 LCM:
    - TS concentrations ~25–108 pg/µL
    - dv200 high enough for clear rRNA peaks
    - cDNA ~2–3 ng/µL from 26 µL reactions using 20 PCR cycles
    - Final libraries after 8 cycles looked excellent and sequenced well (biologically meaningful results, see [repo](https://github.com/zdellaert/Porites_LCM_test))

---


## Notes on the LCM dissections and challenges faced in this project

A few representative fields from the time‑series slides illustrate why these dissections were challenging:

- The ethanol‑only, no‑stain protocol meant that many sections retained areas of **thick OCT** embedding medium surrounding the tissue
- In many areas I had to **re‑cut the same ROI multiple times** to fully detach tissue from the slide.
 - Some dissections were abandoned completely because I was not able to cut them in a timely manner and had to move on.
- This increased laser exposure and total time per slide, and probably **contributed to RNA degradation** (_more time at room temperature before lysis + potential heating/burning of tissue from laser_)

*Example images:*

<img width="500" alt="Example_1" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/random/POR_LCM/20260619/Example_1.png">

<img width="500" alt="Example_2" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/random/POR_LCM/20260619/Example_2.png">

<img width="500" alt="Example_3" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/random/POR_LCM/20260619/Example_3.png">

<img width="500" alt="Example_4" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/random/POR_LCM/20260619/Example_4.png">

<img width="500" alt="Example_5" src="https://raw.githubusercontent.com/zdellaert/ZD_Putnam_Lab_Notebook/refs/heads/master/images/random/POR_LCM/20260619/Example_5.png">

## Interpretation of Time‑Series Attempt (as of June 2026)

- LCM of OE and OG across the 12 time‑series fragments is **logistically feasible** but challenging
- Ethanol‑only, no‑stain slide prep gave cuttable tissue and reasonable dissection areas per tube, but there remained much OCT on the slides that made the LCM difficult (many dissections had to be cut over and over again), likely contributing to the severe RNA degredation
- **RNA integrity is poor** in the time‑series LCM extracts:
  - dv200 typically ~10–30%; most extractions had no visible rRNA peaks.
  - By contrast, POR_3/POR_4 LCM and validation extractions had dv200 >50–70 with small but clear peaks.
  - cDNA yield is low for the small subset of RNA extracts I tested:
    - POR_R72_C1_362 (OE): 20.7 pg/µL, dv200 16.4, no peaks, cDNA 0.465 ng/µL.
    - POR_R72_C1_363 (OG): 38.7 pg/µL, dv200 30.2, tiny peaks, cDNA 0.642 ng/µL.

At this time, I am unlikely to achieve a full 24‑library LCM RNA‑seq dataset at usable quality without further optimization. A few tubes (e.g. 362, 363) could yield libraries, but the RNA is degraded and they would be sub-optimial. There's a chance the tubes I have not yet extracted yield much better RNA, but this seems unlikely.

## Preserved for Future Use

- All remaining LCM-dissection tubes (~38) stored at -80 °C
- Slides re-frozen at -80 °C
- Original blocks (POR_R3_*, POR_R72_*) stored at -80 °C