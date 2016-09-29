---
layout: post
title: Geoduck homogenization and RNA extraction
date: '2016-08-30'
categories: Processing
tags: [P. generosa, shellfish]
---

20160824-20160829
Homogenization of juvenile geoduck samples for use in nucleic acid extractions

[**Tissue Homogenization for Nucleic Acid Analysis Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Homogenization-N2-protocol/)

## Sample list 20160824   
* EPI-276 
* EPI-282
* EPI-283
* EPI-289
* EPI-290
* EPI-298
* EPI-299
* EPI-302
* EPI-303
   
## Sample list 20160825  
* EPI-275 

Homogenized samples on liquid nitrogen and split in half for RNA and DNA extractions
Placed samples immediately on dry ice and moved them directly to -80° storage 

## RNA Extractions
* Added 1.0ml of RNAzol to each tube and homogenized with teflon pestle
* moved 0.5ml of homogenate to new tube
* Added 0.4ml of nuclease free water to each new tube
* Added 0.5ml of RNAzol to the initial homogenate-RNAzol mix and replaced at -80°C
* Proceeded with [**RNA Extraction Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/RNA-Extraction-Protocol/)

## RNA Quantification 20160826
* Diluted samples 1:100 in nucelase-free water
* Used 10µl of sample and 190µl of Qubit Mix
* Ran [**RNA Quantification Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Qubit_HS_RNA_Protocol/)

## RNA Concentrations

|---
|-:|-:
| **Sample.ID** | **Conc.(ng/µl)** 
| EPI-275 | 582 
| EPI-276 | 1180 
| EPI-282 | 1160 
| EPI-283 | 1160 
| EPI-289 | 790 
| EPI-290 | 1060 
| EPI-298 | 1020 
| EPI-299 | 762 
| EPI-302 | 888 
| EPI-303 | 706 
|===

## RNA Quality 20160826
* Ran [**RNA Quality Check Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Bioanalyzer_Euk_Total_RNA_Pico_Protocol/)

* Diluted above 1:100 dilution of samples again 1:10 and ran on bioanalyzer (plus test sample EPI 291)
* [BioAnalyzer 20160826 Chip 1]({{ https://hputnam.github.io}}/project_juvenile_geoduck_OA/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-08-26_12-00-14_chip1.pdf)

* Used samples from above 1:100 dilute and ran on bioanalyzer (plus test sample EPI 291)
* [BioAnalyzer 20160826 Chip 2]({{ https://hputnam.github.io}}/project_juvenile_geoduck_OA/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-08-26_12-48-37_chip2.pdf)

* Results were very noisy and degraded, ladder did not display correctly despite the fact it was new
* Appears to be a problem with chip, kit, ladder, or setup

## RNA Quality 20160829
* Issue with 8-26 Bioanalyzer was identified as wrong clip position on loading syringe. Moved clip to top position.
* Ran [**RNA Quality Check Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Bioanalyzer_Euk_Total_RNA_Pico_Protocol/)

* Diluted samples extracted on 20160824 - 20160825 1:100 and ran on bioanalyzer along with a positive control from larval geoduck RNA extracted by SJW (#35)
* [BioAnalyzer 20160829 Chip 1]({{ https://hputnam.github.io}}/project_juvenile_geoduck_OA/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-08-29_11-19-26_chip1.pdf)


## Conclusions
* **Only a single large peak is expected for geoduck RNA, as the in the rRNA the 28S contains a hidden break that when the sample is heat denatured will break the 28S in half and these fragments will co-migrate with the 18S** 
* Many peaks seen prior to the tall single peak, some potential for genomic DNA to be present after the large rRNA peak
* The identical patterns of the smaller peaks prior to the large rRNA peak suggests the small peaks are not due to degradation. It is possible they are RNAs from other "symbiotic" or prey organisms as the geoducks are fed diatoms and dinoflagellates. The positive control would not have these small peaks as the prey is in too low of concentration at the larval stage the RNA was obtained from.
* To check for degradation and to minimize genomic carry over, RNA extraction should be repeated with a higher RNAzol to tissue ratio to minimize genomic DNA carryover and to prevent the capacity of the spin columns from being overwhelmed.
