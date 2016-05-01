---
layout: project
title: D1GIT
date: May 1, 2012
image: d1gitTitle.png
image2: d2.png
image3: d3.png
image4: d4.png
image5: d5.png
image6: d6.png
image7: d7.png
image8: d8.png
image9: d9.png
image10: d10.png
image11: d11.png
permalink: "d1git.html"
---

## Overview
The goal of this project was to design an automated, temperature-calibrated measurement of capillary refill time. This was a year long senior design project with Dorsey Standish, Anat Bordoley, Craig McDonald, and Viraj Kalyani at the University of Pennsylvania.

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZLoK4BW4Wg0" frameborder="0" allowfullscreen></iframe>
</p>

Capillary refill time (CRT) is the time required for return of blood after application of blanching pressure to a distal capillary bed (typically a finger tip). It is used medically to test for shock and/or dehydration. We set out to make a compact device that standardizes the capillary refill time test, incorporating and facilitating all of the actions of a human doctor.

Our design goals were as follows: lightweight, inexpensive, safe, easily sterilized, and compact enough to fit in a lab coat pocket.

#### Mechanical Design

Preliminary testing showed that CRT is dependent on force applied with a p-value of .05. 
</p>
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image2 }}" width="600" />
</p>

Testing of compression by three doctors showed large inter-doctor variability in applied force.
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image3 }}" width="600" />
</p>

D1GIT features a 59 N/in spring calibrated to compress 0.1 in., which results in a 5.9 N force being applied to the patient’s finger. 
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image5 }}" width="600" />
</p>

The design for D1GIT went through four major design iterations.
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image4 }}" width="600" />
</p>

Here is the final design.
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image6 }}" width="600" />
</p>

#### Electrical Design

A phototransistor transmits current in proportion to the amount of light it receives. In the D1GIT, an IR LED and phototransistor in transmission detect the departure and return of blood flow.
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image7 }}" width="600" />
</p>

In healthy subjects, CRT is less than two seconds. In unhealthy patients (simulated by holding fingers in icy water), CRT can be up to 4.5 seconds. This sensing technology was validated through 60+ tests on subjects on varying race, gender, and body temperature. 

All of the onboard electronics were incorporated on a custom made printed circuit board. 

<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image8 }}" width="600" />
</p>
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image9 }}" width="600" />
</p>

#### Software Design

The intuitive lights and display signals guide the user through the capillary refill testing process. Embedded programming controlling the device can be represented by a finite state machine with five active states. Transitions between the states are triggered by events both internal and external to the microcontroller.

When the button is released, the microcontroller begins recording data. When the blood level stops changing (based on the value of the filtered, differentiated signal), the CRT time is measured. 
Previous research has determined an indirect linear relationship between skin temperature and CRT. D1GIT uses this algorithm to account for patient skin temperature, which is measured with an integrated zener diode.

<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image10 }}" width="600" />
</p>
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image11 }}" width="600" />
</p>

#### Commercial Use

In this project, we met all of our initial design goals. D1GIT is geared towards large-scale production. It is low-cost, with the prototype under $100 and further cost reduction with mass production. It is of small size, lightweight, and plastic form is easy to sterilize between patients.

#### Recognition

This project received the following honors:
<l>
<li> Tatnall Prize in MEAM for most outstanding senior design project </li>
<li> UPenn SEAS Design Competition, 2nd Honorable Mention </li>
<li> DEBUT: Design by Biomedical Undergraduate Teams, 2nd Honorable Mention - Diagnostic Devices </li>Category
</l>


