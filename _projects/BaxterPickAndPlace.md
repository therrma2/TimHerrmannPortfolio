---
layout: project
title: Baxter Pick and Place
date: December 10, 2015
image: baxter.jpg
---

## Overview
As a final project for ME495: Embedded Systems in Robotics, students competed in groups of 4 to program Rethink Robotics' Baxter robot to pick 6 objects from a table and place them in a box.  Points were awarded for speed and for introducing various degrees of difficulty and robustness to the process.  Programming was done in Python utilizing ROS.

### Project Team
*  Tim Herrmann  
*  Mikhail Todes  
*  Yunchu Liu  
*  Minghe Jiang  

### Github Link:
<https://github.com/therrma2/Baxter-Pick-And-Place>


### Object Detection and Image Processing
For object detection, we utilized the camera built into Baxter's hand.  Using OpenCV, we filtered the image for red and green pixels and drew a rectangular bounding box around the largest collection of pixels.  A gui is provided that allows HSV values to be changed on the fly if other colors are desired.


### End Effector Positioning and Orientation
To aid in centering the gripper above the object, the end effector remains locked in the upright position throughout the pick process.  Using calibrated meter per pixel values, the end effector is moved so that the detected object is centered correctly.  To align the gripper with the orientation of the block, we calculate the slope of the the bottom line of the rectangular bounding box and rotate the gripper until the slope is zero.


### Inverse Kinematics
For joint angle calculations, we utilize Baxter's built-in IK solver.  To ensure the IK Solver convergees, we use a set of user defined seed angles.  It will start with current joint angles as the seed, and if that fails, will add random noise until a solution is generated.


### Competition Results
Our group managed to win 1st place in the final competion with a combination of the second fastest time and multiple added degrees of difficulty.

Capabilities:

   - Dynamic Image Processing
   - Object Variation
      * Color
      * Size
      * Shape
      * Orientation
      
### Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/Uo60e5Leo50" frameborder="0" allowfullscreen></iframe>


