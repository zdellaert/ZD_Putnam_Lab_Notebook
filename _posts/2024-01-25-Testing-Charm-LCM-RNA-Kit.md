---
layout: post
title: Testing Charm Biotech RNA Extraction on Cryosectioned and LCM-d P. acuta 
date: '2024-01-25'
categories: Processing
tags: [DNA, RNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Charm Kit on P. acuta

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Charm-LCM-RNA-Kit-Protocol/)

## 11/10/23 - Extracting RNA from LCM-captured RNA as well as from cryosections manually dissected fom slides

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM)Sample Total RNA/MicroRNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_RNA_Kit.pdf)

### Sectioning performed on 10/23/23 and LCM on 10/24/23. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-LCM/)

- For the LCM sample, I had to make some adjustments to the protocol. After LCM, I originally resuspended the cells in 50 uL of RNAse/DNAse-free water, but I should have made digestion buffer and resuspended the captured cells in this. To try to make up for this, I made the digestion buffer at 2X concentration of BME and Proteinase K by doing the following:
    - 40 uL buffer RD2 + 9 uL Proteinase K + 2 uL BME
        - I later realized this was actually 4X concentration of BME...
- Then, I followed the protocol as written for FFPE, with a 3 hour digestion at 60 ºC.
- For the other two samples, I removed a cryosectioned slide from -80 ºC (same sample/sectioning round as used for LCM) thawed a slide on dry ice 
    - Rinsed slide in 70% Ethanol for 5 minutes on dry ice
    - Replaced ethanol with RNAse/DNAse-free water to rinse
    - Remove slide to dark background over PCR rack (over dry ice, though be careful to not freeze the water once the volume on the slide is low, if that's freezing move to regular ice) and use sterile razor blade, cleaned with RNAse cleaner, to scrape off tissue sections into a tube filled with prepared RD2 digestion buffer.
    - Then, I followed the protocol as written for FFPE, with a 3 hour digestion at 60 ºC.


#### Qubit Results

- Used Broad range RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 374.78 (S1) & 10451.62 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| LCM sample "C"   |  nd |  nd        |   nd         |
| One Section  |  16.0   |  15.8      |   15.9       |
| Three Sections  |  21.0   |  21.2   |   21.1       |

#### RNA Quality Check: Tapestation

![2023-11-10.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2023-11-10.JPG?raw=true)

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2023-11-10.pdf)


## 1/25/24 - Extracting RNA from cryosections manually dissected fom slides, using frozen tissue protocol instead of FFPE protocol

Used Charm Biotech Just-a-Tube ™ Laser Captured Microdissection (LCM)Sample Total RNA/MicroRNA Purification [Kit](https://www.charmbiotech.com/lcm-rna.htm), [protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Charm_Biotech_LCM_RNA_Kit.pdf)

### Sectioning performed on 10/23/23 and LCM on 10/24/23. See details [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-LCM/)

- Removed a cryosectioned slide from -80 ºC (same sample/sectioning round as used for LCM) thawed a slide on dry ice 
    - Rinsed slide in 70% Ethanol for 5 minutes on dry ice
    - Replaced ethanol with RNAse/DNAse-free water to rinse
    - Remove slide to dark background over PCR rack (over dry ice, though be careful to not freeze the water once the volume on the slide is low, if that's freezing move to regular ice) and use sterile razor blade, cleaned with RNAse cleaner, to scrape off tissue sections into a tube filled with prepared RD1 digestion buffer.
    - Then, I followed the protocol as written for frozen tissue, with a 1 hour digestion at 52 ºC.

#### Qubit Results

- Used Broad range RNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

 RNA Standards: 370.23 (S1) & 9494.15 (S2)

| colony_id | RNA_QBIT_1 | RNA_QBIT_2 | RNA_QBIT_AVG |
|-----------|------------|------------|--------------|
| Charm_Low_Input   |  10.8   |  10.4     |   10.6       |
| Charm_High_Input  |  10.8   |  11.0     |   10.9       |

#### RNA Quality Check: Tapestation

![2024-01-25.JPG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-01-25.JPG?raw=true)

Full results can be found [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/tapestation/2024-01-25.pdf)

### Thoughts:

It seems like the FFPE protocol/RD2 buffer worked better than the frozen one. Maybe we should try the RD2 protocol again but with a shorter incubation? The RIN was higher for the RD2 protocol (for FFPE).

--- 

## Notes and troubleshooting ideas based on Qiagen PAXgene RNA protocols:

Paxgene recommends extracting RNA using the PAXgene Tissue RNA/miRNA [Kit](https://www.qiagen.com/us/products/discovery-and-translational-research/dna-rna-purification/rna-purification/mirna/paxgene-tissue-rna-mirna-kit), [handbook](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Tissue_RNA_miRNA_Kit.pdf)

And has the following notes about extracting using this kit for Paxgene Fixed, Cryoembedded (PFCE) Samples from [sections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_RNA_PFCE_sections.pdf) and [LCM microdissections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_RNA_from_microdissected_PFPE_and_PFCE.pdf).

  - *For DNA: Paxgene recommends extracting DNA using the PAXgene Tissue DNA [Kit](https://www.qiagen.com/us/products/discovery-and-translational-research/sample-collection-stabilization/tissue-ffpe/paxgene-tissue-dna-kit), [handbook](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_Tissue_DNA_Kit.pdf)*
    - *And has the following notes about extracting using this kit for Paxgene Fixed, Cryoembedded (PFCE) Samples from [sections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_gDNA_from_PFCE_sections.pdf) and [LCM microdissections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_gDNA_from_microdissected_PFPE_and_PFCE.pdf).*

### Extracting RNA from PFCE [sections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_RNA_PFCE_sections.pdf):

1. In a labelled 1.5 mL tube, prepare a lysis mixture in the tube by mixing **150 μl Buffer TR1** with *290 μl RNase-free water*. Mix by gently flicking the tube. Add *10 μl Proteinase K*, mix again and centrifuge briefly to collect residual liquid from the sides of the tube.
   - **Pre-cool this lysis mixture on ice**
   - **total volume = 450 ul**
2. Using a cryostat, make a tissue section of 8–12 μm thickness from the PFCE tissue.
3. Using pre-cooled forceps, transfer the PFCE tissue section into the lysis reagent cooled on ice and mix by vortexing for 5 s.
4. If required, repeat steps 2 and 3 for a maximum of 3 sections.
5. **Incubate on a shaker–incubator for 15 min at 56°C and 1400 rpm.**
6. Centrifuge for 3 min at maximum speed (but do not exceed 20,000 x g).
7. Carefully transfer the supernatant to a new 1.5 ml microcentrifuge tube without disturbing the pellet.
8. Continue with the addition of ethanol in step 12 of the protocol “Purification of Total RNA from Sections of PFPE Tissue” in the PAXgene Tissue RNA Kit Handbook (page 17).
   - Supernatant volume: **450 uL** 
   - What are those following steps:
     1. Add 675 μl isopropanol (**~roughly 2x volume**). Mix by vortexing for 5 s, and centrifuge briefly (1–2 s at 500−1000 x g) to remove drops from the inside of the tube lid.
     2. Pipet up to 700 μl sample, including any precipitate that may have formed, into a PAXgene RNA MinElute spin column. Centrifuge for 1 min at 8000 x g. Discard the flow-through.
     3. Repeat
     4. Wash TM2
     5. DNAse digestion
     6. Keep DNase flow through, mix with 350 TM2, reapply
     7. Wash TM3
     8. Wash Ethanol
     9. Dry column
     10. Elute

### Extracting RNA from PFCE [microdissections](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Paxgene_RNA_from_microdissected_PFPE_and_PFCE.pdf):

<u>**Manual microdissection (from slides)**</u>

1. In a labelled 1.5 mL tube, prepare a lysis mixture in the tube by mixing **60 μl Buffer TR1** with *290 μl RNase-free water*. Mix by gently flicking the tube. Add *10 μl Proteinase K*, mix again and centrifuge briefly to collect residual liquid from the sides of the tube.
   - **Pre-cool this lysis mixture on ice**
   - **total volume = 360 ul**
2. Section tissue onto slides, 6-12 um thick sections
   - **make sure slides are RNAse free....**
3. Remove embedding medium and stain (optional) according to the [Supplementary Protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/HB-1543-S01-001_PX20_SP_TIssue_System_Preparation_of_sections_from_PFPE_and_PFCE_tissues_for_manual_or_LMD_1015_WW.pdf)
   - 1 minute in 70% Ethanol
   - 45 s in 50% Ethanol
   - 30 s in 30% Ethanol
   - **Keep freshly prepared slides in ice-cold ethanol until microdissection.**
4. For manual microdissection, remove the slide from the ethanol. Using an absorbent sheet, wipe away the liquid on the slide that surrounds the tissue section.
5. Place the slide on a horizontal working plate and overlay it with *100 μl ice-cold Buffer TR1*. Make sure that the whole section is covered.
   - What is a horizontal working plate?! 
6. Detach the tissue from the slide by pipetting the lysis mixture up and down. Transfer the tissue and all liquid to the labeled 1.5 ml safelock microcentrifuge tube from step 1 and mix by vortexing for 5 s.
   - **total volume = 460 ul**
7. **Incubate on a shaker–incubator for 15 min at 56°C and 1400 rpm.**
8. Centrifuge for 3 min at maximum speed (but do not exceed 20,000 x g).
9.  Carefully transfer the supernatant to a new 1.5 ml microcentrifuge tube without disturbing the pellet.
      - **Supernatant contains RNA**
10. Continue with the addition of ethanol as described in step 12 of the protocol “Purification of Total RNA from Sections of PFPE Tissue” in the PAXgene Tissue RNA Kit Handbook (page 17).
   - Supernatant volume: **460 uL** 

<u>**Laser capture microdissection (LCM)**</u>

1. Using a Laser Microdissection System, dissect a tissue area of ≥5000 μm^2 (≥50 cells) from the PFCE LMD slide.
2. Collect cells directly into a dedicated **collection tube filled with 15 μl Buffer TR1 *with BME*** (e.g., use the cap of a 0.5ml PCR tube when using a Leica LMD system).
   - **Buffer TR1 should be pre-cooled**
   - Note: If not possible, add Buffer TR1 immediately after collecting the cells. Make sure to add β-ME to Buffer TR1 before use (see “Things to do before starting”).
3. Add **65 μl Buffer TR1**. Mix by vortexing for 30 s and centrifuge briefly (1–2 s at 500–1000 x g) to remove drops from the tube lid.
   - **Buffer TR1 should be pre-cooled**
   - Note: The volume of Buffer TR1 depends on the collection vessel used for microdissection, but **should not exceed 80 μl**. Lysates in Buffer TR1 can be frozen at –80°C, however, freezing may impact RNA yield when a low number of cells is used. Thaw frozen lysates on ice and proceed with step 6.
4. If processing <5000 cells, 20 ng carrier RNA (5 μl of a 4 ng/μl solution) may be added to the lysate. Prepare the carrier RNA as described in “Things to do before starting”.
5. Add 145 μl RNase-free water and 5 μl Proteinase K and mix by vortexing for 5 s.
   - Note: Do not mix Buffer TR1 and Proteinase K before adding them to the sample.
   - Total volume: 80 + 145 + 5 = **230 uL** 
6. **Incubate on a shaker–incubator for 15 min at 56°C and 1400 rpm.** After incubation, centrifuge briefly (1–2 s at 500–1000 x g) to remove drops from the tube lid.
7.  Transfer the sample and Buffer TR1 to a 1.5 ml safelock microcentrifuge tube (not provided).
8.   Continue with the addition of ethanol as described in step 12 of the protocol “Purification of Total RNA from Sections of PFPE Tissue” in the PAXgene Tissue RNA Kit Handbook (page 17).
   - Supernatant volume: **230 uL** 

#### From this I get:

- Lysis buffer is called TR1 with added BME
  - guanidine-containing buffer
  - Add 10 μl BME per 1 ml Buffer TR1  
- **Pre-cool lysis buffer** mixture, and use about 450 uL for max 3 sections, 460 uL total for manual dissections from slides, and 230 uL for LCM samples
- Pre-cool forceps
- **Incubate on a shaker–incubator for 15 min at 56°C and 1400 rpm.**
  - try this with the charm kit
- Then, to the supernatant, they add isopropanol and it goes into columns
  - could try this protocol with the AllPrep Qiagen kit

#### Potential to use Carrier RNA?

"The PAXgene Tissue RNA Kit contains poly-A RNA for use as carrier RNA. When added to lysates from microdissected tissue, the carrier RNA may improve the recovery of total RNA. Carrier RNA is not required when processing more than 5000 cells. The small amounts of poly-A RNA used as carrier RNA do not interfere with subsequent RT-PCR, even when oligo-dT is used as a primer for reverse transcription. Reverse-transcription reactions typically contain an excess of oligo-dT primers, and the small amounts of poly-A used as carrier RNA are insignificant in comparison. Total RNA purified using poly-A RNA as carrier RNA can be amplified with the QIAGEN® QuantiTect® Whole Transcriptome Kit, which uses a mix of random and oligo-dT primers."
   - "When processing <5000 cells, carrier RNA may be added to the lysate (see “Carrier RNA”, page 2). Before using carrier RNA for the first time, dissolve it (310 μg) in 1 ml RNase-free water. Store this stock solution at –20°C and use it to make fresh dilutions for each set of RNA preparations. The concentration of this stock solution is 310 ng/μl. Prepare a working solution of 4 ng/μl using Buffer TR1."

### Other important notes: What about improving sample prep?

revisiting helpful vidoes and references from my [cryosectioning protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Cryosectioning-Protocol/)

[Roy et al 2020 Bioprotocols](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/BioProtoc-10-01-3475.pdf)

- Sectioning tips:
    - [Video](https://www.youtube.com/watch?v=aNrnnmQB8y0)
    - [Video 2](https://www.youtube.com/watch?v=qUBoyIN65vA)
    - [Video 3](https://www.youtube.com/watch?v=3s3zeRCwQyE&list=PLfaSRwcfHcq0D8RTy9LR8sKsWcF6C8TAt&index=5)
    - ["Where to put hands"](https://bitesizebio.com/28466/can-stand-cold-cryosectioning-beginners/)
    - [Anti-roll plate leica manual](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Leica_AntiRoll.pdf)

- [Paxgene protocol](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/HB-1543-S01-001_PX20_SP_TIssue_System_Preparation_of_sections_from_PFPE_and_PFCE_tissues_for_manual_or_LMD_1015_WW.pdf)

- [Helpful notes about cryosectioning for LCM](https://www.thermofisher.com/us/en/home/references/ambion-tech-support/rna-isolation/general-articles/getting-intact-rna-from-lcm-samples.html)

## Game Plan as of 1/26/24:

Next week Monday, I will embed and section more Pocillopora tissue with the modifications listed below and try to extract RNA from cryosectioned slides same day, using the modified protocol below. I will also dry and freeze slides and attempt to extract RNA from those slides the next day, to see if desiccating slides and reducing condensation during thawing helps improve RNA quality.

Simultaneously, I am decalcifying fixed Porites and Montipora to move forward with learning how to section these more difficult tissues and then will start optimizing the RNA extraction protocol for these species (and Seriatopora, easy to section) as well.
s
Modifications to protocol below:

1. Modifications to Charm Extraction Protocol
   1. **Pre-cool lysis buffer** mixture
   2. Use increased volume of lysis buffer mixture for whole sections
      1. 100 uL lysis buffer mixture, 200 uL RB7
   3. Pre-cool forceps and razor blades for transferring tissue to lysis buffer
   4. **Incubate on a shaker–incubator for 15 min at 56°C and 1400 rpm.**
      1. instead of 1 hour at 52 ºC or 3 hours at 60 ºC. Feels like a big jump, but seems like PAXgene isn't crosslinking RNA based off of their RNA extraction protocols.
   5. Stain and wash all slides and perform dissections in petri dishes (or 96-well plate lids) cleaned to be RNAse free
2. Improve sample prep for all sectioned tissues.
   1. Use dessicants to dry slides before they go into -80 ºC
      1. Cut sections onto slide, then air dry PEN slide at room temp for 2 minutes on dessicant ([Roy et al 2020 Bioprotocols](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/BioProtoc-10-01-3475.pdf))
      2. **If staining, transport slides to lab in ice cold ethanol**
         1. Dehydrate in ethanol series and perform staining
            1. Stain and wash all slides and perform dissections in petri dishes (or 96-well plate lids) cleaned to be RNAse free
            2. 2 minute in ice-cold 70% Ethanol
            3. 45 s in ice-cold 50% Ethanol
            4. 30 s in ice-cold 30% Ethanol
            5. if there is excess OCT, dip slide in ice-cold RNAse free water 5-6 times over 1-2 mins
         2. Staining: cresyl violet or H&E
            1. incubate in CV-staining solution for 30 secs
               1. dissolve solid CV at 1% w/v in 50% ethanol. Stir overnight at room temp. filter before use
            2. remove stain from slide on absorbant surface
            3. Rinse 3x in ice-cold 70% ethanol for washing
            4. Rinse 3x with ice-cold 100% ethanol
            5. **Dry on dessicator for 1-2 minutes, use immediately for LCM or store at -80 ºC**
      3. If able to perform LCM day of, perform immediatley after dessication or **keep freshly prepared slides in ice-cold ethanol until microdissection.**
            1. Dry slides again on dessicator right before LCM if needed
      4. **If not able to perform LCM day of**, store dried slide at -80 ºC in a slide mailer in vaccum bag (or just in a falcon tube?) containing dessicant
         1. day of, take slide in container with desiccant out of -80 ºC and allow  to slowly reach room temperature, for at least 60 min, before opening ([Roy et al 2020 Bioprotocols](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/BioProtoc-10-01-3475.pdf))
3. Improvements to LCM sample collection protocol, [Roy et al 2020 Bioprotocols](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/BioProtoc-10-01-3475.pdf)
      1. "Clean the collect tube caps (0.5 ml) with RNaseZap, followed by a rinse with RNase-free water."
      2. Immediately add lysis buffer to the collection caps, close the cap upside down and vortex for 1 min.
      3. Centrifuge and store tubes at -80 °C.

To order to make game plan happen, trying to get good RNA out of sections (not even LCM yet):
1. Dessicants
2. Dessicator (glass jar)
3. Cresyl violet stain (maybe? unclear if we need any stain to visualize what we care about dissecting)