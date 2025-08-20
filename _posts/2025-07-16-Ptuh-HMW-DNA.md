---
layout: post
title: Extracting HMW DNA for P. tuahiniensis Genome with Qiagen Genomic Tip Protocol
date: '2025-07-16'
categories: Protocols, Processing
tags: [DNA, Pocillopora, E5]
---

# Extracting HMW DNA for P. tuahiniensis Genome, sample POC-222

Jill Ashey and I successfully extracted HMW DNA for the genome on 7/15/25. I originally posted about this [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Pocillopora-HMW-Genome/). The detailed protocol is [here](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/HMW-Tip-Protocol/) and here are example steps and results for [P. meandrina](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/pm-HMW-2/) and [P. acuta](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/pacuta-HMW/). 

Important notes specific to this extraction: 

- We used [NEB RNAse A](https://www.neb.com/en-us/products/t3018-monarch-rnase-a?srsltid=AfmBOoriTpLHKWFX6PPJ4wNstB0RuPdygmCw7G4JJ8ZqJ-ReokcniGSh), which is at a concentration of 1/5th the Qiagen one, so we added 95 uL instead of 19 ul to the digestion buffer
- We used [Zymo Proteinase K](https://www.zymoresearch.com/products/proteinase-k-w-storage-buffer-set?srsltid=AfmBOoqnDzZFFjOVpndzfZn0elRhOi3YC07GgB1-vny8PV-RXMkDqaZP)
- We measured 1.8059 g chunk of coral from the "Molec 1" whirlpak sample of POC-222 from the January timepoint (TP1, 20200103). This coral is from site 2.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/whirlpak.jpeg?raw=true" height="500">

## Following Genomic Tip High Molecular Weight DNA Extraction [Protocol written by Maggie Schedl](https://github.com/meschedl/MESPutnam_Open_Lab_Notebook/blob/master/_posts/2021-04-18-HMW-Tip-Protocol.md).

Much of the text below is copied straight from this protocol, but modified to reflect exactly what I did.

#### This protocol is used to extract high molecular weight (very very long fragments) of DNA from tissues (typically flash frozen). It is typically done with 1 sample at a time. Usually this is for nanopore/long read sequencing, such as for generating a genome. Usually the aim is to get a very large amount of DNA as well, up to 25-30ug (25,000-30,000ng).

### Materials and Equipment

- [QIAGEN Genomic-tip 100/G](https://www.qiagen.com/us/products/discovery-and-translational-research/dna-rna-purification/dna-purification/genomic-dna/qiagen-genomic-tip-100g/#orderinginformation)
- [QIAGEN Genomic DNA Buffer Set](https://www.qiagen.com/us/products/discovery-and-translational-research/dna-rna-purification/dna-purification/genomic-dna/blood-and-cell-culture-dna-midi-kit/#orderinginformation)
- [QIAGEN RNase A (100mg/mL concentration)](https://www.qiagen.com/us/products/discovery-and-translational-research/lab-essentials/enzymes/rnase-a/?clear=true#orderinginformation)
  - *We used [NEB RNAse A](https://www.neb.com/en-us/products/t3018-monarch-rnase-a?srsltid=AfmBOoriTpLHKWFX6PPJ4wNstB0RuPdygmCw7G4JJ8ZqJ-ReokcniGSh)*, which is at a concentration of 1/5th the Qiagen one, so we added 95 uL instead of 19 ul to the digestion buffer.
- [QIAGEN Proteinase K](https://www.qiagen.com/us/products/discovery-and-translational-research/lab-essentials/enzymes/qiagen-proteinase-k/?clear=true#orderinginformation)
  - *We used [Zymo Proteinase K](https://www.zymoresearch.com/products/proteinase-k-w-storage-buffer-set?srsltid=AfmBOoqnDzZFFjOVpndzfZn0elRhOi3YC07GgB1-vny8PV-RXMkDqaZP)*
- [DNA lo-bind tubes](https://online-shop.eppendorf.us/US-en/Laboratory-Consumables-44512/Tubes-44515/DNA-LoBind-Tubes-PF-56252.html)
- Ceramic mortar and pestle
- Forceps and scrapper (and maybe clipper, depends on your sample)
- Temperature controlled centrifuge (must go to 4 degrees C)
- Thermomixer (not 100 necessary if you have the incubator)
- TE buffer
- Rocking incubator (Incubator Genie)
- Orbital shaker
- Liquid Nitrogen
- Balance/scale
- Pipettes
- Filter pipette tips
- Wide bore pipette tips
- 100% isopropanol
- 70% ethanol

**Important Notes about HMW DNA**

- HMW DNA is very fragile, pipetting or vortexing can sheer it easily
- Do not vortex after extraction, to mix the samples flick gently then spin down
- Whenever you are pipetting the actual sample (ie, not buffers) you should use wide bore pipette tips, these are next to the kit on the Putnam shelf. They have a larger opening to the tip and are gentler
- **Do not freeze the DNA**, freeze thaws can break up the long fragments, keep HMW DNA in the 4 degree fridge for storage
- HMW DNA can really clump, especially in this extraction method that pellets it in a precipitation. For quantifying with the Qubit, take a top and bottom of the tube 1ul: do 2 Qubits for each sample and average them together for the whole tube concentration

## Protocol

### Set up

- Bring the balance to the bench you'll work at
- Set the incubator genie to 50 degrees C
- Make a 50mL conical with 9.5mL of Buffer G2 (in genomic buffer set) and 19ul of RNase A (**95 uL of NEB RNase A at 20 mg/ml**). Vortex and spin down to mix
- Clean the forceps and scrapper (and clipper if needed) with 10% bleach, DI, and 70% ethanol, then place on dry ice or in the -80 to chill down
- Put the mortar and pestle on dry ice or in the -80 to chill down
- Use the Prada or Puritz lab Thermoflask and fill with Liquid Nitrogen (you don't need a lot, less than 1/4 full)

### Tissue Grinding and Incubation

- Place the chilled mortar and pestle on the balance and tare
- Clip or use forceps to put the tissue piece in the pestle while on the scale, a weight between 0.5 and 1.5g (depending on how much tissue you see and how much skeleton) is good
- Take the pestle off the balance and pour in some LN2
- Wait for the liquid to boil off
- Grind the tissue until powdery, this can be hard with the skeleton. Use latex palm gloves to hold the very cold mortar and pestle. Use more LN2 if needed to keep the powder powdery and not a paste

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/powder_1.jpeg?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/powder_2.jpeg?raw=true" height="500">

- Use the scrapper to scrape the tissue powder into the 50mL conical with the buffer G2 mix
- Vortex the 50mL conical
- Add 500ul of Protienase K to the conical
- Vortex the conical again
- Place the conical (on a rack) in the incubator genie at 50 degrees C and set to rocking speed 15. Incubate for 2 hours

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/jill.jpeg?raw=true" height="500">

### Genomic Tip Extraction

- With 10 minutes left in the incubation, set the cold centrifuge to 4 degrees C and run for 10 minutes (brings temp down)
- After incubation, transfer 1mL of lysed tissue liquid into each of **8** 1.5mL DNA lo-bind tubes with wide bore pipette tips
  - the amount of tubes depends on your tissue:debris ratio, I usually get around 8.
- Centrifuge at 4 degrees C for 10 minutes at 5000 rcf to pellet any extra debris
- While that is centrifuging, set up one Qiagen Genomic tip column (long column with resin filter) inside the blue holder (holds it in the tube rack) over a 50mL conical
- Add 4mL of equilibration buffer (QBT) to the resin column with filter tips and let it drip through the column, this should be done about when the centrifugation is done
- After the centrifugation there may be a pellet of debris in each tube
- Then add the supernatant from the 8 sample tubes to the resin tip with wide bore pipette tips and let drip through the column. This can take anywhere from 7 to 40 minutes depending on the sample/species etc. No pressure is applied to the column, it just drips
- When it is finished, switch out the 50mL conical underneath for a new one. Pour the liquid into a labelled waste container and dispose of the conical.
- Add 7.5mL of wash buffer (QC) and let drip through the column. This can take 5 to 15 minutes
- Pipette 5mL of elution buffer (QF) to a 5mL tube and put in the incubator genie to warm up to 50 degrees C
- After the first wash, add another 7.5mL of wash buffer (QC) and let drip through the column
- When it's done, transfer the resin tip to a different 50mL conical
- Add the 5mL of warmed buffer QF and let drip through

### Isopropanol Precipitation of DNA

- Set up 6 DNA lo-bind tubes with all of the final labeling on them. Depending on how much liquid came out of the column you may need 6 or 7 tubes.
- Add 833ul of the eluted liquid (from the last drip out of the resin column) to each new lo-bind tube. There might not be enough for the last tube to have 833ul, so measure however much liquid you do put in that tube.
  - **For this extraction, I had 5 tubes with 833 uL and a 6th tube with 920 uL.**
- One tube at a time, add 0.7 volumes of 100% isopropanol to each DNA low-bind tube and gently invert to mix ~10 times. For tubes that had 833ul of sample, 0.7 volumes is 583ul of isopropanol. If you have a tube with less than 833ul, calculate out what 0.7 times that volume is
  - I added 538 uL to tubes 1-5 and 644 uL to tube 6 (this was pushing the volume of the 1.5mL tube though)
- Sometimes you can see DNA precipitate already here, but sometimes not
- Centrifuge the lo-bind tubes for 30 minutes at 4 degrees C, 10,000 rcf
- Put a conical of 70% ethanol (you only need 1 mL per tube) in the -20 freezer to cool down while the samples are centrifuging. When ready to use, put it on an ice bucket at the bench
- Look for pellets after centrifuging, should be whitish, could be very small
- Keep the tubes in the cold centrifuge when not working with them
- One tube at a time, take them out of the centrifuge and remove most of the supernatant, not disturbing the pellet. Supernatant can go in a waste basin
- To one tube at a time, add 1mL of cold 70% ethanol and place back in the centrifuge
  - Maggie says to vortex but I do not vortex here in case the pellets are loose
- Centrifuge tubes for 10 minutes at 4 degrees C 10,000 rcf
- After centrifugation, remove all of supernatant when finished, used a p20 to get small volumes out. Do the best you can to not disturb the pellet. If you cannot see a pellet, act like there is one there
- Leave the caps open and let any extra ethanol air dry for 7 minutes
- Add 50ul of TE buffer to each tube, gently
- Place each tube in the Thermomixer for 1 hour at 55 degrees C **no shaking**
- Place the tubes in a tube rack on the orbital shaker for overnight, 200rpm. Qubit and TapeStation the next day. If it is a Friday, put the tubes on the shaker as long as you can, then place them in the 4 degree C fridge for the weekend. Before Qubit the next Monday, put them on the shaker for an hour

## QC

### What is our goal for amount of DNA?

- From the sequencing facility (BYU, through genohub): "Three micrograms of DNA should be provided to enable library construction and Blue-Pippin size selection for large fragment whole genome libraries"

- (Danielle's post said: For PacBio we need 10-20ug of genomic DNA (as quantified by Qubit) in less than 400ul. Quality of the DNA should be over 40kb in size, though we can remove smaller fragments.)


### Qubit

- Use the broad range DNA assay and [protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Qubit-Assay-Protocol.md)
- Quantify both the top and bottom of each tube and then use the averages of each tube for the final concentration

DNA Standards: 189.27 (S1) & 21484.19 (S2)

| Tube Number | Top Read 1 (ng/uL) | Top Read 2 (ng/uL) | Bottom Read 1 (ng/uL) | Bottom Read 2 (ng/uL) | Average (ng/uL)          | Amount in tube (*47 uL) |
|-------------|--------------------|--------------------|-----------------------|-----------------------|--------------------------|-------------------------|
| 1 | 68.6 | 70.4 | 72.2 | 73   | 71.05  | 3339.35  |
| 2 | 118  | 118  | 124  | 123  | 120.75 | 5675.25  |
| 3 | 158  | 159  | 158  | 159  | 158.5  | 7449.5   |
| 4 | 34.2 | 31.8 | 34.4 | 32.6 | 33.25  | 1562.75  |
| 5 | 98   | 91   | 100  | 93.4 | 95.6   | 4493.2   |
| 6 | 38.4 | 33.4 | 36.6 | 30.8 | 34.8   | 1635.6   |
|             |                    |                    |                       |                       | Total DNA extracted (ng) | 24155.65       |
|             |                    |                    |                       |                       | **Total DNA extracted (ug)** | **24.1556**5    |

**AMAZING QUANTITY! YAY!**

### TapeStation

- For accurate sizing, we use the TapeStation instead of a gel. However it still isn't the absolute best, the best thing for HMW DNA is a pulse-phase gel that's run super slowly and alternates the position of the current to separate out the large fragments. You can look at [pictures](https://international.neb.com/monarch/high-molecular-weight-dna-extraction), pretty cool. However, we don't have the type of gel box for that!
- Use the **Genomic DNA** screentapes and reagent/ladder. This reads from 48,000bp to 100bp
- Follow the [protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/DNA-Tapestation/)
- Your goal is to have a huge peak at the 60,000bp size or around there, and very minimal smearing elsewhere
- Good trace:
![](https://raw.githubusercontent.com/meschedl/MESPutnam_Open_Lab_Notebook/master/images/Screen%20Shot%202021-04-18%20at%204.59.16%20PM.png)
- Bad trace:
![](https://raw.githubusercontent.com/meschedl/MESPutnam_Open_Lab_Notebook/master/images/Screen%20Shot%202021-04-18%20at%205.04.25%20PM.png)

#### Results: Hmm, this is weird.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/Screenshot%202025-07-16%20at%2011.48.38.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/Screenshot%202025-07-16%20at%2011.48.43.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/Screenshot%202025-07-16%20at%2011.48.54.png?raw=true" height="500">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2025-07-16_Ptuh_HMW.pdf)

### Gel:

Run by [Natalie](https://github.com/nchampney/NEC_Putnam_Lab_Notebook/blob/master/_posts/2025-07-16-TimeSeries-DNA-RNA-Extractions.md) at 80 volts for 45 minutes

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-16-Timeseries-gel.jpg?raw=true" height="500">

## Thoughts on the degradation:

### Scenario 1

1. If I'm being an optimist, I can hope that the DNA is all there but I didn't homogenize it fully enough so it's not being pipetted into the tapestation/gel and only the smallest fragments are being quantified and visualized. If we believe this, then this should be solved by trying to [homogenize the DNA further](https://www.neb.com/en-us/tools-and-resources/usage-guidelines/homogenization-of-high-molecular-weight-dna-hmw-dna-samples-after-elution), by pipetting up and down with wide bore tips and other means.

### [Homogenization guide from NEB](https://www.neb.com/en-us/tools-and-resources/usage-guidelines/homogenization-of-high-molecular-weight-dna-hmw-dna-samples-after-elution)

#### For Samples Agitated at Low Speeds (UHMW DNA) 

  *Samples isolated following agitation with low speeds are extremely viscous and require additional effort to relax and homogenize before analysis and use*. When homogenized completely, samples will appear consistent throughout the tube and OD measurements will become more consistent. The following steps are recommended: 

  - After elution, **pipette up and down 5–10 times using a 200 µl wide bore pipette**; ensure any clumps of DNA are dispersed.  
  - Incubate DNA samples for 30–60 minutes at 37°C. 
  - Pipette up and down 5–10 times again using the same wide bore pipette tip. 
  - Repeat 1–2 times each day for at least 2 days. 

If quantitation of UHMW DNA remains challenging following the above steps, needle shearing is recommended prior to spectrophotometric measurement.  

### Scenario 2

2. Maybe more realistically, this could be what all the DNA looks like. This could be due to a variety of factors:
   1. Thawing of the frozen tissue fragment during transit or other time
      1. Solution: try a different whirlpak (timepoint) from the same corla
   2. Too much tissue input for the digestion buffer amount led to degradation during the digestion 
      1. Solution: use less input
   3. Heating during elution led to degradation
      1. In Maggie's workflow, she always elutes the DNA pellet at 55 ºC for one hour, but NEB recommends not exceeding 30 minutes at this temperature.
      2. Solution: try reducing 55 ºC incubation time; also try doing the incubation in the incubator genie instead of thermomixer, this can be gentler

From [NEB](https://www.neb.com/en-us/tools-and-resources/usage-guidelines/homogenization-of-high-molecular-weight-dna-hmw-dna-samples-after-elution):

- Heat 
  - Heat will reduce the viscosity of the solution and significantly increase the speed of homogenization of HMW DNA solutions. Below are some additional guidelines when using heat: 
    - Temperatures > 60°C are generally not recommended as they will lead to DNA denaturation and degradation.  
    - **Incubation at 56°C, the temperature used for elution, is appropriate only for short incubation times. Do not exceed 30 minutes.**  
    - Samples can be incubated at 37°C for several hours safely; DNA integrity will not be affected. 
    - Incubation at room temperature overnight facilitates even homogenization of the DNA. 
    - Incubation at 4°C for days or weeks also facilitates homogenization and relaxation of HMW DNA. 

## July 18, 2025 Try

We are trying again with a fragment from a different timepoint in the hopes that it was better preserved and did not experience the potential thawing that the other timepoint did. 

- We measured 1.5769 g chunk of coral from the "Molec 1" whirlpak sample of POC-222 from the September timepoint (TP3). This coral is from site 2.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-18-whirlpak.jpeg?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-18-mass.jpeg?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-18-powder-1.jpeg?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-18-powder-2.jpeg?raw=true" height="500">

### Qubit

- Use the broad range DNA assay and [protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Qubit-Assay-Protocol.md)
- Quantify both the top and bottom of each tube and then use the averages of each tube for the final concentration

DNA Standards: 189.47 (S1) & 25689.24 (S2)

| Tube Number | Top Read 1 (ng/uL) | Top Read 2 (ng/uL) | Bottom Read 1 (ng/uL) | Bottom Read 2 (ng/uL) | Average (ng/uL)          | Amount in tube (*47 uL) |
|-------------|--------------------|--------------------|-----------------------|-----------------------|--------------------------|-------------------------|
| 1 | 8.1  | 8.36 | 8.9  | 9.1  | 8.615  | 404.905 |
| 2 | 11.3 | 11.1 | 9.04 | 9.06 | 10.125 | 475.875 |
| 3 | 8.86 | 8.88 | 8.84 | 8.86 | 8.86   | 416.42  |
| 4 | 7.26 | 7.18 | 6.68 | 7.16 | 7.07   | 332.29  |
| 5 | 6.76 | 6.82 | 6.78 | 6.78 | 6.785  | 318.895 |
| 6 | 9.84 | 9.74 | 9.78 | 9.78 | 9.785  | 459.895 |
|             |                    |                    |                       |                       | Total DNA extracted (ng) | 2408.28      |
|             |                    |                    |                       |                       | **Total DNA extracted (ug)** | **2.408**    |

### Tapestation

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-20_Ptuh_HMW_1.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-20_Ptuh_HMW_2.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-20_Ptuh_HMW_3.png?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-07-20_Ptuh_HMW_4.png?raw=true" height="500">

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2025-07-20_Ptuh_HMW.pdf)

## Potential gDNA already extracted by KXT:

Master extraction sheet: https://docs.google.com/spreadsheets/d/1A764av1a3VORX6m9aDUEcoY9Bx9l0fvGtV5ycm2J9Wo/edit#gid=0

- for POC-222, all tubes of DNA were sent to Azenta for WGBS
  - Tubes: 65, 305, 555, 879
- Potential extractions that had high quantity and were not sent to Azenta:
  - Tube 321, TP2 POC-238 extracted 20211018
  - Tube 325, TP2 POC-248 extracted 20211007
  - **BOTH RUN ON TAPESTATION 7/20 BUT BOTH P. meandrina :/ ** (see above)
- Potential acutally *P tuaheniensis* ones:
  - Tube 727, TP4 POC-48 extracted 20211018
  - Tube 417, TP2 POC-57 extracted *by JA* on 20240816
  - Tube 643, TP3 POC-48 extracted 20210930
  - Tube 655, TP3 POC-43 extracted 20210930
  - Tube 773, TP4 POC-44 extracted 20210907
  - Tube 179, TP1 POC-68 extracted 20211115
  - Tube 695, TP3 POC-47 extracted 20211001

## August 19 Attempt

We are trying again with a fragment from the September timepoint, but with newly ordered Genomic DNA buffers to see if there is a chance the 5-year old buffers could be causing an issue. If this extraction yields degraded DNA, we will need a different approach or new samples.

- We measured 2.2229 g chunk of coral from the "Molec 1" whirlpak sample of POC-222 from the September timepoint (TP3). This coral is from site 2.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-08-19_Ptuh_HMW_1.JPEG?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-08-19_Ptuh_HMW_2.JPEG?raw=true" height="500">
<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/random/HMW_Ptuh/2025-08-19_Ptuh_HMW_2.JPEG?raw=true" height="500">

### Qubit and TS will be done on 8/21.

- Use the broad range DNA assay and [protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Qubit-Assay-Protocol.md)
- Quantify both the top and bottom of each tube and then use the averages of each tube for the final concentration

DNA Standards: XXXX (S1) & XXXX (S2)

| Tube Number | Top Read 1 (ng/uL) | Top Read 2 (ng/uL) | Bottom Read 1 (ng/uL) | Bottom Read 2 (ng/uL) | Average (ng/uL)          | Amount in tube (*47 uL) |
|-------------|--------------------|--------------------|-----------------------|-----------------------|--------------------------|-------------------------|
