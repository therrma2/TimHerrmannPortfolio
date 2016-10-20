---
layout: project
title: DinoBot
date: March 18, 2016
image: mech/dino.jpg
---

## Project Goal

Design a line following robot that utilizes an android phone camera for line detection and communicates with a PIC microcontroller to drive motors and control the robot.

### Skills
* MCU programming
* Android application development
* CDC communication
* PCB design
* PID Control
* Laser cutting
* 3D printing

### Android Line Detecting Application

The Android phone is mounted in the middle of the robot facing forward.  The application accesses the camera and uses a set of color filters to identify the center of mass of the red line at 4 different horizontal locations in the image.  These values are sent to the microcontroller for use in the motor control loop.

<img style=" float:left; display:inline-block;margin:0px 5px" src="/TimHerrmannPortfolio/public/images/mech/line.png" height="400" alt="Line App"/>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Microcontroller and PCB Design

Components

* PIC32 MX250F128B microcontroller
* Mini USB port
* Reset and programmable user buttons
* Voltage regulator
* Power switch
* External 8MHz crystal oscillator
* Power and programmable LEDs
* H-Bridge
* Various capacitors and resistors

<img style=" float:left; display:inline-block;margin:0px 5px" src="/TimHerrmannPortfolio/public/images/mech/pcb.jpg" height="300"  alt="Line App"/>
<img style=" float:left; display:inline-block;margin:0px 5px" src="/TimHerrmannPortfolio/public/images/mech/pcb2.jpg" height="300" alt="PCB"/>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### Demo Video

<embed src="/TimHerrmannPortfolio/public/images/mech/dinobot.mp4" autostart="false" height="540" width="960" />