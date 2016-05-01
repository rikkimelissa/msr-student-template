---
layout: project
title: Robockey
date: December 11, 2011
image: robockey2.jpg
image2: robockey1.jpg
permalink: "robockey.html"
---

## Overview
This project was part of the course MEAM 410, Design of Mechatronic Systems, at the University of Pennsylvania. The goal of the project was to build a team of three autonomous robotic hockey players to compete in 'Robockey'. We built the robots, designed custom electronics for them to interface with the environment, and developed a state machine to organize their actions.

The robots use infrared sensors arranged radially around their bodies to see the puck (which glows with IR light). Position information is derived from a custom mWii sensor capable of detecting a constellation of infrared stars mounted above the rink. On the bottom of the robot is a four bar linkage system which uses a vertically mounted motor to shoot the puck as well as cutouts on the body to drive the puck. Game play consists of the robots working as a team to find the puck and get it into the opposite team's goal.

<p align="center">
<img src="{{site.baseurl}}/{{site.image_path}}/{{ page.image2 }}" width="600" />
</p>

Watch some highlights of our two offensive players attempting to drive the puck into the goal. 

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/C22qALZhxXI" frameborder="0" allowfullscreen></iframe>
</p>


