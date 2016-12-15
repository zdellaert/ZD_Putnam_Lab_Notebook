---
layout: post
title: Geoduck RRBS Library Prep - part 2
date: '2016-12-09'
categories: Processing
tags: [DNA, DNA Methylation, geoduck, P. generosa, RRBS]
---

Prepping remaining 76 RRBS libraries for geoduck juvenile OA acclimatization study.

20161206

Chose remaining 76 samples from 88 sample set for full timepoint coverage of geoduck ocean acidification study.100ng was used as the starting amount of DNA for each sample and the volume of water in each reaction was adjusted as necessary. 0.5% unmethylated lambda DNA was spiked in (w/w DNA) to determine conversion efficiency by estimating the error rate at which a C count occurs at an unmethylated C position.

# Step 1 MSPI DNA Cutting
MSPI restriction endonuclease in NEBuffer2

* MspI - 25,000U (NEB cat: R0106L)
* NEBuffer2 10x (NEB cat: B7002S)

## Reaction Mix
* Samples were mixed as follows to a total reaction volume of 30µl. Samples were incubated at 37°C starting at 15:00 
* Lambda DNA (581ng/µl) was diluted 1:1160 for a concentration of 0.5ng/µl and 1µl added to each sample
* Unmethylated lamda phage DNA (Promega cat: D1501)

	* 3µl NEBuffer2
	* 1µl MSPI 20U/µl
	* 16µl DNA (100ng)
	* 10µl of H20
	* 30µl total

Date|EPI.Tube.Num|Tank|Treatment|TimePoint|Homogenization|DNA.Extraction|DNA.QC|DNA.Conc.ng.µl|DNA.vol.µl|DNA.amount.µg|vol for 100ng|lambda.0.5%|Water.µl|NSBuffer2.µl|MSPI.µl
---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---
16-Mar-16|EPI_41|Time0|Field|Day0|20160912|20161025|20161026|13.6|140|1.904|7.4|1|17.6|3|1
16-Mar-16|EPI_42|Time0|Field|Day0|20160912|20161028|20161028|79|140|11.06|1.3|1|23.7|3|1
16-Mar-16|EPI_43|Time0|Field|Day0|20160912|20161025|20161026|17.2|140|2.408|5.8|1|19.2|3|1
16-Mar-16|EPI_44|Time0|Field|Day0|20160912|20161025|20161026|14.8|140|2.072|6.8|1|18.2|3|1
17-Mar-16|EPI_45|Tank11|Low|Day1|20160912|20161028|20161028|43.1|140|6.034|2.3|1|22.7|3|1
17-Mar-16|EPI_46|Tank11|Low|Day1|20160912|20161028|20161028|21.2|140|2.968|4.7|1|20.3|3|1
17-Mar-16|EPI_47|Tank12|Super.Low|Day1|20160912|20161028|20161028|57.6|140|8.064|1.7|1|23.3|3|1
17-Mar-16|EPI_48|Tank12|Super.Low|Day1|20160912|20161028|20161028|12.6|140|1.764|7.9|1|17.1|3|1
17-Mar-16|EPI_49|Tank13|Ambient|Day1|20160912|20161025|20161026|63.4|140|8.876|1.6|1|23.4|3|1
17-Mar-16|EPI_50|Tank13|Ambient|Day1|20160912|20161028|20161028|8.21|140|1.1494|12.2|1|12.8|3|1
17-Mar-16|EPI_51|Tank14|Low|Day1|20160912|20161025|20161026|14.6|140|2.044|6.8|1|18.2|3|1
17-Mar-16|EPI_52|Tank14|Low|Day1|20160912|20161025|20161026|9.82|140|1.3748|10.2|1|14.8|3|1
17-Mar-16|EPI_53|Tank15|Ambient|Day1|20160912|20161025|20161026|27.4|140|3.836|3.6|1|21.4|3|1
17-Mar-16|EPI_54|Tank15|Ambient|Day1|20160912|20161025|20161026|15|140|2.1|6.7|1|18.3|3|1
17-Mar-16|EPI_55|Tank16|Super.Low|Day1|20160912|20161025|20161026|12.4|140|1.736|8.1|1|16.9|3|1
17-Mar-16|EPI_56|Tank16|Super.Low|Day1|20160912|20161025|20161026|21.4|140|2.996|4.7|1|20.3|3|1
29-Jul-16|EPI_151|Ambient|Ambient|Day135|20160909|20161004|20161006|11.8|140|1.652|8.5|1|16.5|3|1
29-Jul-16|EPI_152|Ambient|Ambient|Day135|20160909|20161004|20161006|16.8|140|2.352|6|1|19|3|1
29-Jul-16|EPI_153|Ambient|Ambient|Day135|20160909|20161025|20161026|22.4|140|3.136|4.5|1|20.5|3|1
29-Jul-16|EPI_154|Ambient|Ambient|Day135|20160909|20161025|20161026|19.5|140|2.73|5.1|1|19.9|3|1
29-Jul-16|EPI_159|Low|Low|Day135|20160909|20161004|20161006|21.4|140|2.996|4.7|1|20.3|3|1
29-Jul-16|EPI_160|Low|Low|Day135|20160909|20161004|20161006|10.8|140|1.512|9.3|1|15.7|3|1
29-Jul-16|EPI_161|Low|Low|Day135|20160909|20161028|20161028|24.9|140|3.486|4|1|21|3|1
29-Jul-16|EPI_162|Low|Low|Day135|20160909|20161007|20161010|12.5|140|1.75|8|1|17|3|1
29-Jul-16|EPI_167|Super.Low|Super.Low|Day135|20160908|20160930|Pass|13.2|190|2.508|7.6|1|17.4|3|1
29-Jul-16|EPI_168|Super.Low|Super.Low|Day135|20160908|20160930|Pass|6.18|190|1.1742|16.2|1|8.8|3|1
29-Jul-16|EPI_169|Super.Low|Super.Low|Day135|20160908|20161007|20161010|14.8|140|2.072|6.8|1|18.2|3|1
29-Jul-16|EPI_170|Super.Low|Super.Low|Day135|20160908|20161007|20161010|11.2|140|1.568|8.9|1|16.1|3|1
8-Aug-16|EPI_175|Bin1|Low-Ambient|Day145|20160908|20160930|Pass|19.6|190|3.724|5.1|1|19.9|3|1
8-Aug-16|EPI_176|Bin1|Low-Ambient|Day145|20160908|20160930|Pass|7.84|190|1.4896|12.8|1|12.2|3|1
8-Aug-16|EPI_181|Bin2|Ambient-Ambient|Day145|20160908|20161004|20161006|40.8|140|5.712|2.5|1|22.5|3|1
8-Aug-16|EPI_182|Bin2|Ambient-Ambient|Day145|20160908|20161004|20161006|20.8|140|2.912|4.8|1|20.2|3|1
8-Aug-16|EPI_184|Bin3|Ambient-Ambient|Day145|20160908|20161007|20161010|7.46|140|1.0444|13.4|1|11.6|3|1
8-Aug-16|EPI_185|Bin3|Ambient-Ambient|Day145|20160907|20161007|20161010|18.6|140|2.604|5.4|1|19.6|3|1
8-Aug-16|EPI_187|Bin4|Super.Low-Ambient|Day145|20160907|20160930|Pass|17.1|190|3.249|5.8|1|19.2|3|1
8-Aug-16|EPI_188|Bin4|Super.Low-Ambient|Day145|20160907|20160930|Pass|14.5|190|2.755|6.9|1|18.1|3|1
8-Aug-16|EPI_193|Bin5|Low-Ambient|Day145|20160907|20161004|20161006|9.26|140|1.2964|10.8|1|14.2|3|1
8-Aug-16|EPI_194|Bin5|Low-Ambient|Day145|20160907|20161004|20161006|11.7|140|1.638|8.5|1|16.5|3|1
8-Aug-16|EPI_199|Bin6|Super.Low-Ambient|Day145|20160907|20161004|20161006|21.8|140|3.052|4.6|1|20.4|3|1
8-Aug-16|EPI_200|Bin6|Super.Low-Ambient|Day145|20160907|20161004|20161006|21.2|140|2.968|4.7|1|20.3|3|1
8-Aug-16|EPI_205|Bin7|Ambient-Low|Day145|20160907|20160930|Pass|11.9|190|2.261|8.4|1|16.6|3|1
8-Aug-16|EPI_206|Bin7|Ambient-Low|Day145|20160906|20160930|Pass|18.1|190|3.439|5.5|1|19.5|3|1
8-Aug-16|EPI_208|Bin8|Low-Low|Day145|20160906|20161007|20161010|31|140|4.34|3.2|1|21.8|3|1
8-Aug-16|EPI_209|Bin8|Low-Low|Day145|20160906|20161007|20161010|22|140|3.08|4.5|1|20.5|3|1
8-Aug-16|EPI_214|Bin9|Super.Low-Low|Day145|20160906|20161004|20161006|13.3|140|1.862|7.5|1|17.5|3|1
8-Aug-16|EPI_215|Bin9|Super.Low-Low|Day145|20160906|20161004|20161006|22.6|140|3.164|4.4|1|20.6|3|1
8-Aug-16|EPI_220|Bin10|Super.Low-Low|Day145|20160906|20160930|Pass|48.8|190|9.272|2|1|23|3|1
8-Aug-16|EPI_221|Bin10|Super.Low-Low|Day145|20160906|20160930|Pass|30|190|5.7|3.3|1|21.7|3|1
8-Aug-16|EPI_226|Bin11|Ambient-Low|Day145|20160902|20161007|20161010|13.1|140|1.834|7.6|1|17.4|3|1
8-Aug-16|EPI_227|Bin11|Ambient-Low|Day145|20160902|20161007|20161010|31.6|140|4.424|3.2|1|21.8|3|1
8-Aug-16|EPI_229|Bin12|Low-Low|Day145|20160902|20160930|Pass|17.4|190|3.306|5.7|1|19.3|3|1
8-Aug-16|EPI_230|Bin12|Low-Low|Day145|20160902|20160930|Pass|10.1|190|1.919|9.9|1|15.1|3|1
21-Aug-16|EPI_235|Bin1|Low-Ambient|Day158|20160902|20161004|20161006|10.6|140|1.484|9.4|1|15.6|3|1
21-Aug-16|EPI_236|Bin1|Low-Ambient|Day158|20160902|20161004|20161006|8.66|140|1.2124|11.5|1|13.5|3|1
21-Aug-16|EPI_242|Bin2|Ambient-Ambient|Day158|20160902|20161028|20161028|15.5|140|2.17|6.5|1|18.5|3|1
21-Aug-16|EPI_243|Bin2|Ambient-Ambient|Day158|20160902|20161028|20161028|17.2|140|2.408|5.8|1|19.2|3|1
21-Aug-16|EPI_246|Bin3|Ambient-Ambient|Day158|20160902|20161025|20161026|19.4|140|2.716|5.2|1|19.8|3|1
21-Aug-16|EPI_247|Bin3|Ambient-Ambient|Day158|20160902|20161028|20161028|8.23|140|1.1522|12.2|1|12.8|3|1
21-Aug-16|EPI_250|Bin4|Super.Low-Ambient|Day158|20160901|20161025|20161026|28.2|140|3.948|3.5|1|21.5|3|1
21-Aug-16|EPI_251|Bin4|Super.Low-Ambient|Day158|20160901|20161025|20161026|16|140|2.24|6.3|1|18.7|3|1
21-Aug-16|EPI_257|Bin5|Low-Ambient|Day158|20160901|20161004|20161006|15.4|140|2.156|6.5|1|18.5|3|1
21-Aug-16|EPI_258|Bin5|Low-Ambient|Day158|20160901|20161028|20161028|18.8|140|2.632|5.3|1|19.7|3|1
21-Aug-16|EPI_264|Bin6|Super.Low-Ambient|Day158|20160901|20161025|20161026|8.42|140|1.1788|11.9|1|13.1|3|1
21-Aug-16|EPI_265|Bin6|Super.Low-Ambient|Day158|20160901|20161025|20161026|17.5|140|2.45|5.7|1|19.3|3|1
21-Aug-16|EPI_271|Bin7|Ambient-Low|Day158|20160901|20161028|20161028|39.1|140|5.474|2.6|1|22.4|3|1
21-Aug-16|EPI_272|Bin7|Ambient-Low|Day158|20160901|20161028|20161028|105|140|14.7|1|1|24|3|1
21-Aug-16|EPI_275|Bin8|Low-Low|Day158|20160825|20161025|20161026|15|140|2.1|6.7|1|18.3|3|1
21-Aug-16|EPI_276|Bin8|Low-Low|Day158|20160824|20161025|20161026|21|140|2.94|4.8|1|20.2|3|1
21-Aug-16|EPI_282|Bin9|Super.Low-Low|Day158|20160824|20161004|20161006|10.3|140|1.442|9.7|1|15.3|3|1
21-Aug-16|EPI_283|Bin9|Super.Low-Low|Day158|20160824|20161028|20161028|36.6|140|0.77|2.7|1|22.3|3|1
21-Aug-16|EPI_289|Bin10|Super.Low-Low|Day158|20160824|20161025|20161026|13.4|140|1.876|7.5|1|17.5|3|1
21-Aug-16|EPI_290|Bin10|Super.Low-Low|Day158|20160824|20161025|20161026|7.4|140|1.036|13.5|1|11.5|3|1
21-Aug-16|EPI_298|Bin11|Ambient-Low|Day158|20160824|20161028|20161028|79.9|140|11.186|1.3|1|23.7|3|1
21-Aug-16|EPI_299|Bin11|Ambient-Low|Day158|20160824|20161007|20161010|17.6|140|2.464|5.7|1|19.3|3|1
21-Aug-16|EPI_302|Bin12|Low-Low|Day158|20160824|20161004|20161006|32.8|140|4.592|3|1|22|3|1
21-Aug-16|EPI_303|Bin12|Low-Low|Day158|20160824|20161004|20161006|32.4|140|4.536|3.1|1|21.9|3|1

### Step 1 conclusions

* no errors were seen on the PCR machine. Samples assumed to have been cut with MSPI

# Step 2 Bisulfite conversion
* Removed from incubator at 09:45 on 20161207
* Proceeded with EZ DNA Methylation-Gold Kit (Catalog Nos. D5005 & D5006)
[EZ DNA Methylation-Gold Manual](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/DNA_Methylation_Gold_Bisulfite_d5005i.pdf)


### Bisulfite conversion kit prep

* Prepared the **CT Conversion Reagent** for larger DNA samples (30µl) by adding 800µl of water, 300µl of M-Dilution and 50µl of M-Dissolving

* Added 30µl of sample described in table to 120 µl of **CT Conversion Reagent**, mixed by flicking, and spun down
* Placed tubes in PCR machine at 10:45 and set as follows:
	* 98°C for 10 min
	* 64°C for 2.5 hours
	* 4°C forever

* followed protocol steps [EZ DNA Methylation-Gold Manual](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/DNA_Methylation_Gold_Bisulfite_d5005i.pdf)

* Eluted in 12µl of elution buffer

### Bisulfite Conversion ssDNA QC
* 1µl was used to assess fragment size on the bioanalyzer.  

Expected DNA size for Gold kit (A)

![Expected DNA size](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/expected_DNAsize_truseq_meth.jpg?raw=true =400x200)

### Results of bisulfite converted samples
 
20161209

![chip1](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-09_15-06-27.jpg?raw=true =300x300)

* Samples all look good except EPI-44. Will run again

![chip2](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-09_15-34-41.jpg?raw=true =300x300)

* Samples 52, 53, 54, 55, 56 are as expected, samples 151, 152, 153, 154, 159, 160 are shifted to a larger proportion of smaller fragments

![chip3](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-09_16-10-55.jpg?raw=true =300x300)

* Samples are shifted to a larger proportion of smaller fragments

20161211

![chip4](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-12_17-13-19.jpg?raw=true =300x300)

* Samples 185, 188, 193, 200, 205, 206, 208, and 209 are shifted to a larger proportion of smaller fragments  

![chip5](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-12_17-40-14.jpg?raw=true =300x300)

* Samples 214, 229, 230, 235, 236, 242 are shifted to a larger proportion of smaller fragments

![chip6](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-12_18-05-35.jpg?raw=true =300x300)

* Samples 243, 246, 247, 250, 251, 258, 264, 265, and 272 are shifted to a larger proportion of smaller fragments 

![chip7](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_Eukaryote_Total_RNA_Pico_DE72902486_2016-12-12_18-30-34.jpg?raw=true =300x300)

* Sample 275 has abnormal peak around 3000
* Sample 44 was re-reun and still has strange very small fragment size
* Samples 275, 276, 282, 283, 298 are shifted to a larger proportion of smaller fragments 


20161213

# Step 3 Library Prep

[Ilumina TruSeq DNA Methylation Library Preparation Guide](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/truseq-dna-methylation-library-prep-guide-15066014-a.pdf)

Illumina Adapter Sequences
Document # 1000000002694 v01 17 February 2016 
TruSeq DNA Methylation Index PCR Primers
5’ CAAGCAGAAGACGGCATACGAGAT[6 bases]GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT 

* Index 1: ATCACG 
* Index 2: CGATGT 
* Index 3: TTAGGC 
* Index 4: TGACCA 
* Index 5: ACAGTG 
* Index 6: GCCAAT 
* Index 7: CAGATC 
* Index 8: ACTTGA 
* Index 9: GATCAG 
* Index 10: TAGCTT 
* Index 11: GGCTAC 
* Index 12: CTTGTA 

Illumina library prep was completed according to manufacturer's instructions with modifications as described in red text on the protocol and listed below.

* samples eluted in 12µl post BS conversion
* 200µl of 80% ethanol used for rinsing beads
* Samples were stored at -20 for ~24h between _Purify the Tagged DNA_ and _Amplify the Library and Add an Index_ steps
* Library prep was started 20161213
* Library prep was finished 20161213
* Individual barcodes were used for each sample from the Illumina TruSeq DNA Methylation Index PCR Primers (10 reactions, 12 indexes Cat #: EGIDX81312)


**Sample.ID** | **Index.Number** | **Index.Sequence**
---|---|---
EPI_151 | 1 | ATCACG
EPI_152 | 2 | CGATGT
EPI_153 | 3 | TTAGGC
EPI_154 | 4 | TGACCA
EPI_159 | 5 | ACAGTG
EPI_160 | 6 | GCCAAT
EPI_161 | 7 | CAGATC 
EPI_162 | 8 | ACTTGA
EPI_167 | 9 | GATCAG
EPI_168 | 10 | TAGCTT
EPI_169 | 11 | GGCTAC
EPI_170 | 12 | CTTGTA
EPI_175 | 1 | ATCACG
EPI_176 | 2 | CGATGT
EPI_181 | 3 | TTAGGC
EPI_182 | 4 | TGACCA
EPI_184 | 5 | ACAGTG
EPI_185 | 6 | GCCAAT
EPI_187 | 7 | CAGATC 
EPI_188 | 8 | ACTTGA
EPI_193 | 9 | GATCAG
EPI_194 | 10 | TAGCTT
EPI_199 | 11 | GGCTAC
EPI_200 | 12 | CTTGTA
EPI_205 | 1 | ATCACG
EPI_206 | 2 | CGATGT
EPI_208 | 3 | TTAGGC
EPI_209 | 4 | TGACCA
EPI_214 | 5 | ACAGTG
EPI_215 | 6 | GCCAAT
EPI_220 | 7 | CAGATC 
EPI_221 | 8 | ACTTGA
EPI_226 | 9 | GATCAG
EPI_227 | 10 | TAGCTT
EPI_229 | 11 | GGCTAC
EPI_230 | 12 | CTTGTA
EPI_41 | 1 | ATCACG
EPI_42 | 2 | CGATGT
EPI_43 | 4 | TGACCA

### Library Quantification
20161213
Libraries were quantified on the Qubit using the [dsDNA High Sensitivity Kit](https://github.com/hputnam/Putnam_Lab_Notebook/blob/master/protocols/Qubit_dsDNA_HS_Assay_UG.pdf)

* Samples were loaded 1µl of library + 199µl of Qubit dye/buffer mix (1:200)
* Standards were loaded 10µl of standard + 190µl of Qubit dye/buffer mix (1:200)

* Illumina indicates samples should be >3ng/µl


**Sample.ID** | **ng/µl**
---|---
EPI_151 | 0.242 
EPI_152 | 0.486 
EPI_153 | 0.580 
EPI_154 | 0.320 
EPI_159 | 0.356 
EPI_160 | 0.210 
EPI_161 | 0.226  
EPI_162 | 0.930 
EPI_167 | 0.808 
EPI_168 | 0.880 
EPI_169 | 0.500 
EPI_170 | 0.866 
EPI_175 | 0.552 
EPI_176 | 0.676 
EPI_181 | 1.18 
EPI_182 | 0.902 
EPI_184 | 0.956
EPI_185 | 0.972 
EPI_187 | 0.976 
EPI_188 | 1.05 
EPI_193 | 1.74 
EPI_194 | 0.518
EPI_199 | 0.464 
EPI_200 | 0.664 
EPI_205 | 0.312 
EPI_206 | 0.270 
EPI_208 | 0.408 
EPI_209 | 0.114 
EPI_214 | 0.350 
EPI_215 | 1.192 
EPI_220 | 0.888 
EPI_221 | 0.492 
EPI_226 | 1.71 
EPI_227 | 0.796 
EPI_229 | 0.808 
EPI_230 | 0.642 
EPI_41 | 0.314 
EPI_42 | 0.740 
EPI_43 | 0.252

* Library concentration is significantly lower than expected in the majority of the samples 


# Library Quality 
20161214

* 1.0µl of each sample was run on the Agilent DNA High Sensitivity Kit


Illumina DNA Methylation kit expected library size on high sensitivity chip
![expected size](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/expected_librarysize_truseq_meth_.jpg?raw=true =400x200)

[RRBS Chip 1 Data](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_High_Sensitivity_DNA_Assay_DE72902486_2016-12-14_14-05-21.pdf)

![RRBS Chip 1 Data](https://github.com/hputnam/project_juvenile_geoduck_OA/blob/master/Sample_Processing/Gels/2100expert_High_Sensitivity_DNA_Assay_DE72902486_2016-12-14_14-05-21.jpg?raw=true =300x300)

### Conclusions

* Library quality is shifted to a smaller size in libraries that are detectable.
* Given the low concentraiton and poor traces, no further chips were run and the library preps need to be redone.