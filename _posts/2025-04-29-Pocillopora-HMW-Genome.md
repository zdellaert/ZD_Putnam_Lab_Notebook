---
layout: post
title: Extracting HMW DNA for P. tuahiniensis Genome
date: '2025-04-29'
categories: Protocols, Processing
tags: [DNA, Pocillopora, E5]
---

# Extracting HMW DNA for P. tuahiniensis Genome, sample POC-222

## Finding flash-frozen samples that are left after E5 metabolomics 

| Colony ID | Site            | Timepoint | Fragment | Subset Bag Color | Freezer Inventory Fragment notes                                             | Airbrushed for metabolomics (by JA) | Theoretically available for HMW extraction / Javi | Extracted for HMW? | Available for Javi post-HMW? |
|-----------|-----------------|-----------|----------|------------------|------------------------------------------------------------------------------|-------------------------------------|---------------------------------------------------|--------------------|------------------------------|
| POC-222   | Mahana (site 2) | TP1       | M1       | green            |                                                                              | Yes (20250115)                      | No                                                | No                 |                              |
| POC-222   | Mahana (site 2) | TP1       | M2       | red              |                                                                              | No                                  | Yes!                                              |                    |                              |
| POC-222   | Mahana (site 2) | TP2       | M1       | green            | No date on whirlpak, but from March - based on handwriting. Zoe has picture. | No                                  | Yes!                                              |                    |                              |
| POC-222   | Mahana (site 2) | TP2       | M2       | yellow           | From "undated" March bag - Zoe has picture                                   | No                                  | Yes!                                              |                    |                              |
| POC-222   | Mahana (site 2) | TP3       | M1       | green            |                                                                              | Yes (20250117)                      | No                                                | No                 |                              |
| POC-222   | Mahana (site 2) | TP3       | M2       | grey             |                                                                              | No                                  | Yes!                                              |                    |                              |
| POC-222   | Mahana (site 2) | TP4       | M1       | pink             |                                                                              | Yes (20250117)                      | No                                                | No                 |                              |
| POC-222   | Mahana (site 2) | TP4       | M2       | pink             |                                                                              | found by jill but not airbrushed?   | Yes!                                              |                    |                              |

### So, I need to locate the following, and choose one to extract from:

- [ ] POC-222, TP1 M2 - red bag
- [ ] POC-222, TP2 M1 - green bag (*No date on whirlpak, but from March - based on handwriting. Zoe has picture.*)
  - [ ] OR - POC-222, TP2 M2 - yellow bag (*From "undated" March bag - Zoe has picture*))
- [ ] POC-222, TP3 M2 - grey bag
- [ ] POC-222, TP4 M2 - pink bag 

We only need to extract from one fragment, and ideally we would have an extra fragment for each timepoint to send to FIU for other analyses. If we can locate one of the green or yellow bag (TP2) fragments, that would be perfect.

## What is our goal for amount of DNA?

- From the sequencing facility (BYU, through genohub): "Three micrograms of DNA should be provided to enable library construction and Blue-Pippin size selection for large fragment whole genome libraries"

- (Danielle's post said: For PacBio we need 10-20ug of genomic DNA (as quantified by Qubit) in less than 400ul. Quality of the DNA should be over 40kb in size, though we can remove smaller fragments.)



## Protocol

1. Want to use the NEB High Molecular Weight DNA Extraction, first tested by Danielle in this post:
   1. https://github.com/daniellembecker/DanielleBecker_Lab_Notebook/blob/master/_posts/2023-07-12-HMW-DNA-Acropora%20pulchra-sperm.md
2. However, I am starting with adult tissue so will need to grind the fragment in LN2:
   1. See an example from Maggie(https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/pacuta-HMW/), who used the [Qiagen Genomic Tip Kit](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/HMW-Tip-Protocol/)

### **Important Notes about HMW DNA** from [Maggie](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/HMW-Tip-Protocol/)

- HMW DNA is very fragile, pipetting or vortexing can sheer it easily
- Do not vortex after extraction, to mix the samples flick gently then spin down
- Whenever you are pipetting the actual sample (ie, not buffers) you should use wide bore pipette tips, these are next to the kit on the Putnam shelf. They have a larger opening to the tip and are gentler
- **Do not freeze the DNA**, freeze thaws can break up the long fragments, keep HMW DNA in the 4 degree fridge for storage
- HMW DNA can really clump, especially in this extraction method that pellets it in a precipitation. For quantifying with the Qubit, take a top and bottom of the tube 1ul: do 2 Qubits for each sample and average them together for the whole tube concentration

### Other notes

[New England Biolabs High Molecular Weight DNA Extraction Guidelines](https://www.neb.com/monarch/high-molecular-weight-dna-extraction?gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_kHBvc274KwNljTVwN6r2KJbjBQjnWFzkyJLI6GpmEZw7UNU-HPjmEaAt_tEALw_wcB)

[New England Biolabs High Molecular Weight DNA Cells and Blood Kit](https://www.neb.com/-/media/nebus/files/manuals/manualt3050.pdf?rev=41e2c417f75c4889b2d0caeaa6746419&hash=1A3E03456DCB79B426622B85DFB85111)

[New England Biolabs High Molecular Weight DNA Tissue Kit](https://www.neb.com/en-us/-/media/nebus/files/manuals/manualt3060.pdf?rev=667e1391e07b4684a8ca19682aac7c5d&hash=0FA39FAF9C63BFC6DF4E7CB995776D91)


### Protocol, Using the [**New England Biolabs/Monarch High Molecular Weight DNA Tissue Kit**](https://www.neb.com/en-us/products/t3060-monarch-hmw-dna-extraction-kit-for-tissue#Protocols--Manuals---Usage)

#### Caveat: FAQ: Can the Monarch HMW DNA Extraction Kits be used to process marine samples, including marine invertebrates?
    "We have not tested the kit on these organisms. Often these organisms contain a lot of mucus/ polysaccharide-based material, which may cause problems during bead binding. If you have an optimized lysis chemistry, you may be able to employ that upstream of our bead workflow using the Monarch HMW DNA Extraction Kit for Tissue (NEB #T3060)."


#### Materials

- Monarch® HMW DNA Extraction Kit for Tissue - NEB #T3060S/L
- Mortar and Pestle
- Liquid nitrogen
- Bucket of dry ice
- Thermal mixer containing a 1.5 ml tube block
- Isopropanol, 550 μl per sample
- Ethanol (≥ 95%)
- 1.5 ml DNase-free, **low DNA binding** microfuge tubes (e.g., Eppendorf® DNA LoBind®, #0030108051) are recommended for elution and storage (1 per sample)
- Recommended: vertical rotating mixer (e.g., Thermo Scientific® HulaMixer® Sample Mixer).
- Wide-bore pipette tips
- Microcentrifuge

#### Important notes:

- Review the complete protocol before beginning.
- Add ethanol (≥ 95%) to the gDNA Wash Buffer as indicated on the bottle label.
- Preheat thermal mixer with 1.5 ml block to 56°C.

#### Part 0 - Prepare tissue

1. Prelabel tubes (one 5mL tube for all tissue powder and one Monarch Pestle Tube for the extraction) and pre-cool these as well as your forceps and tissue scraping/scooping utensil of choice on dry ice.
2. Sterilize the mortar and pestle and then cool it with liquid nitrogen, allow it to evaporate off.
3. Keeping tissue as cold as possible, grind the flash frozen tissue sample from the -80ºC freezer to a powder.
4. Transfer to pre-cooled  tube as quickly as possible and keep on dry ice.
   - Keep tubes containing tissue powder on dry-ice and use small pre-chilled scoops that allow for the transfer of 2 or 10 mg frozen tissue powder at a time.
   - Keep the aliquoted samples on dry ice to ensure the powder stays frozen. 
5. Choose your input amount of tissue. This gets complicated with coral due to the skeleton.
   1. "*The sample input range is 2–25 mg for most tissues (2–15 mg of DNA-rich/soft organ tissues (e.g., kidney, liver), 2–20 mg for brain). The upper limit for tissue input amounts is often limited by the viscosity of the lysed sample, which negatively impacts enzyme access, protein removal, precipitation onto the beads, and dissolving/resuspension of the purified DNA. In some samples, the high amounts of fibers or fatty acids can be factors that limit the input amounts. If a lower-than-recommended input amount is used, DNA recovery will be significantly reduced. Standard and low input protocols are provided to ensure the buffer volumes are appropriate and that precipitation onto the beads is efficient. If working with fatty or fibrous tissues (e.g., brain and muscle), and only very small amounts of sample are available (< 5 mg), see guidance in “Using Very Low Input Amounts*”.
6. Tare pre-chilled ***Monarch Pestle Tube*** on the micro balance and transfer the appropriate amount of frozen tissue powder to tube for weighing. Do not use more tissue than recommended (see “Choosing Input Amounts”). Work quickly to prevent the tube from warming up on the balance.
7. **Alternatively:** Tare the chilled mortar on the balance and weigh out the exact amount of tissue you want (clip off pieces from the fragment using clippers over dry ice), keeping the rest of the frozen fragment intact.

#### Part 1 - Tissue Lysis

1. Prepare a master mix of HMW gDNA Tissue Lysis Buffer and Proteinase K according to the table below and the number of samples that will be processed
   1. 600 uL Tissue Lysis Buffer 
   2. 20 uL Proteinase K
2. Take the Monarch Pestle Tube containing the desired amount of tissue powder (see above) from the dry ice, and briefly spin down on a benchtop microcentrifuge to collect tisse to the bottom of the tube.
   1. If the powder is stuck to the tube, let the sample thaw briefly before spinning and proceed immediately to homogenization. 
3. Homogenization with pestle:
   1. Use the pestle to **grind the sample** within the pestle tube; leave the pestle in the tube
   2. Leave the pestle in the tube
   3. Using a **wide-bore pipette tip**, add 600 µl of the lysis master mix to the sample. Do not dispose of this tip yet, as it will be used to mix the sample.
   4. Ensure there is no tissue material remaining on the pestle, then discard the pestle.
      1. *If visible DNA threads or tissue material stick to the pestle, transfer it carefully into the tube by wiping the pestle tip along the tube rim*. 
   5. Using the wide-bore tip, **pipette up and down a few times** to homogenize the tissue lysate and ensure rapid, complete lysis. Discard the pipette tip.
   6. **Begin incubation** in the thermal mixer (Step 5), and repeat steps a-e with any remaining samples.
4. Incubate samples in a thermal mixer at **56°C for a minimum of 45 minutes with agitation at the desired speed**.
   1. When lysis is complete, samples will **turn from turbid to clear** (or mostly clear, depending on the tissue type). 
   2. The speed of the thermal mixer influences fragment length and lysis; higher agitation speeds reduce DNA size and sample lysis time. For most applications, maximum agitation speed (1400-2000 rpm) is recommended.
   3. For highest yields, particularly when working with low input samples or samples with relatively low DNA content (e.g., brain and muscle), stop agitation after 15 minutes and continue the remaining incubation time without agitation.
5. Add **10 µl RNase A** and mix by inverting 5–10 times.
6. Incubate for **10 minutes at 56°C** at the **same agitation speed** used in Step 5.
7. Add **300 µl Protein Separation Solution** and **mix by inverting for 1 minute**.
8. Centrifuge for **10 minutes at 16,000 x g.**. 
   1. The sample will separate into a large, clear phase (DNA) and a smaller (often brown) protein phase, usually on the bottom of the tube. For some tissues, the protein phase may be yellow or clear. Additional centrifugation time (10–20 minutes) may be required for complete phase separation, particularly when low agitation speeds were used. 
   2. *Prepare the plastics for Part 2*:
      1. 1 Monarch Spin Collection Tube (no need to label)
      2. 1 Monarch Bead Retainer inserted into the collection tube; this will be used to remove the wash buffer from the gDNA bound to the beads.
      3. 2 Monarch 2 ml Tubes; one for phase separation and one for elution.
      4. 1 1.5 ml microfuge tube (DNA low bind recommended, not provided); this will be used to collect the eluate.
9. Using a **1000 µl wide-bore pipette tip**, transfer the upper phase containing the DNA (large, clear phase) to a labeled Monarch 2 ml Tube.
   1.  A substantial fraction of HMW DNA will be located at the interface between the clear upper phase and the protein phase; highest yields will be achieved by transferring as much of the upper phase as possible. **Using a 200 µl wide-bore pipette tip to transfer the final volume of upper phase is recommended for maximum yield.** *Avoid transferring material from the protein layer*, although a small amount (1–2 µl) will not be detrimental. If a small amount of the protein phase enters the pipette tip, gently push it back into the tube. If a lower protein phase is not visible, leave ~30 µl behind to ensure protein is not carried over. **Typically, the transferred volume will be ~ 800 µl** (Low Input: ~400 µl).
   2.  *If the volume of the sample is < 700 µl (Low Input: < 350 µl), adjust the volume of isopropanol used in Step 2 of Part 2: HMW gDNA Binding and Elution to 0.7 volumes. *

#### Part 2: HMW gDNA Binding AND Elution

1. Using clean forceps, **add 2 DNA Capture Beads** to each sample, which should be contained in a Monarch 2 ml Tube.

2. Add **550 μl isopropanol**, close the cap, and mix on a vertical rotating mixer at 10 rpm for 5 minutes to attach DNA to the beads.
   - If a vertical rotating mixer is not available, invert slowly and gently by hand 25–30 times. A manual inversion is complete when the tube returns to the upright position. Slow inversion is critical for the DNA to bind to the beads; each full inversion should take ~5–6 seconds. If necessary, flick the tube to release any beads that stick to the bottom of the tube.
   - After a 2–3 inversions, the solution becomes more viscous and the DNA will wrap loosely around the beads. During the following inversions, precipitation of gDNA may be visible, especially with larger input samples. The DNA complex will often contain small air bubbles. With increasing number of inversions, the DNA will completely wrap around the beads, often causing the beads to stick together. DNA binding to the beads should be complete after 25–30 inversions, and the solution should no longer be viscous. Additional inversions may be necessary for larger input samples.
   - Note: at this step should see DNA precipitate on the DNA beads

3. **Remove and discard liquid by pipetting**. Avoid removing any of the gDNA wrapped around the glass beads. For optimal DNA solubility, avoid letting the bound DNA dry out on the beads during this and the following steps; **add the next buffer quickly**. There are two suggested options for carrying out this step:
    - Keeping tube upright, insert pipette tip and gently push beads aside to remove liquid.
    - Angle tube so that beads remain at the bottom, and liquid reaches toward tube opening. Pipette from the liquid surface and continue to angle as liquid is removed (tube will be almost horizontal at the end).

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/Monarch_HMW_1.png?raw=true"  width="400" />

4. Add **500 μl gDNA Wash Buffer**, close the cap, and mix by inverting the tube 2–3 times. Remove the gDNA Wash Buffer as described in Step 3. The loose gDNA complex will condense around the beads more tightly.

5. Repeat the wash in Steps 4. Remove the gDNA Wash Buffer by pipetting. It is not necessary to remove all the gDNA Wash Buffer at this point.

6. Place a labeled Bead Retainer into a Monarch Spin Collection Tube. Pour the beads into the bead retainer and close the cap. Discard the used Monarch 2 ml Tube.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/Monarch_HMW_2.png?raw=true"  width="200" />

7. Pulse spin (1 second or less) the sample in a benchtop minicentrifuge to remove any residual wash buffer from the beads.

8. Separate the bead retainer from the collection tube, pour the beads into a new, labeled Monarch 2 ml Tube, and **insert the used bead retainer into the labeled 1.5 ml microfuge tube** (_DNA low bind recommended_, not provided) for later use during elution. Discard the used collection tube.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/Monarch_HMW_3.png?raw=true"  width="200" />

9.  Immediately add **100 μl Elution Buffer II** onto the glass beads and **incubate for 5 minutes at 56°C in a thermal mixer with agitation at the lowest speed (300 rpm)**. Halfway through the incubation, ensure the beads are not stuck to the bottom of the tube by *tilting the tube almost horizontally and gently shaking*
   - This ensures that the beads can move freely, allowing for optimal release of the DNA from the beads. It also ensures that the lower bead does not stick to the bottom of the tube during the following transfer step.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/Monarch_HMW_4.png?raw=true"  width="200" />

10. Ensure the bead retainer is inserted into the 1.5 ml microfuge tube. **Pour the eluate and the glass beads into the bead retainer and close the cap**. Typically, all the eluate flows into the bead retainer upon pouring. If any volume remains in the 2 ml tube, spin briefly and transfer.

<img src="https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/Monarch_HMW_5.png?raw=true"  width="200" />

11.   **Centrifuge for 30 seconds at 12,000 x g** to separate the eluate from the glass beads. *Discard the beads and retainer.*

12.  **Pipette eluate up and down 5–10 times with a wide bore pipette tip and ensure any visible DNA aggregates are dispersed.** Before analysis or downstream use, HMW DNA must be homogeneously dissolved. **After pipetting, incubate at 37°C for 30-60 minutes, overnight at room temperature, or for > 24 hours at 4°C**.

*Pipette up and down 5-10 times again before analyzing or using the HMW DNA. Samples processed using low agitation speeds during lysis will require additional time to fully dissolve. See additional guidance in “Homogenization of HMW DNA”. Samples can be stored at 4°C for short term use (weeks), or at -20°C for long term storage. The elution buffer (10 mM Tris, pH 9.0, 0.5 mM EDTA) is formulated for long term storage of gDNA*

Note: at this step should see DNA precipitate at bottom of tube

### QC:

The sample needs to be thoroughly homogenized for accurate readings. It is sometimes best to wait 2-3 with the sample at 4ºC before performing QC.

1. Broad range Qubit DNA
2. gDNA Tapestation 
3. Nanodrop
   1. If purity is not high enough, perform [ethanol precipitation](https://github.com/daniellembecker/DanielleBecker_Lab_Notebook/blob/master/_posts/2023-07-12-HMW-DNA-Acropora%20pulchra-sperm.md)
   2. PacBio requests a 260/280 ratio between 1.8 and 1.9

## Failed Extraction attempts with NEB Kit

- I followed the above protocol on 5/8/25 but it was not successful. Notes about steps taken:
  - I was shooting for a 0.1 g of tissue (minimizing skeleton) input, but wasn't sure what would be best so I tested two input levels
  - High input tube: 0.0978g
  - Low input tube: 0.0222g
  - Both had quite a bit of skelton
  - During 56 ºC incubation (step 4), I used a speed of 1600 rpm for 45 minutes. After 15 minutes, I spun down the tube and removed the supernatant into a clean tube to minimize skeletal carryover, then proceeded with the rest of the incubation
- I am not sure if we are getting enough tissue input into the extraction. During the protein separation phase, there was not a clear separation of layers even after 30 minutes of centrifuging. Instead, drops of what looked like oil floated at the top of the aqueous layer and were very difficult to separate.
- Jill had the exact same result on her attempt on 5/14/25. Her modifications:   
  - tried scraping tissue from the chunk to minimize skeletal input
- QC results:


Used Broad Range dsDNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
All samples read twice, standard only read once

DNA Standards: 189.42 (S1) & 21542.59 (S2)

| Tube Number | Top Read 1 (ng/uL) | Top Read 2 (ng/uL) | Bottom Read 1 (ng/uL) | Bottom Read 2 (ng/uL) | Average (ng/uL)          | 
|-------------|--------------------|--------------------|-----------------------|-----------------------|--------------------------|
| Zoe, High Input (5/8) | nd   | nd   |  nd    |  nd  |  0   |
| Zoe, Low Input (5/8)  | nd   | nd   |  nd    |  nd  |  0   |
| Jill (5/14)           | nd   | nd   |  nd    |  nd  |  0   |


## 5/27/25 Genomic Tip Extraction

On 5/27/25, Natalie and I attempted Maggie's Qiagen Genomic Tip HMW extraction protocol, which was successful for P. acuta in the past. [P. acuta link is here](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/pacuta-HMW/) and detailed protocol [here](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/HMW-Tip-Protocol/). However, all of the buffers are very expired.

I followed her protocol exactly, except I warmed the Tris EDTA buffer to 55 ºC prior to elution. I can't imagine this hurt, since the tubes go straight into that temperature after elution, but I wanted to note it. After elution, as recommended, I incubated the tubes for 1hr at 55 ºC in the Theremomixer, no shaking, and then transferred to an orbital shaker 200rpm overnight.

### QC results

- Used Broad Range dsDNA Qubit [Protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Qubit-Protocol/)
- All samples read twice, standard only read once

DNA Standards: 182.25 (S1) & 20034.97 (S2)

| Tube Number | Top Read 1 (ng/uL) | Top Read 2 (ng/uL) | Bottom Read 1 (ng/uL) | Bottom Read 2 (ng/uL) | Average (ng/uL)          | Amount in tube (*46 uL) |
|-------------|--------------------|--------------------|-----------------------|-----------------------|--------------------------|-------------------------|
| 1           | 5.67               | 5.84               | 5.95                  | 6.06                  | 5.88                     | 270.48                  |
| 2           | 6.6                | 6.73               | 6.41                  | 6.46                  | 6.55                     | 301.3                   |
| 3           | 6.95               | 7.08               | 8.04                  | 8.15                  | 7.555                    | 347.53                  |
| 4           | 3.95               | 3.95               | 3.8                   | 3.83                  | 3.8825                   | 178.595                 |
| 5           | 7.11               | 7.19               | 6.78                  | 6.93                  | 7.0025                   | 322.115                 |
| 6           | 7.44               | 7.43               | 7.46                  | 7.52                  | 7.4625                   | 343.275                 |
|             |                    |                    |                       |                       | Total DNA extracted (ng) | 1763.295                |
|             |                    |                    |                       |                       | Total DNA extracted (ug) | 1.8                     |

Result: pretty low compared to Maggie's [results](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/pacuta-HMW/), but also not compltetely a failure! 
