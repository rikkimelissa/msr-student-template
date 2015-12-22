---
layout: project
title: Baxter Pick and Place
date: December 10, 2015
image: baxter_pick.png
---

## Overview
This project was part of the course ME 495, Embedded Systems in Robotics, at Northwestern University. The main goal of this project was to use the Baxter robot to autonomously pick objects off of a work surface and place them in a container. The blocks can be placed at any position and orientation on the table, and they are also sorted by tag number into two groups.

We split the task into four main parts which are implemented through a state machine:

<l>
<li> Locating a block with tags using ar_track_alvar</li>
<li> Moving to above the block position using a joint trajectory</li>
<li> Adjusting the height using a Cartesian trajectory</li>
<li> Grabbing the block and dropping it in a specified position</li>
</l>

All of the code for this project is hosted on [this page](https://github.com/rikkimelissa/baxter_pick_and_place).

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/H4gZ741p81o" frameborder="0" allowfullscreen></iframe>
</p>


