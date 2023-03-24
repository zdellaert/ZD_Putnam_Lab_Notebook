---
layout: post
title: 2023-03-14 PCR Protocol
date: '2023-03-14 16:00:00'
categories: Protocol
tags: [DNA, Porites, Pocillopora]
---

## PCR Protocol for POC and POR Species ID (Can be modified for other primers)

See [base protocol and notes from Hollie](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/SpeciesID-via-PCR-Sanger-Sequencing.md). This protocol format is based off of [Maggie's](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/mtORF-protocol/), with adjustments to the protocol in advisement from Kristina (notable differences: no diluting DNA beforehand and strip tubes instead of plates).

#### Goal

Amplify the mtORF region (mitochondrial open reading frame) of _Pocillopora_ and _Porites_ coral DNA using PCR (polymerase chain reaction). Then use amplification product for Sanger Sequencing and determination of _Pocillopora_ coral species. Primer sequences and concept developed in [Johnston et. al 2018](https://peerj.com/articles/4355/) and [Tisthammer et al 2020](https://peerj.com/articles/8550/).

Information on Sanger sequencing at the URI GSC is [here](https://web.uri.edu/gsc/sanger_sequencing/). Sequencing takes place after 10am on Tuesdays and Thursdays, so samples need to be dropped of before 10am on those days.  

#### Materials and Equipment

- Primers (orderable from IDT), see specific primers for each species below, stored in -20 ºC
- [EmeraldAmp® GT PCR Master Mix Cat # RR310A RR310B](https://www.takarabio.com/documents/User%20Manual/RR310A_DS.v1902Da-a_116982.pdf), stored in -20 ºC
- [Ultrapure free water/PCR grade water](https://www.fishersci.com/shop/products/invitrogen-ultrapure-dnase-rnase-free-distilled-water-2/10977015#?keyword=ultrapure+water), stored in -20 ºC
- Thermocyler

----------------

## _Pocillopora_

### mtORF: [Johnston _et al._ 2018](https://peerj.com/articles/4355/)

#### mtORF Primers

FatP6.1 5′-TTTGGGSATTCGTTTAGCAG-3′    
RORF 5′-SCCAATATGTTAAACASCATGTCA-3′

#### mtORF PCR profile

1 cycle: 94 °C for 60 s   
30-40 cycles: 94 °C for 30 s, 53 °C for 30 s, and 72 °C for 75 s   
1 cycle: 72 °C for 5 min.  

### PocHistone 3 region: [Johnston _et al._ 2018](https://peerj.com/articles/4355/)

DNA from individuals of mtORF type 1 (_P. meandrina_ and _P. eydouxi_) need also to be amplified using novel primers for the histone 3 region

#### PocHistone Primers
PocHistoneF: 5′-ATTCAGTCTCACTCACTCACTCAC-3′ 
PocHistoneR: 5′-TATCTTCGAACAGACCCACCAAAT-3′

#### PocHistone PCR profile:  

1 cycle: 94 °C for 60 s   
30-40 cycles: 94 °C for 30 s, 53 °C for 30 s, and 72 °C for 60 s   
1 cycle: 72 °C for 5 min.

## _Porites_

### Coral nuclear histone region spanning H2A to H4 (H2)

#### Reference: [Tisthammer _et al._ 2020](https://peerj.com/articles/8550/)

#### H2 Primers

zH2AH4f 5′-GTGTACTTGGCTGCYGTRCT-3′    
zH4Fr 5′-GACAACCGAGAATGTCCGGT-3′

#### H2 PCR profile

1 cycle: 96 °C for 2 min   
34 cycles: 96 °C for 20 s, 58.5 °C for 20 s, and 72 °C for 90 s   
1 cycle: 72 °C for 5 min.

expected band size ∼1,500 bp

----------------

## Protocol Steps

- Primer working stock dilution
- PCR amplification
- 1% Gel to check controls and amplicon length
- Ethanol precipitation
- Nanodrop or Qubit
- DNA dilution and prep for sequencing

All references to H2O refer to PCR-grade, nucelic acid, DNAse, and RNAse free H2O.

### Primer Hydration from shipped dried primers (to 200µM)

[IDT's website](https://www.idtdna.com/pages/education/decoded/article/my-oligos-have-arrived-now-what-) has a link to a "Resuspension Calculator" that you can use to hydrate the primers to a concentration of 200µM. You will need to make an account to use the calculator, and you tell it the concentration you want to dilute to (200µM) and the "OD" number in units "nmol" written on the tube of the primer, which will be different for each tube. For example, for primer zH2AH4f, the OD # was 93.5 nmol and I wanted a final concentration of 200µM, so the calculator told me to add 467.5 µL of Low TE buffer or PCR-grade H2O.

Make sure to spin down the tube with the dehydrated primers before opening it so that none escapes!

### Primer Dilution to 10 µM from Hydrated Primers (200 µM)

Then, make a stock solution of the primers for yourself for daily use. This will have a concentration of 10 µM:

    25 µL of 200 µM primer + 475 µL PCR-grade H2O

Store in -20 ºC freezer with other PCR reagents (H2O, MasterMix)

### PCR Amplification

For all primer sets below, I used the same reaction formula:

| Master Mix 25 µL reaction |                                   |
|---------------------------|-----------------------------------|
| 12.55                     | Emerald Master Mix                |
| 10.80                     | Nuclease Free Water               |
| 0.32                      | 10µM working stock of For Primer  |
| 0.32                      | 10µM working stock of Rev Primer  |
| 1.00                      | DNA Template                      |
| 25                        | Total Volume                      |

This is based on a 33 µL formula from Kristina:

| Master Mix 33 µL reaction |                                   |
|---------------------------|-----------------------------------|
| 16.66                     | Emerald Master Mix                |
| 14.66                     | Nuclease Free Water               |
| 0.43                      | 10µM working stock of For Primer  |
| 0.43                      | 10µM working stock of Rev Primer  |
| 1                         | DNA Template                      |
| 33.18                     | Total Volume                      |

For each amplification, you will need to have a positive control and a negative control. Ideally, the positive control is a sample of DNA that has been successfully amplified using that primer set before. If you don't have this, you can probably skip the positive control. For the negative control, add everything except for the DNA into the reaction. The negative control is the most important because it will show a sign of any contamination in your reaction, primers, master mix, or water.

1. Each sample will be amplified one time in a 25µL reaction volume
2. Calculate the amount of master mix is needed: add number of samples and controls plus a % error (5-10%) to get the _n_ number (ex: for 15 samples, make enough for n = 18)
3. Make master mix in 1.5mL or 5mL tube with these components scaled up to your _n_ number:
     - 12.55µL Emerald PCR master mix * _n_ =
     - 10.80µL UltraPure water * _n_ =
     - 0.32µL 10uM working stock FatP6.1 primer * _n_ =
     - 0.32µL 10uM working stock RORF primer * _n_ =
4. Vortex and spin down master mix and keep on ice.
5. Into labeled PCR strip tubes, add 24µL of master mix to as many tubes as samples you have + the number of positive and negative controls planned. Positive and negative controls could be in a separate strip tube or individual 0.2 mL tubes since they do not need to be kept after the gel imaging step.
6. Using a p2 pipette, add 1µL of DNA sample to their respective tube where the master mix is added. Add in 1 µL of H2O (or nothing) to the tube for the negative control and add 1 µL of the positive control DNA to the positive control tube. You should have 25µL in each tube.
7. Spin down in microcentrifuge with strip-tube attachment.
8. Turn on thermocyler and login to PUTNAM (1,2,3,4) and navigate to the program (in Sanger folder) for the given primer set.
    - POC mtORF program: FATP RORF, bold fields are cycled 30 times
      - 60 seconds 94 ºC
      - **30 seconds 94 ºC**
      - **30 seconds 53 ºC**
      - **75 seconds 72 ºC**
      - 5 minutes 72 ºC
    - POC PocHistone program: PocHistone, bold fields are cycled 30 times
      - 60 seconds 94 ºC
      - **30 seconds 94 ºC**
      - **30 seconds 53 ºC**
      - **60 seconds 72 ºC**
      - 5 minutes 72 ºC
   - POR H2 program: POC zH2AH4f, bold fields are cycled 34 times
      - 120 seconds 96 ºC
      - **20 seconds 96 ºC**
      - **20 seconds 58.5 ºC**
      - **90 seconds 72 ºC**
      - 5 minutes 72 ºC
9. Run that program, bold fields are cycled 30-40 times depending on the program (see details above).
10. The program runs for about 1 hour and 40 minutes
11. Take tubes out and store at 4 ºC if not running gel / cleaning up immediately

### DNA and RNA Quality Check: 1% [Gel](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Gel-Protocol/) at 80V for 30 mins.

No loading dye needed to add to samples because of the green dye in the Master Mix.

### Ethanol precipitation to clean up PCR product

- Sodium acetate EtoH precipitation, protocol coming soon!

- Elute in TRIS
### Nanodrop of cleaned PCR product

- Blank nanodrop with TRIS
### For Sanger Sequencing

### Primer Dilution from 10 µM Primer Working stock to 3.2 µM for sequencing

1.6 µL of 10 µM primer + 3.4 µL H2O = 5 µL

Make enough for # of sequencing reactions, 2µL per reaction (e.g. 35 µL for 15 samples, 30 µL plus extra for error)