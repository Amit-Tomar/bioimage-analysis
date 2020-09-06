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

1. TOC
{:toc}

---

# Fiji

Fiji is an wrapper over ImageJ which has lot of plugins pre-installed and provides east updates to them. It provides high level operations like tracking, segmentation, directionality etc. and low level image operations like edge detection, background removal, blurring etc. UI for it is complex and so **best way to use it is by directly using the search box** for opening up the relevant plugin. Buttons in the **UI provide more options with right-click, double click**. Fiji has many inbuilt sample datasets which are a great source to test out Fiji. A typical worlflow looks like this :

1. Thresholding : Distinguish objects/background.
2. Set measurements : Select relevant attributes for measurements.
3. Analysze particles : Generates the results for selected attributes.

UI shows various attributes of an image with different labels : 

* c: Color.

* z: Current slice number along z-axis.

* t: Current position in time.

* Physical size of the image is also mentioned. **In case this information is not present in the meta-data, we have to set the correct measureemnts manually.** 

* Image dimensions.

* Bit depth

* Intensity value of the current pixel of the current channel.

## Brightness and Contrast 

Sometimes the images have values such that most of the values are distributes in a very small range of intensity values. This leads to a not of spread mapping ontp the lookup table. We can change the minimum and maximum values of the intensities in that case to get a broader spread of the intensities. These settings are to be done seperately for each channel.

## ROI

Region of interests can be selected by rectangle/oval etc tools. To do union of regions, press Shift while moving the mouse and to do substraction, press alt. **Brush tool allow to do selection freely**.

## Measurements

We can set the measurements we are interested in and then **calculate the values by pressing M key.**

## ROI manager

It can be used to keep a track of various ROIs we are interested in and then run measurement operation on them as required. **Press T key to add the ROI to ROI manager**

## Image Operations

Various image operations we can perform in Fiji can be divided as follows :

1. Filteration

We apply an algorithm which modifies the intensity values of selected pixels in the image. eg.

- **Background noise / artifact removal**
Noise is an unintended change in the signal value while capturing/storing/handling the data. eg. not focused lens while capturing data using microscope, issue with analog-to-digital converter etc. With too much noise in the image, algorithms like segmentation find difficult to find relevant structures easiely. **When the variation in the background values is less, it is easy to differentiate the objects.** eg. workflow :

a. Extract the background

b. Substract/Divide the original image with the background

- **Contrast enhancement**
- **Correcting uneven illumination**

- **Types of Filters**

  1. Linear Filter
  We move a nxn matrix on all the pixels and then calculate the value at given pixel based on all pixels in this matrix. This matrix is called moving window/rolling ball. eg. replacing a pixel with average of all the pixels in moving window.

  2. Non-Linear Filter 
  Here the pixel is replaced but with a non linear value. eg. replace the value with mean/max/median of all pixels in the moving window. 

- **Edge detection**
It is used to extract out surfaces from the image. Applying a median filter before hand will help in getting a better output.

When we want to count the objects, it might make sense to substract the edges from the original image so that objects which are very close to each other get clearly seperated. This will give better results during the segmentation operation. eg. workflow :

 a. Extract the edges

 b. Substract the edges from original image.

2. **Segmentation**

For objects to be seperately identified in the images, we perform the segmentation operation. This involves replacing all the intensities in the image with just two, 0 and 1. This helps define clear boundaries of what is it that we consider as an individual object and where are its boundaries. It is a process of discreatisation of the image from large varying values. 

3. **Thresholding**

It is the process of defining certain threshold value, and all values above/below it are then replaced with this fix value. 

- **Otsu's method**
We consider all the possible threshold values from minimum to maximum intensity and plot the classes above/below the threshold value. We then calculate the variance in the pixel intensities in these classes. When the sum of variance of all the classes is minimal, it is a good point to do thresholding. Taking weighted variance (number of pixels in the class/total pixel * variance ) gives better results. [Further Reading](http://www.labbookpages.co.uk/software/imgProc/otsuThreshold.html)

We should not be finding the thresholding value manually and should reply on different algorithms.

- **Refining masks**

Images generated after thrsholding might not be perfect. We have to perform operations like binary opening/closing to refine the shapes further. 

## Further reading / References

1. [Lecture 2-10](https://www.youtube.com/watch?v=Akedfyp5AxY&list=PL5ESQNfM5lc7SAMstEu082ivW4BDMvd0U&index=2)


--- 