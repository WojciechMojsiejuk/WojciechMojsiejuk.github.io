---
layout: page
title: Genetic Algorithm
description: finding extrema of a functions of two variables
img: /assets/img/geneticalg/alexander-popov-eXoXJrOGqG4-unsplash.jpg
importance: 2
github: https://github.com/WojciechMojsiejuk/genetic-algorithms
---
  
Photo by <a href="https://unsplash.com/@5tep5?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Alexander Popov</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

This is my final project for Artificial Intelligence course from 4th semester (Summer Semester 2018/19), conducted in cooperation with [Pawel](https://github.com/pa-b). 

For function parsing we used SymPy symbols and lambdify function which results then were computed using NumPy ndarrays. 

PyQt5 as a GUI, Matplotlib as a data visualisation. 

> **Features**
* Defining function of two variables, its domain and range
* Parsing function
* Function visualization in 3D with possibility to manipulate angles of a 3D object
* Defining crossover, mutation probability, number of individuals and epochs in GA
* Plot of each generation
* Summary with chromosome which values will give the best solution
* Plot of best, median and mean value in each epoch

***

Screenshots
----

***

**Functions visualization, setting function domain and range**

$$ x^2 + y^2; x \in \langle -2, 2 \rangle y \in \langle -2, 2 \rangle  $$

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/1.png' | relative_url }}"/>
    </div>
</div>
<br/>

$$ x^3 + y^2; x \in \langle -3, 3 \rangle y \in \langle -4, 4 \rangle  $$

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/6.png' | relative_url }}"/>
    </div>
</div>

<br/>

$$ -x^2 + 3 \cdot y; x \in \langle -3, 3 \rangle y \in \langle -4, 4 \rangle  $$

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/7.png' | relative_url }}"/>
    </div>
</div>

<br/>

**Solving genetic algorithm**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/2.png' | relative_url }}"/>
    </div>
</div>

<br/>

**Generation plots**

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/4.png' | relative_url }}"/>
    </div>

    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/3.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Heatmap and points representing chromosomes' value. First generation (left), last generation (right).
</div>

<br/>

**Summary**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/5.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Chromosome values which will result in the best solution. Plot for best, median and mean in each generation.
</div>

***

Remaster
----

***

In 2019 Pawel and I decided to update this project further and with our colleague Daniel we created a new version for Building Desktop Applications using WPF course from 6th Semester (Summer Semester 2019/20). We rewrite whole project to C# and add additional featues such as:

* now many functions with various algorithm parameters can be computed at the same time 
* results can be exported to PDF file

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/1.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Main window
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/2.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Adding function
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/3.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Adding algorithm parameters
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/4.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Main window with added functions and parameters
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/5.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Selecting which functions and parameters are being fit
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/6.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Obtained result
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/7.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Result's raport I
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/8.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Result's raport II
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/9.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Result's raport III
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/11.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    Exporting results to PDF
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'assets/img/geneticalg/remaster/12.png' | relative_url }}"/>
    </div>
</div>
<div class="caption">
    PDF file
</div>