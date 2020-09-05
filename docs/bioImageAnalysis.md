---
layout: default
title: Bio Image Analysis
nav_order: 2

---

Bio image analysis involves different steps : 

1. **Pre-processing:** We convert the data into more usable form and remove different artifacts if present. This may require normalizing colors (eg. in case images are stained with different concentrations, different kind of scanners ) , re-orientation/registration for better alignment (different slices might require operations to be applied to align them as their correct physical orientations when they were part of single tissue) , reducing file size (for faster processing), background/noise removal (for easiely extractable features) etc.

2. **Filtering/Segmenting:** Extracting out the relevant structures (like cells) from the image.

3. **Analysis:** Analysing the attributes of extracted structures (like area/orientation/volume), relations among them, variation of properties across images/over-time.

etc.