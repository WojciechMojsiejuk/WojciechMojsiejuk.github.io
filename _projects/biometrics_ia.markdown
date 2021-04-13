---
layout: page
title: Biometrics - Image processing
description: histogram, binarizations, filters
img: /assets/img/biometrics/ia/usgs-Eu2uXqoHenE-unsplash.jpg
importance: 3
github: https://github.com/WojciechMojsiejuk/PodstawyBiometrii01
---


Photo by <a href="https://unsplash.com/@usgs?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">USGS</a> on <a href="https://unsplash.com/s/photos/image-processing?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

This is one of projects for Biometrics Basics course from 6th semester (Summer Semester 2019/20)

> **Features**
* Operations on the File: Create New, Load, Save, Quit
* Convert to BW
* Gamma Correction
* Update pixel value (RGB)
* Histogram
    * Plot
        * R Channel
        * G Channel
        * B Channel
        * AVG
    * Normalization
    * Equalization
        * Grayscale
        * YCrCb
* Binarization
    * Otsu
    * Binary Threshold
    * Niblack
* Filter
    * Prewitt
    * Sobel
    * Laplace
    * Edge Detection
    * Median
    * Box Blur
    * Gaussian Blur
    * Kuwahara


> **Technology** 
* GUI: PyQt5
* Data Visualization: Matplotlib
* Operations on data: NumPy 

***

Screenshots
----

***

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/1.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Main Window
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/2.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Histogram
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/3.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Gamma Correction
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/4.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Grayscale
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/5.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Histogram Equalization
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/5_hist.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Equalized Histogram
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/6.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Error Message
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/7.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Binary Thresholding
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/8.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Kuwahara Filter
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/biometrics/ia/9.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Laplace Filter
</div>