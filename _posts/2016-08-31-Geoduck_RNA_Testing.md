---
layout: post
title: Geoduck RNA ReExtraction and Testing
date: '2016-08-31'
categories: Processing
tags: [RNA, P. generosa, shellfish]
---

20160829-20160830 Testing for improved yield of RNA with no genomic DNA contamination and for removal of rRNA through one round of polyA selection on total RNA

## Sample list from samples with additional RNAzol on 20160825   
* EPI-275
* EPI-276 
* EPI-282
* EPI-283
* EPI-289
* EPI-290
* EPI-298
* EPI-299
* EPI-302
* EPI-303
   

## RNA Extractions 20160829
* moved 0.5ml of RNAzol/homogenate mix to new tube
* Added 0.2ml of nuclease free water to each new tube
* Proceeded with [**RNA Extraction Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/RNA-Extraction-Protocol/)
* After initial centrifugation mixed yielded ~0.65ml of supernatant that was mixed with 0.65ml of 100% ethanol and was added to the spin column step

## RNA Quantification 20160829
* Diluted samples 1:100 in nucelase-free water
* Used 10µl of sample and 190µl of Qubit Mix
* Ran [**RNA Quantification Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Qubit_HS_RNA_Protocol/)
* Saved samples at -80°C in 4 aliquots (3,3,~20,~20µl)

## RNA Concentrations

|---
|-:|-:
| **Sample.ID** | **Conc.(ng/µl)** 
| Standard2 | 10.2
| EPI-275 | 390 
| EPI-276 | 420 
| EPI-282 | 1040 
| EPI-283 | 572 
| EPI-289 | 210 
| EPI-290 | 614 
| EPI-298 | 632 
| EPI-299 | 290 
| EPI-302 | 336 
| EPI-303 | 418 
|===

* a 20µl aliquot with an average of ~500ng/µl the samples has ~10µg of total RNA, more than necessary (4µg) for Illumina mRNASeq library prep

## rRNA Removal 20160830 from samples extracted 20160825
To test for removal of rRNA the samples were run through the Ambion rRNA Poly(A) Purist kit. One of the ~20µl aliquots of RNA from each sample was used. 

* EPI-283
* EPI-289
* EPI-290
* EPI-298

* Added 0.23ml of nuclease free water to each sample
* Added 0.25ml of 2x binding solution and mixed thoroughly
* Added mix to Oligo(dT) Cellulose and mixed by pipetting
* Heated the mixture  for 5min at 70°C
* Placed tube on rotating rack for 30min
* Centrifuged at 2000g for 3min at room temperature
* Removed supernatant which should contain rRNA and other non-mRNA components and saved to check on Bioanalyzer
* Placed THE RNA Storage Solution at 70°C 
* Added 0.5ml of **Wash Solution 1** to Olido(dT) Cellulose and vortexed to mix
* Placed mixture in spin column in 2ml microfuge tube
* Centrifuged at 3,000 for 3min at room temperature and discarded flow through
* Added 0.5ml of **Wash Solution 1** to Olido(dT) Cellulose and vortexed to mix
* Placed mixture in spin column in 2ml microfuge tube
* Centrifuged at 3,000 for 3min at room temperature and discarded flow through
* Added 0.5ml of **Wash Solution 2** to Olido(dT) Cellulose and vortexed to mix
* Placed mixture in spin column in 2ml microfuge tube
* Centrifuged at 3,000 for 3min at room temperature and discarded flow through
* Added 0.5ml of **Wash Solution 2** to Olido(dT) Cellulose and vortexed to mix
* Placed mixture in spin column in 2ml microfuge tube
* Centrifuged at 3,000 for 3min at room temperature and discarded flow through and collection tube
* Place column in new microfuge tube
* Added 0.2ml of heated THE RNA Storage Solution to the Olido(dT) Cellulose and vortexed to mix
* Centrifuged at 5,000g for 2 min and 
* Saved the flow through in 4 aliquots (3µl, 3µl, 85µl and 85µl) at -80°C

## RNA Quantification of polyA selected samples and supernatant with other RNAs 20160830
* For mRNA samples used 20µl of sample and 180µl of Qubit Mix
* For rRNA (supernatant) samples used 1µl of sample and 199µl of Qubit Mix
* Ran [**RNA Quantification Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Qubit_HS_RNA_Protocol/)

## RNA Concentrations

|---
|-:|-:
| **Sample.ID** | **Conc.(ng/µl)** 
| EPI-283 mRNA | 0.259 
| EPI-289 mRNA| 0.20 
| EPI-290 mRNA| 0.20 
| EPI-298 mRNA| 0.21 
| EPI-283 rRNA | 57.6 
| EPI-289 rRNA| 39.6 
| EPI-290 rRNA| 31 
| EPI-298 rRNA| 33 
|===


## RNA Quality check of re-extracted samples, mRNA, and rRNA 20160830
* Ran [**RNA Quality Check Protocol**](https://hputnam.github.io/Putnam_Lab_Notebook/Bioanalyzer_Euk_Total_RNA_Pico_Protocol/)

* Diluted RNA ReExtraction 10 samples from 20160829 with a 1:100 dilution and ran on bioanalyzer, also added one sample of mRNA from polyA selection 20160830 with no dilution (283 mRNA)
* [BioAnalyzer 20160830 Chip 1]({{ https://hputnam.github.io}}/project_juvenile_geoduck_OA/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-08-30_14-41-55_chip1.pdf)

* Ran 3 samples of mRNA from polyA selection 20160830 with no dilution (289, 290, 298), 4 samples of mRNA diluted 3µl+97µl (283 289, 290, 298 mRNA), and 4 samples of rRNA supernatant diluted 3µl+97µl (283 289, 290, 298 rRNA)
* [BioAnalyzer 20160830 Chip 2]({{ https://hputnam.github.io}}/project_juvenile_geoduck_OA/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-08-30_15-09-31_chip2.pdf)


## Conclusions
* **Only a single large peak is expected for total geoduck RNA, as the in the rRNA the 28S contains a hidden break that when the sample is heat denatured will break the 28S in half and these fragments will co-migrate with the 18S** 
* The identical patterns of the smaller peaks prior to the large rRNA peak again suggests the small peaks are not due to degradation. It is possible they are RNAs from other "symbiotic" or prey organisms as the geoducks are fed diatoms and dinoflagellates. 
* The use of a higher RNAzol:Tissue ratio minimized the genomic DNA carryover in chip1 samples
* PolyA selection resulted in total removal of the large 18S and 28S single peak, which was only visible in the rRNA supernatant fraction and not the mRNA fraction
* Due to eluting in 200µl of THE RNA Storage Solution, the mRNA was of low concentration and barely detectable on the Bioanalyzer (chip 1 sample 283) and was not detectable in the diluted mRNA samples
* One round of polyA selection appears to be enough to remove rRNA. This will be done as part of the Illumina library prep kit, step 1

* Assuming that the identical patterned smaller peaks are from feeding of diatoms and dinoflagellates, will continue with homogenizations and extractions of RNA for Illumina library prep