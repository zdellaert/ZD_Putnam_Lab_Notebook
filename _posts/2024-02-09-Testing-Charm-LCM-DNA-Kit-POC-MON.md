---
layout: post
title: Testing Charm Biotech RNA Extraction on Cryosectioned P. comp and M. cap 
date: '2024-02-09'
categories: Processing
tags: [RNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Charm DNA Kit on P. comp and M. cap

### [Protocol Link](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Charm-LCM-DNA-Kit-Protocol/)

Samples:
- P_1_1 - POR DD1 buffer 1 hr incubation, 56 ºC, 1400rpm
- P_1_3 - POR DD1 buffer 3 hr incubation, 56 ºC
- P_2_1 - POR DD2 buffer 1 hr incubation, 56 ºC, 1400rpm
- P_2_3 - POR DD2 buffer 3 hr incubation, 56 ºC

**Sample prep notes for extracting from whole sections instead of LCM samples:**

1. Remove a cryosectioned slide from -80 ºC (same sample/sectioning round as used for LCM), transfer to -20 ºC for 30 minutes, then transfer slide to cooler with dry ice
   1. KEEP CONTAINER CLOSED, with dessicant inside
      - "take slide in container with desiccant out of -80 ºC and allow  to slowly reach room temperature, for at least 60 min, before opening ([Roy et al 2020 Bioprotocols](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/BioProtoc-10-01-3475.pdf))"
2. Pre-cool lysis buffer mixture on ice
3. Pre-cool forceps and razor blades for transferring tissue to lysis buffer
4. Stain and wash all slides and perform dissections in petri dishes cleaned to be RNAse free
5. Remove OCT, in RNAse free petri dish on ice, pipette solutions on and off slide with 1mL pipette
    - 2 minute in ice-cold 70% Ethanol
    - 45 s in ice-cold 50% Ethanol
    - 30 s in ice-cold 30% Ethanol
    - if there is excess OCT, dip slide in ice-cold RNAse free water 5-6 times over 1-2 mins
6. Remove slide to dark background over PCR rack (over dry ice, though be careful to not freeze the water once the volume on the slide is low, if that's freezing move to regular ice) and use sterile razor blade, cleaned with RNAse cleaner, to scrape off tissue sections into a tube filled with prepared **100 uL digestion buffer**.

### Alternate version of this for Paxgene-fixed, cryoembedded samples (incubation does not need to be as aggressive because there is no paraffin and the tissue was fixed with Paxgene fixative, not formalin)

1. **Sample prep from LCM samples**
   - LCM from PFCE tissue sections
     - Add 100 uL buffer DD2
2. Incubate the inverted tube at 60 ºC for 10 minutes to allow the captured cells and tissues detaching from the cap into the digestion buffer.
3. Centrifuge briefly to collect all liquid at the bottom of the tube. Mix the liquid by pipetting up and down the solution several times to disperse any pellet precipitate.
4. Digestion with Proteinase K
   - **LCM from PFCE tissue sections**
     - Add 10 uL proteinase K to the tube and mix well
     - Incubate at 60 °C for 3-4 hours with occasional mixing until lysis is complete.
        -  (Optional: You may perform digestion at 52 ºC overnight if preferred).
      -  **Alternatively, I have had success with a shorter incubation** for RNA, see notes [here](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Testing-Charm-LCM-RNA-Kit/)
         -  Instead of 60 °C for 3-4 hours, try **shaker–incubator for 1 h at 56°C and 1400 rpm.**
   - **At the end of incubation,no pellets should be visible**, otherwise, extend incubation 15 minutes more to make sure no pellets exist.
5. Centrifuge the microtube at maximum speed (about 13000 rpm or 16000 X g) for one minute.

### Quality Control (QC)

These steps analyze the quantity and quality of the DNA extracted.

#### DNA Quantity  

Follow Broad Range dsDNA Qubit [protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/) to analyze sample **quantity**. Read standards once and record values, read all samples twice.

#### DNA Quality  

If DNA quantity is sufficient (typically >10 ng/µL) follow the PPP Agarose Gel [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Gel-Protocol/) to determine DNA quality. "Good" DNA should form a distinct band a the very top of the gel.