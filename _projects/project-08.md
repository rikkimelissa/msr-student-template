---
layout: project
title: Baxter Pick and Place
date: December 10, 2015
image: baxter_pick.png
permalink: "pick-and-place.html"
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

#### Detecting the block with AR tracking  <a name="Vision"></a>
In this state, ar_track_alvar is used to find the block positions and orientations. Each block has a unique tag; if multiple blocks are found, the block that is closest to the current position will be used. 

#### Moving above the block  <a name="Movement"></a>
In this state, a joint trajectory is calculated to move between from the current position to 10 mm above the block. The joint angles for the gripper position at the block is calculated through inverse kinematics and transformed to the robot's base frame. The joint trajectory is then calulcated with quintic time scaling and the joint positions are sent sequentially to move the gripper to the desired position.

#### Adjusting the height  <a name="fine"></a>
In this state, a Cartesian trajectory is used to hold the orientation of the gripper constant and just change the height as the gripper moves closer to the block. The laser range data from Baxter's hand is used in a feedback loop to determine when the gripper has reached the block.

#### Dropoff <a name="drop"></a>
In this state, the gripper grabs the block and moves to drop it off in a specified location. The blocks are sorted into two groups using metadata from the AR tags to specify which dropoff location to use.