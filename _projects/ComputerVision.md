---
layout: project
title: Computer Vision
date: March 18, 2016
image: cv/cars.png
---

## Overview 
In EECS 332: Computer Vision, I was able to implement several computer vision algorithms from scratch, as well as a final capstone project at the end of the 10 week course.  Click the following links contain details and examples: 

* <a href="/TimHerrmannPortfolio/public/images/cv/MP1 - Tim Herrmann.pdf">Connected Component Labeling</a>
* <a href="/TimHerrmannPortfolio/public/images/cv/MP2 - Tim Herrmann.pdf">Morphological Operators</a>
* <a href="/TimHerrmannPortfolio/public/images/cv/MP3 - Tim Herrmann.pdf">Histogram Equalization</a>
* <a href="/TimHerrmannPortfolio/public/images/cv/MP4 - Tim Herrmann.pdf">Skin Color Detection</a>
* <a href="/TimHerrmannPortfolio/public/images/cv/MP5 - Tim Herrmann.pdf">Edge Detection</a>
* <a href="/TimHerrmannPortfolio/public/images/cv/MP6 - Tim Herrmann.pdf">Hough Transforms</a>

<img style=" float:left; display:inline-block;margin:0px 5px" src="/TimHerrmannPortfolio/public/images/cv/cv.png" height="400" alt="Comp Vision"/>

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

### <a href="/TimHerrmannPortfolio/public/images/cv/CarSpotting.pptx">Roadway Vehicle Detection and Counting (Final Project)</a>

Goal: Develop a method for identifying and counting vehicles using stock highway footage

* Identified moving portions of the image through background subtraction techniques in OpenCV
* Used morphological operators to clean up image and identify contiguous areas of moving pixels
* Set mimimum size of contiguous area to filter out noise
* Tracked the center of mass of these areas as they cross a line near the bottom of the image in order to count
