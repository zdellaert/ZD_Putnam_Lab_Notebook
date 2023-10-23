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

### Preparing slides for LCM
- All surfaces and equipment should be treated with RNAse cleaner!!!
- Making the slides RNAse free (from [this memo](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/lmdslidememo.pdf) and [guide](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide.pdf)): "The foil slides can be treated to remove RNases by dipping them into a bath of pure RNase Zap (Ambion Corp) for 15 seconds. Follow this with two rinses in DEPC water"
- Preparing the slide with UV Irradiation (from [this memo](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/lmdslidememo.pdf) and [guide](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide.pdf)): "The slides should be irradiated at 220nm to 260nm at full power for 30 minutes."
- Then [cryosection!!](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/4c37b61755cfaea5c9378dbe929cf6070dacacc1/_posts/2023-08-31-Cryosectioning-Protocol.md)
    - Make sure to use RNAse cleaner and perform all steps as quickly as possible. 
    - Clean the cryostat before sectioning to avoid contamination
    - Trim the block so that there is not much excess OCT - we want to get as many sections on the slide as possible, so the smaller the size of the sections the better
    - *"Important: If you are using FrameSlides, the FrameSupport is strongly recommended. Sections can be fixed with ice-cold acetone for 2–3 minutes, 70% or 100% ethanol for 20 seconds or mixture of ethanol : acetic acid (19:1) to increase the adhesion of the tissue to the PPS-, PEN-, PET-, POL- or FLUO-membranes."*
    - "Keep the slides in the cryostat or on dry ice, if LMD is performed on the same day. Alternatively, they may be stored in **sealed slide boxes with a desiccant at –80°C until needed**."
- RNA preservation is incredibly important since the amount of tissue we will use for RNA extraction will be so limited. Notes from the [guide](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide-May-2015.pdf) ([old version](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide.pdf))
    - Stain right before performing LCM. Stain as quickly as possible, then dry slide, then go to LCM.
    - **After staining**: "Dry slides at room temperature for 15 minutes using a drying chamber with desiccant or at 40°C for 10 minutes. This is a critical step for successful LMD. Sample slides should be stained just prior to microdissection."
    - "Just before laser microdissection, the container with the slides should be taken out of the freezer and *slowly adjusted to room temperature* to avoid formation of water condensation inside the container, e.g. allow for at least **15 min each step to equilibrate at -20°C, 4°C and room temperature**"

### HOW TO USE

Sample Preparation for LCM [guide](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/leicalmdprotocolguide.pdf)


How to use Leica LMD7000 [presentation](https://github.com/zdellaert/ZD_Putnam_Lab_Notebook/blob/master/protocols/Leica%20LMD7000%20-%20Operating%20Instructions.pdf)


### What I did:

- See [this post](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/PAXgene-Fix-Decalc/) for sample prep info, the two branches used here for sectioning and embedding are the two that were put into sucrose on 10/16/23 and embedded on 10/17/23

- Slide prep of Leica LDM slides (one PEN glass slide and one PEN frame slide) was done on 10/22/23
    - using sterilized and RNAse zap-ped forceps, dipped slides in RNAse zap for 15 seconds
    - 2 15 second rinses in DEPC water
    - let dry , propped up on parafilm for about 30 minutes (could also do what they suggest which is drying at 37ºC)
    - when visibly dry, placed in UV box for 30 minutes
    - with clean, gloved hands, transferred to slide box for sectioning tomorrow. 

- Sectioning using [this protocol](https://zdellaert.github.io/ZD_Putnam_Lab_Notebook/Cryosectioning-Protocol/) on 10/23/23
    1. moved blocks to -80 ºC 30 minutes before sectioning and placed PEN slide under UV light for 30 minutes
    2. prepared RNAse free cleaning solutions for cryostat in 50 mL tubes
        - 1:1 mixture of 70 % Ethanol : RNAse zap
        - 95 % Ethanol

- Staining
    1. Morning of LCM, bring slide up to room temperature
        - 15 minutes at - 20 ºC
        - 15 minutes at 4 ºC
        - 15 minutes at room temp (ideally there is no condensation)
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
            - "Dry slides at room temperature for 15 minutes using a drying chamber with desiccant or at 40°C for 10 minutes. This is a critical step for successful LMD. Sample slides should be stained just prior to microdissection."

Total time: 45 mins coming to temp + ~15 mins staining + 10 mins to dry: 1 hour 10 mins