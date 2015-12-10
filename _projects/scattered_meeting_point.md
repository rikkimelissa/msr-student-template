---
layout: project
title: Weighted Terrain Meeting Point
date: November 20, 2015
image: p11.png
image1: p12.png
image2: sp2.png
image3: p31.png
image4: p14.png
image5: p32.png
---

## Overview
This project was part of the course EECS 495, Computational Geometry, at Northwestern University. The goal of the project was to implement an algorithm to calculate the meeting point of scattered robots on weighted terrain surfaces, based on the algorithm detailed in [this paper](http://people.scs.carleton.ca/~lanthier/personal/cv/CATS2005_8.5x11.pdf) by Mark Lanthier, Doron Nussbaum, and Tsuo-Jung Wang. 

The algorithm consists of three main parts:
<l>
<li> Calculating the Delaunay triangulation for a set of points in 3D space.</li>
<li> Constructing a graph of Steiner points and edges at ten per edge of the original triangulation.</li>
<li> Invoking a shortest path algorithm from each of the source vertices on which the robots are positioned. The algorithm is modified as a multiple-source single-target variation such that the algorithm stops at some vertex which is the approximating meeting point.</li>
</l>

All of the code for this project is hosted on [this page](https://github.com/rikkimelissa/scattered-robots-meeting-point).

The triangulation of a sample terrain:
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image2 }}" width="600" />
</p>

Two examples of found meeting points for robots starting at random vertices. The contour map is shown with the start locations of each robot displayed as a circle of the robot's color, each robot's path in a different color, and the calculated meeting point shown as a black circle.
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image1 }}" width="300" />
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image3 }}" width="370" />
</p>
<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image4 }}" width="370" />
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image5 }}" width="370" />
</p>


