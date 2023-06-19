---
layout: post
title: Putnam Lab Physiology Chlorophyll Protocol
date: '2023-06-19'
categories: Protocols
tags: [Physiology, Protocol]
---

# Chlorophyll-a Extraction and Quantification from Coral Tissue Homogenate

#### This protocol was adapted from the protocol written by [Danielle Becker and Hollie Putnam](https://github.com/urol-e5/protocols/blob/master/2020-01-01-Chlorophyll-Protocol.md?plain=1) (and [here](https://github.com/Putnam-Lab/Lab_Management/blob/master/Lab_Resources/Physiology_Protocols/Chlorophyll-Protocol.md)) for the Putnam Lab and collaborators in the [E5 project](https://e5coral.org/) with adjustments and images from [Emma Strand](https://github.com/emmastrand/EmmaStrand_Notebook/blob/master/_posts/2019-10-24-Chlorophyll-A-Protocol.md) and [Jill Ashey](https://github.com/JillAshey/JillAshey_Putnam_Lab_Notebook/blob/master/_posts/2023-01-18-Chlorophyll-a.md?plain=1).  Modified from [Wall et al 2018](https://link.springer.com/content/pdf/10.1007%2Fs00227-018-3317-z.pdf).  


### Materials & Equipment 

- 1 mL (**note**: others use 500 uL) of coral tissue homogenate 
- 100% acetone 
- **Quartz** 96 well plate 
- Microcentrifuge 
- P1000 + tips 
- 1.5 mL tubes 
- [Synergy HTX Multi-Mode Microplate Reader](https://www.biotek.com/products/detection-multi-mode-microplate-readers/synergy-htx-multi-mode-reader/)
- [Gen5 Software](https://www.biotek.com/products/software-robotics-software/gen5-microplate-reader-and-imager-software/)


### Protocol 

1. Thaw 1 mL aliquot of sample homogenate
2. Centrifuge the aliquot of adult homogenate for 3 minutes at 13,000 rpm to separate host and symbiont cells. 
3. Remove and discard supernatent. 
4. Add 1 mL of 100% acetone to the pellet. Vortex the tubes for 15 seconds to mix.
5. Put tubes in the 4°C fridge in the dark for 24 hours.
6. Make a plate map for samples, have two wells per samples for duplicates.
7. The following day, take the tubes out of the fridge and vortex for 15 seconds. 
8. Spin tubes for 3 minutes at 13,000 rpm.
9. Using the quartz 96 well plate, pipette 200 µL of 100% acetone into duplicate wells to be used as blanks.
10. Pipette 200 µL of sample to **duplicate** wells of 96-well quartz plate.
11. Cover the plate with silicone pad every 5th sample or so to reduce evaporate as samples are added.  
12. Remove silicon pad.   
13. Follow steps below to measure the Absorbance at 630, 663, and 750 nm in a 96-well quartz plate.

**Measure the Absorbance**  

Follow the [Synergy HTX Operating Manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/synergy_htx_manual.pdf) and [Gen5 Software Manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Gen5_software_manual.pdf) to install the software on your host computer and general operating instructions.

1. Open the Gen5 software on your computer.
2. To create a new protocol, follow the 'Getting Started' section in the [Gen5 Software Manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Gen5_software_manual.pdf).
3. The plate loader should automatically open. Load your plate following the distinctions in the plate loader and you will be all set.
4. To measure Absorbance, select the 'Chlorophyll Protocol' option.
5. Press the green start protocol button in the GEN5 software and allow the protocol to run through the 630, 663, and 750 nm.
6. Export the raw GEN5 software data file and a CSV to the Desktop in a designated folder. Also, immediately upload to a google drive folder to have for future use. 
7. Standardize for path length in 200µl of sample in 96-well quartz plate.

**Calculating Chlorophyll Concentration**  

Chlorophyll a and c2 concentrations are calculated from the equations in [Jeffrey and Humphrey 1975](https://reader.elsevier.com/reader/sd/pii/S0015379617307783?token=0937035D38C07F29ADF00F1F2A21F20F221219B1CC11A444A4F84D16B98EC3A6AD941D191BA2135A68C98BA62A0B69FE) after substracting A750nm from all measurements.  

![Chlorophyll_Equation.png](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/Chlorophyll_Equation.png?raw=true)

Need to correct for differences in path length of the volume in the 96 well plate compared to the 1cm path length of a cuvette.
[Warren 2007](https://www.tandfonline.com/doi/full/10.1080/01904160802135092?casa_token=RqeUl1Ccg7AAAAAA%3A6SyNAs848qrRk1-Tf1g088xWD10z1Xngb8cmcgRvC3jYSYPugr2cL8QG9wFvrFj7xZF-pqqUozonRg)

R code for this analysis can be found at [K. Wong's Github](https://urldefense.proofpoint.com/v2/url?u=https-3A__github.com_kevinhwong1_Thermal-5FTransplant-5F2017-2D2018_blob_master_scripts_ChlorophyllA.R&d=DwMFaQ&c=dWz0sRZOjEnYSN4E4J0dug&r=hzX7Pj5Cn4ufjLQbICvWcOqlrencJyNZMIrmCT00z_o&m=Hpn_SeiBeA7gle40eXLMx3-j3YSrgRHCsOsZ3E5cSGA&s=q5PUrza32gdiEvIa0nI8pMvjeaMw9LFkIDujTh_tGPw&e=).

4. <a name="References"></a> **References**

    1.  [Jeffrey and Humphrey 1975](https://reader.elsevier.com/reader/sd/pii/S0015379617307783?token=0937035D38C07F29ADF00F1F2A21F20F221219B1CC11A444A4F84D16B98EC3A6AD941D191BA2135A68C98BA62A0B69FE)
    2. [Warren 2007](https://www.tandfonline.com/doi/full/10.1080/01904160802135092?casa_token=RqeUl1Ccg7AAAAAA%3A6SyNAs848qrRk1-Tf1g088xWD10z1Xngb8cmcgRvC3jYSYPugr2cL8QG9wFvrFj7xZF-pqqUozonRg)
    3. [Synergy HTX Operating Manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/synergy_htx_manual.pdf)
    4. [Gen5 Software Manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Gen5_software_manual.pdf)
