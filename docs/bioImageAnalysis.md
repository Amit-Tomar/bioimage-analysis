---
layout: default
title: Bio Image Analysis
nav_order: 2

---

# Tools
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

---

Bio image analysis involves different steps : 

1. **Pre-processing:** We convert the data into more usable form and remove different artifacts if present. This may require normalizing colors (eg. in case images are stained with different concentrations, different kind of scanners ) , re-orientation/registration for better alignment (different slices might require operations to be applied to align them as their correct physical orientations when they were part of single tissue) , reducing file size (for faster processing), background/noise removal (for easiely extractable features) etc.

2. **Filtering/Segmenting:** Extracting out the relevant structures (like cells) from the image.

3. **Analysis:** Analysing the attributes of extracted structures (like area/orientation/volume), relations among them, variation of properties across images/over-time (tracking).

etc.

## Image

An image is a collection of numbers arranged as a matrix. Each of this discrete value represent a Pixel (texel) or picture element. 

## Image Size

Image size is the number of pixels along the width of image vs the number of pixels along the height of the image.

## Pixel Size
 Pixel size refers to the physical distance associated with each pixel. In terms of the digital microscope, pixel size would refer to the physical size of the sensor associated with a single pixel of the captured image.

## Image Resolution (Pixel density)
 Image resolution is the number of pixels present on a physical 1 inch distance. 

## Microscope Resolution
 Microscope reolution is the smallest distance that can be captured by the microscope. In terms of digital microsope, it would refer to the smallest distance between two points such that microsope is able to distinguish between the signal value at these points. 

## Bit depth
 A bit depth of n represents that a total of 2<sup>n</sup> intensity values are possible in the image matrix. More bit depth leads to smoothness of intensities and thus much smoother image.

## Further reading

1. Understanding Resolution in Digital Microscopy Blog Post Teledyne Lumenera. https://www.lumenera.com/blog/understanding-resolution-in-digital-microscopy.
2. Photoshop image size and resolution. https://helpx.adobe.com/in/photoshop/using/image-size-resolution.html#about_pixel_dimensions_and_printed_image_resolution.
3. Methods to determine the size of an object in microns - OpenWetWare. https://openwetware.org/wiki/Methods_to_determine_the_size_of_an_object_in_microns.
4. Adding scale bars to images using ImageJ. http://www.swarthmore.edu/NatSci/nkaplin1/scalebar.htm.
5. A Guide to Choosing the Right Digital Microscope Camera for the Application. https://www.leica-microsystems.com/company/news/news-details/article/a-guide-to-choosing-the-right-digital-microscope-camera-for-the-application/.
6. DeRose, J. A. & Doppler, M. Guidelines for Understanding Magnification in the Modern Digital Microscope Era. Microscopy Today 26, 20–33 (2018). https://www.cambridge.org/core/journals/microscopy-today/article/guidelines-for-understanding-magnification-in-the-modern-digital-microscope-era/E99CB37B30B5DCF7654A17A44A6A682F
