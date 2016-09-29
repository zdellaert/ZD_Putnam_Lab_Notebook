---
layout: post
title: Geoduck RNA Extraction Tests
date: '2016-09-13'
categories: Processing
tags: [RNA, P. generosa, shellfish]
---

Tested RNA extractions for improving quality and identifying if peaks prior to major ribosomal peak are degradation or RNA from gut contents

## Sample list used for comparisons  
* EPI-309 S-309 = siphon tissue only stored in RNAlater, ground to powder on liquid nitrogen on 20160912, and stored at -80
* EPI-309 M-309 = whole body and some siphon tissue stored in RNAlater, ground to powder on liquid nitrogen on 20160912, and stored at -80 
* Geoduck10 G-10 (tissue from Grace) = adult tissue stored at -80, ground to powder on liquid nitrogen on 20160913, and extracted immediately
* EPI-56 = whole body stored at -80, ground to powder on liquid nitrogen on 20160912, and stored at -80
* EPI-103 = whole body tissue stored in RNAlater, ground to powder on liquid nitrogen on 20160912, and stored at -80
* Blank = extraction procedure and QC blank

## Extraction Procedure
* Used ~10mg plastic scoops to transfer 4 scoops (~40mg) of ground tissue to 0.5ml RNAzol
* Homogenized again with teflon pestles in microfuge tubes with RNAzol
* Proceeded with [**RNA Extraction Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/RNA-Extraction-Protocol/)
* After initial centrifugation, yielded ~0.65ml of supernatant that was mixed with 0.65ml of 100% ethanol and was added to the spin column step

## RNA Quantification 
* Diluted samples 1:100 in nucelase-free water
* Used 10µl of sample and 190µl of Qubit Mix
* Ran [**RNA Quantification Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Qubit_HS_RNA_Protocol/)
* Saved samples at -80°C in 3 aliquots (3,~22,~22µl)

## RNA Concentrations

|---
|-:|-:
| **Sample.ID** | **Conc.(ng/µl)** 
| EPI-M-309 | 4.1
| EPI-S-309 | 2.58
| Geo-10 | 2
| EPI-56 | 2.78 
| EPI-103  | 6.14 
| Blank | 0
|===


## RNA Quality check of total RNA
* Ran [**RNA Quality Check Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Bioanalyzer_Euk_Total_RNA_Pico_Protocol/)

* Diluted samples with a 1:100 dilution and ran on bioanalyzer
* [BioAnalyzer 20160913 Chip]({{ https://hputnam.github.io}}/project_juvenile_geoduck_OA/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-09-13_14-38-49.pdf)

## Conclusions
* To test of there is degradation due to storage in RNA later sample EPI-56, EPI-M-309, and EPI-103 were compared. EPI-M-309 and EPI-103 stored in RNAlater showed much more degradation than the sample stored at -80.
* This suggests storage in RNAlater causes more degradation than directly sampling to -80

* To test of there is "gut content" RNAs in whole body extractions, sample EPI-S-309 (siphon only, no guts) and sample EPI-M-309 (siphon and guts, whole body) were compared. M-309 (whole body) again showed much more degradation. S-309 (siphon only) may have background pattern of "gut contents", but it is much reduced compared to M-309 and prior sample results.
* This suggests there may be some RNAs from "gut contents", but reduced in siphon only tissue where food buildup would be low
* This suggests it is not the storage in RNAlater alone that is causing the degradation, as the siphon tissue stored in RNA later decent quality
* Hypotheses: There maybe some interaction of RNAlater and calcium carbonate shell reducing the stabilization of the RNA, or some tissues are differentially degraded in terms of their RNA and the whole body extraction reflects noisy degradation with no role of the shell in extraction inhibition

* The adult geoduck tissue (Geo-10) stored at -80 had the highest quality with no discernible degradation
* The blank had no detectable carry-over contamination from the extraction procedure.