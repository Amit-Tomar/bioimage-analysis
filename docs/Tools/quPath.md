---
layout: default
title: QuPath
parent: Tools
nav_order: 2
---

# QuPath

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
QuPath is open source software for bioimage analysis which is used for digital pathology ,specially whole slide image analysis.

## Annotations

## Color Deconvolution in QuPath
QuPath has the ability of digitally seperating out the various stain merkers (utpo 3) from the image. (An important distinction is that it is not just seperating the channels, rather deriving the stain colors from th e combinedcolors of image). Pressing buttons 1,2,3,4.. switches between these values. Using brightness/contrast buttons, we can also do the same operation along with changing the min/max values of the histogram distribution of each extracted layer seperately. 

## Cell detection
QuPath can run cell detection based on some user specified parameters like threshold intensity, area etc. 

1. Measurement maps
2. Visualize only nucleous or cell
3. Cell fill : Ctrl + F
4. Individual detected cell measurements

## Positive Cell detection
Cell detection with added feature of finding positive/negative cells.

After the cell detection has been done by one of the above methods, we can also run object classifiers on top of it by annotation certain cells as positive/negative etc.

1. Object based classifier
Mark annotations and add classes. Select only a small rectangle to see the %age of classes in that region.

2. Pixel based classifier
Can be directly run on the image by assigning some classes to the annotations.

## Futher reading / References

1. [Official QuPath tutorials](https://www.youtube.com/c/qupath) explains all the use cases nicely.
2. [Quantitative Pathology & BioImage Analysis: QuPath - [NEUBIASAcademy@Home] Webinar](https://www.youtube.com/watch?v=4An5n6Y_rRI&feature=youtu.be)
3. [QuPath 2020 workshop “From Samples to Knowledge”](https://www.youtube.com/playlist?list=PLlGXRBscPbCD89fRULm4peopF57qugciN)
--- 