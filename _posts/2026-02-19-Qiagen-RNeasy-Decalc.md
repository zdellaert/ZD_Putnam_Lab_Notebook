---
layout: post
title: 2026-02-19 Qiagen RNeasy Extraction Tests, PAXgene fixed tissue at various stages of decalcification
date: '2026-02-19'
categories: Processing, Protocols
tags: [Pocillopora, Porites, RNA, Protocol]
---

## Extracting RNA from PAXgene fixed tissue at various stages of decalcification

### Timeline

<img width="1000" alt="timeline" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/timeline.png?raw=true">

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

## 2/19/26: Pre-decalc samples, testing ProK digestion vs. no digestion

Exact protocol written above.

<img width="400" alt="2026-02-19" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-19.png?raw=true">

| sample_id      | concentration             | RIN |
|----------------|---------------------------|-----|
| POC_1          |  96.9 ng/uL         | 9.1 |
| POC_1_ProK     |  91.6 ng/uL         | 8.4 |
| POR_1          |  44.9 ng/uL         | 8.5 |
| POR_1_ProK     |  40.8 ng/uL         | 8.3 |
| MON_1          |  144 ng/uL         | 8.5 |
| MON_1_ProK     |  168 ng/uL         | 5.8 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-19.pdf)

## 2/21/26: First 24 and 48 hours of decalcification results

- Tissue sampled throughout experiment was collected in 500 uL RLT (w/ 1% BME) in a 2mL tube with beads and bead-beat for 2 mins before being frozen at -80ºC
- Tubes were thawed at room temperature and bead-beat ~1 minute to ensure homogenous thawing and to clear any precipitate
- Same protocol followed as above, but without the proK digestion
- **Notes**
  - For POR and MON, these tubes had a lot of tissue and were pretty cloudy/dark in the lysate.
  - Formed big pellets during the 3 min spin suggesting that maybe there was too much tissue input
  - During elution, the POR columns clogged, potential mucus carry-over.
    - Added another 50 uL on top instead of re-eluting with same 50uL, final volume was closer to 75 uL
  - **This is not great news. Even with just 24 hours of decalc, when none of the corals are decalcified, we get substantial decrease in RIN below what we are aiming for.**

<img width="500" alt="2026-02-21" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-21.png?raw=true">

| sample_id      | concentration             | RIN |
|----------------|---------------------------|-----|
| POC_2 (EDTA 6hr)  |  148 ng/uL         | 7.1 |
| POC_3 (EDTA 24hr) |  160 ng/uL         | 7.4 |
| POC_4 (EDTA 24hr+2 hrs sucrose)  |  88.9 ng/uL         | **4.6** |
| POC_5 (EDTA 48hr)  |  82.4 ng/uL         | 7.5 |
| MON_2 (EDTA 24hr)  |  155 ng/uL         | 6.0 |
| MON_3 (EDTA 48hr) |  194 ng/uL         | 5.4 |
| POR_2 (EDTA 24hr) |  52.4 ng/uL         | 6.5 |
| POR_3 (EDTA 48hr) |  35.6 ng/uL         | 6.2 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-21.pdf)

## 2/22/26: First 24 and 48 hours of decalcification results, re-extraction of POR + MON

- Because of the big pellets formed, I thought maybe the filter clogging could be fixed by re-extracting from those tubes with more RLT added to dilute the lysate. Re-extracting  POR_2, POR_3, MON_2, and MON_3
  - Added another 500 uL RLT (w/ 1% BME) to the tubes as they thawed + pipetted to mix
  - Bead-beat ~1 minute to ensure homogenous thawing and to clear any precipitate
  - Moved 450 uL to a new tube and centrifuged for 3 mins to pellet debris, then repeated this with 400 of the supernatant from that spin to try to minimize any debris carry-over into columns.
  - Same protocol followed as above, but without the proK digestion

- As seen below, RINs improved slightly but not substantially, and large gDNA-appearing peaks still occur. I might try one more time with a gentle ProK digestion
  - **This is not great news. Even with just 24 hours of decalc, when none of the corals are decalcified, we get substantial decrease in RIN below what we are aiming for.**

<img width="300" alt="2026-02-22" src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-22.png?raw=true">

| sample_id      | concentration             | RIN |
|----------------|---------------------------|-----|
| POR_2 (EDTA 24hr) |  70.7 ng/uL         | 6.2 |
| POR_3 (EDTA 48hr) |  89.3 ng/uL         | 6.3 |
| MON_2 (EDTA 24hr) |  137 ng/uL         | 6.1 |
| MON_3 (EDTA 48hr) |  142 ng/uL         | 5.6 |

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2026-02-22.pdf)

## Total count of extractions used from this kit (50 preps):

- 6+6+8+4 = 24
- If I re-extract the 4 POR+MON again with Proteinase K and then extract the final 8 tubes, I will have used 36/50 preps from the kit without yet using any of the preps for QC-ing tissue sections. Need to think strategically about which samples to do.

## 2/22/26: All final blocks embedded, details in google sheet and notebook

- This was more rushed than I'd like due to the blizzard on 2/23, several of the POR and MON were not fully decalcified. But it will still give us RNA quality info.

https://docs.google.com/spreadsheets/d/1y8tZUTPmXJmq1QOfvcBU3mhVc6VYH7Xe-fA4zXSnTZ4/edit?usp=sharing

## Embedded blocks were sectioned 2/26/26 and 2/27/26:

| Block_Label | Block_Description | Section_Date | Section_Notes                             | Block_Status | Slide_1_Status       | Slide_2_Status       | Slide_3_Status |
|-------------|-------------------|--------------|-------------------------------------------|--------------|----------------------|----------------------|----------------|
| POC_4       | EDTA-24hr-Sucrose  | 2/26/26      | Was surpisingly good                      | In -80       | H&amp;E Stained 2/26 | H&amp;E Stained 2/26 | Check -80      |
| POC_5       | EDTA-48hr-Sucrose | 2/26/26      |                                           | In -80       | H&amp;E Stained 2/26 | H&amp;E Stained 2/26 | Check -80      |
| POC_6       | EDTA-72hr-noSuc   | 2/26/26      | Was surpisingly good                      | In -80       | Check -80            | Check -80            | Check -80      |
| POC_7       | EDTA-72hr-Sucrose  | 2/26/26      |                                           | In -80       | Check -80            | Check -80            | Check -80      |

| Block_Label | Block_Description | Section_Date | Section_Notes                             | Block_Status | Slide_1_Status       | Slide_2_Status       | Slide_3_Status |
|-------------|-------------------|--------------|-------------------------------------------|--------------|----------------------|----------------------|----------------|
| MON_3       | EDTA-48hr-Sucrose  | 2/27/26      | Too much skeleton, really hard to section | In -80       | Check -80            |                      |                |
| MON_4       | EDTA-72hr-noSuc   | 2/27/26      | Of all the MON, maybe the best?           | In -80       | Check -80            |                      |                |
| MON_5       | EDTA-72hr-Sucrose-short  | 2/26/26      | Too much skeleton, really hard to section | In -80       | Check -80            | Check -80            | Check -80      |
| MON_6       | EDTA-72hr-Sucrose-long  | 2/26/26      | Too much skeleton, really hard to section | In -80       | Check -80            | Check -80            | Check -80      |

| Block_Label | Block_Description | Section_Date | Section_Notes                             | Block_Status | Slide_1_Status       | Slide_2_Status       | Slide_3_Status |
|-------------|-------------------|--------------|-------------------------------------------|--------------|----------------------|----------------------|----------------|
| POR_3       | EDTA-48hr-Sucrose  | 2/27/26      |                                           | In -80       | Check -80            | Check -80            | Check -80      |
| POR_4       | EDTA-72hr-noSuc   | 2/27/26      |                                           | In -80       | Check -80            | Check -80            | Check -80      |
| POR_5       | EDTA-72hr-Sucrose-short  | 2/27/26      |                                           | In -80       | Check -80            | Check -80            | Check -80      |
| POR_6       | EDTA-72hr-Sucrose-long  | 2/27/26      |                                           | In -80       | Check -80            | Check -80            | Check -80      |

## Next Steps Week of 3/1/26:

- Stain slides sectioned 2/26 and 2/27 and assess tissue quality
- Finish extracting tissue samples and cryostat scrolls from selected samples
  - If I re-extract the 4 POR+MON again with Proteinase K and then extract the final 8 tubes, I will have used 36/50 preps from the kit without yet using any of the preps for QC-ing tissue sections. Need to think strategically about which samples to do.