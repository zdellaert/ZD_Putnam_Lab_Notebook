---
layout: post
title: Testing Leica LDM7 Laser Capture Microdissection on P. acuta 
date: '2023-10-16'
categories: Processing
tags: [DNA, RNA, PAXgene, Fixative, Pocillopora, LCM]
---

## Testing Laser Capture Microdissection 

### Necessary supplies:
- We are using 4 µm PEN slides available [here](https://us.vwr.com/store/product/31049722/null) (see notes from Leica [here](https://www.leica-microsystems.com/science-lab/life-science/consumables-for-laser-microdissection/) and [here](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/lmdslidememo.pdf)). To test, we are using one PEN membrane (4 µm) coated glass slide (VWR #11600288) and a PEN frame slide (not available on VWR).
    - We will likely use the PEN coated glass slide for future applications. If we use lower magnification, a 2 µm thickness of PEN membrane will also likely work, and these are available RNAse free (VWR #11505189 or #11505158). 4 µm slides are the easiest to use because: "the membrane is stronger compared to the 2 µm standard which allows easier section mounting and a lower risk of membrane injury during the mounting procedure and the membrane itself is heavier and thus easier to collect via gravity".
    - The frame slides are recommended for single-cell and other high-magnification (150X) applications.
    - If we are having issues with PEN membrane autofluorescense, we can try to switch to PPS or PET slides.
- All other supplies are listed in the [cryosectioning protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Cryosectioning-Protocol/)

### Resources

Sample Preparation for LCM [guide](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide-May-2015.pdf) ([old version](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide.pdf))
    - RNA preservation is incredibly important since the amount of tissue we will use for RNA extraction will be so limited. Protocol below is largely based off of this guide with bits from the [PAXgene protocol](https://www.preanalytix.com/storage/download/_ProductResources_/SuppProtocols/HB-1543-S01-001_PX20_SP_TIssue_System_Preparation_of_sections_from_PFPE_and_PFCE_tissues_for_manual_or_LMD_1015_WW.pdf).

How to use Leica LMD7000 [presentation](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Leica%20LMD7000%20-%20Operating%20Instructions.pdf)

### Step by step protocol:

- What I did: See [this post](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/PAXgene-Fix-Decalc/) for sample prep info, the two branches used here for sectioning and embedding are the two that were put into sucrose on 10/16/23 and embedded on 10/17/23. Slide prep on 10/22/23 and sectioning on 10/23/23. Test on 10/24/23.

- **All surfaces and equipment should be treated with RNAse cleaner!!!**

- Slide prep of Leica LDM slides (one PEN glass slide and one PEN frame slide) was done on 10/22/23
    - Make sure to not damage or touch the membrane in any way
    - Using sterilized and RNAse zap-ped forceps, dip slides in RNAse zap for 15 seconds
    - Follow this by two 15 second rinses in DEPC water
    - Let dry, at room temperature or at 37 ºC
    - When visibly dry, place in UV box for 30 minutes (ideally do so immediately prior to sectioning)
    - With clean, gloved hands, transfer to slide box for sectioning

- Section using [this protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Cryosectioning-Protocol/); Notes:
    1. Move OCT-tissue blocks to -20 ºC 30 minutes before sectioning
        - and place PEN slide under UV light for 30 minutes
    2. Prepared RNAse free cleaning solutions for cryostat in 50 mL tubes
        - 1:1 mixture of 70 % Ethanol : RNAse zap
        - 95 % Ethanol
    3. Clean the cryostat before sectioning with RNAse zap:Ethanol mixture followed by 70% or 95% ethanol
    4. Trim the block so that there is not much excess OCT - we want to get as many sections on the slide as possible, so the smaller the size of the sections the better
    5. Very carefully transfer sections to PEN membrane without damaging the membrane
    6. Keep the slides in the cryostat and transport in sealed slide boxes on dry ice
    7. After sectioning, keep in "sealed slide boxes with a desiccant at –80°C until needed"

- Staining

    - **Stain right before performing LCM. Stain as quickly as possible, then dry slide, then go to LCM.**

    - All surfaces and equipment should be treated with RNAse cleaner!!!

    1. Morning of LCM, bring slide up to room temperature, slowly to avoid formation of water condensation inside the container
        - 15 minutes at - 20 ºC
        - 15 minutes at 4 ºC
        - 15 minutes at room temp (ideally there is no condensation)
            - can place in dessicator
    2. Make sure all OCT is removed:
        - 70% EtOH, 1 min
        - DEPC water, 30 s
    3. Hoescht staining: 
        - make 1 µg/ml solution of Hoescht 
            - add 0.001 g to 1 mL of RNAse/DNAse free H2O
            - wrap tube in aluminum foil to keep dark and store at -20ºC 
        - Add 100 uL of the Hoescht solution to each section and allow to stain in the dark for 5 mins.
    4. Wash in DEPC water or RNAse-free 1X PBS in dark
        - 95% EtOH, 30 s
        - 100% EtOH, 30 s
    5. Remove excess liquid by aspirating and pat dry area around sample with Kimwipe
    6. Air dry, covered to prevent dust from accumulating
        - **10 mins at 40 ºC to fully dry sections**

Total time: 45 mins coming to temp + ~10 mins staining + 10 mins to dry: 1 hour 5 mins

- Notes:
    - we may want to purchase dessicant and vaccum bags to keep condensation away: [Roy et al 2020 Bioprotocols](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/BioProtoc-10-01-3475.pdf)

#### Laser capture time!
- How to use Leica LMD7000 [presentation](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Leica%20LMD7000%20-%20Operating%20Instructions.pdf)



#### Notes after first test
- the tissue was disintegrated. Trying to cut thicker sections (20 uM), trying the glass membrane PEN slide, using the frame support if using the PEN frame slides should help. We also decided to not do the Hoescht staining prior to LCM to try to reduce the stress on the tissue. This will also reduce UV stress on the tissue when imaging using fluorescence. We can see algal cells just fine in brightfield. If we want, we can try H&E staining or any of the stains in the leica [guide](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide-May-2015.pdf).

Images!

Scope

![scope.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/scope.jpg?raw=true)

ROIs (large-scale sections for testing RNA extraction) collected in tube C:

![C_BEFORE.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/C_BEFORE.jpg?raw=true)

![C-AFTER.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/C-AFTER.jpg?raw=true)

![C-CAP.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/C-CAP.jpg?raw=true)

![C2_BEFORE.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/C2_BEFORE.jpg?raw=true)

![C2-AFTER.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/C2-AFTER.jpg?raw=true)

![C2-CAP.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/C2-CAP.jpg?raw=true)

Example of drawing ROI to collect specific cells:

![draw_roi.PNG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/draw_roi.PNG?raw=true)

![post_cut.PNG](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/post_cut.PNG?raw=true)


Example of visualizing fluorescence using this scope. Not ideal and not adding much information:

![DAPI_1.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/DAPI_1.jpg?raw=true)

![GREEN_1.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/GREEN_1.jpg?raw=true)

![RED_1.jpg](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/images/protocols/LCM/RED_1.jpg?raw=true)
