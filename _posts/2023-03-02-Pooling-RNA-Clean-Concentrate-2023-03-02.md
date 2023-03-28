---
layout: post
title: 2023-03-02 Pooling RNA Using Zymo Clean and Concentrate Kit for ENCORE Project
date: '2023-03-02 16:00:00'
categories: Processing
tags: [DNA, RNA, ENCORE, Diploria labyrinthiformis, Montastraea cavernosa, Madracis decactis, Porites astreoides]
---

## Pooling RNA Using Zymo Clean and Concentrate Kit for ENCORE Project, March 2, 2023

For the purpose of creating reference transcriptomes, I made 3 pools of RNA for 3 species, *Diploria labyrinthiformis, Montastraea cavernosa,* and *Madracis decactis*. I am not making a pool for *Porites astreoides* because we have not been able to extract high quality RNA from that species for the samples from this project. The purpose of the pools is to capture genetic diversity and treatment diversity in our reference transcriptome, so the four samples chosen per pool are all from different genotypes and were all exposed to different temperatures (16, 22, 29, and 36 ºC). We will then send these three pools to Azenta for RNA sequencing. We used the [Zymo RNA Clean and Concentrate Kit](https://www.zymoresearch.com/products/rna-clean-concentrator-5) on the pools to concentrate the pooled RNA to the recommended concentration required by Azenta, >2 µg @ >50 ng/µL.


## Samples

| colony_id | Temp.Cat | Extraction.Date | RNA_Qubit_AVG (ng/µL) |
|-----------|----------|-----------------|-----------|
| Dlab-A4   | 16       | 20221005        | 13.5      |
| Dlab-B5   | 22       | 20230113        | 11.6      |
| Dlab-D1   | 29       | 20221003        | 12.3      |
| Dlab-C7   | 36       | 20221005        | 10.7      |

------

| colony_id | Temp.Cat | Extraction.Date | RNA_Qubit_AVG (ng/µL) |
|-----------|----------|-----------------|-----------|
| Mdec-F4   | 16       | 20230118        | 22.1      |
| Mdec-B5   | 22       | 20221017        | 14.1      |
| Mdec-E1   | 29       | 20221005        | 22        |
| Mdec-A7   | 36       | 20221003        | 18.3      |

------

| colony_id | Temp.Cat | Extraction.Date | RNA_Qubit_AVG (ng/µL) |
|-----------|----------|-----------------|-----------|
| Mcav-B4   | 16       | 20230118        | 17.1      |
| Mcav-D5   | 22       | 20221017        | 0    (but good bands on gel)     |
| Mcav-E1   | 29       | 20230113        | 27.3      |
| Mcav-A7   | 36       | 20230216        | 23.5      |


## Protocol

For each species, take 40 µL per sample (4 samples total) and transfer into a new tube labelled for that species. Mix together, final volume in each tube will be 160 µL. This is pooling 12 tubes into 3 species-specific tubes, and these three tubes will be all you work with for the clean and concentrate kit.

Then, follow the [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Zymo_RNA_Clean_Concentrate.pdf) for the Zymo Clean and Concentrate kit, eluting in 25 µL of DNAse/RNAse free water.

1. Since each sample is 160 uL, add 320 uL of RNA binding buffer.
2. Add an equal volume (480 uL) of 100% ethanol and mix.
3. Transfer the sample to the Zymo-Spin™ IC Column in a Collection Tube and centrifuge. Discard the flow-through.
4. Add 400 µl RNA Prep Buffer to the column and centrifuge. Discard the flow-through.
5. Add 700 µl RNA Wash Buffer to the column and centrifuge. Discard the flow-through.
6. Add 400 µl RNA Wash Buffer to the column and centrifuge for 1 minute ensure complete removal of the wash buffer. Carefully, transfer the column into a RNase-free tube (not provided).
7. Add 25 µl DNase/RNase-Free Water directly to the column matrix and centrifuge.

## Qubit Results

- Used Broad range dsDNA and RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 416.13 (S1) & 9020.64 (S2)

| colony_id | Species                     | RNA_QBIT_1 | RNA_QBIT_2 | AVG (ng/uL) | Volume (uL), after Qubit| Final Amount RNA (ng) |
|-----------|-----------------------------|------------|------------|--------------|-------------|-----------------|
| Dlab Pool | *Diploria labyrinthiformis* | 45.6       | 45.2       | **45.4**     | 24          | **1089.6**           |
| Mcav Pool | *Montastraea cavernosa*     | 76.0       | 75.6       | **75.8**         | 24          | **1819.2**            |
| Mdec Pool | *Madracis decactis*         | 80.4       | 78.4       | **79.4**         | 24          | **1905.6**           |

So all three pools are at least double the minimum amount of 500 ng, but a little lower (DLAB almost 1/2) than the recommended amount of 2000 ng. MDEC and MCAV are both well above the recommened concentration of 50 ng/uL and DLAB is very close, so I believe all pools are ready for sequencing.

### Information about estimated concentrations and % loss of RNA

Based on the amount of RNA entering each pool from the original Qubit values, I estimated the following expected amount of RNA after concentrating and calculated a % recovery:

| Pool | Estimated total RNA of Pool (ng) | Est. Conc. of Pool (ng/uL) | Actual Qubit Conc. | Actual ng RNA | % efficiency |
|------|----------------------------------|----------------------------|--------------------|---------------|--------------|
| DLAB | 1924                             | 76.96                      | 45.4               | 1135          | 58.99%       |
| MDEC | 3060                             | 122.4                      | 75.8               | 1895          | 61.93%       |
| MCAV | 2716                             | 108.64                     | 79.4               | 1985          | 73.09%       |

I calculated "Estimated total RNA of Pool (ng)" by summing the ng amount of RNA from each tube that was added into the pool (same RNA concentration * 40 uL). Then, to calculate "Est. Conc. of Pool (ng/uL)", I divided that number by 25 uL , the amount that I eluted the pools into. Finally, I calculated % efficiency by dividing Estimated total RNA of Pool (ng) by the Actual ng RNA.
