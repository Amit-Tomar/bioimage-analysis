---
layout: default
title: Tools
parent: Histopathology
nav_order: 2
---

# Tools
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

## Fiji

Fiji is an wrapper over ImageJ which has lot of plugins pre-installed and provides east updates to them. It provides high level operations like tracking, segmentation, directionality etc. and low level image operations like edge detection, background removal, blurring etc. UI for it is complex and so **best way to use it is by directly using the search box** for opening up the relevant plugin. Buttons in the **UI provide more options with right-click, double click**. Fiji has many inbuilt sample datasets which are a great source to test out Fiji. A typical worlflow looks like this :

1. Thresholding : Distinguish objects/background.
2. Set measurements : Select relevant attributes for measurements.
3. Analysze particles : Generates the results for selected attributes.

UI shows various attributes of an image with different labels : 

- c: Color.

- z: Current slice number along z-axis.

- t: Current position in time.

- Physical size of the image is also mentioned. **In case this information is not present in the meta-data, we have to set the correct measureemnts manually.** 

- Image dimensions.

- Bit depth

- Intensity value of the current pixel of the current channel.

### Brightness and Contrast 

Sometimes the images have values such that most of the values are distributes in a very small range of intensity values. This leads to a not of spread mapping ontp the lookup table. We can change the minimum and maximum values of the intensities in that case to get a broader spread of the intensities. These settings are to be done seperately for each channel.

### ROI

Region of interests can be selected by rectangle/oval etc tools. To do union of regions, press Shift while moving the mouse and to do substraction, press alt. **Brush tool allow to do selection freely**.

### Measurements

We can set the measurements we are interested in and then **calculate the values by pressing M key.**

### ROI manager

It can be used to keep a track of various ROIs we are interested in and then run measurement operation on them as required. **Press T key to add the ROI ti ROI manager**

### Further reading / References

1. [Lecture 2-10](https://www.youtube.com/watch?v=Akedfyp5AxY&list=PL5ESQNfM5lc7SAMstEu082ivW4BDMvd0U&index=2)