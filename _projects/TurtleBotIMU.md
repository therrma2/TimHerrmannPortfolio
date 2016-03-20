---
layout: project
title: TurtleBot IMU Integration
date: March 18, 2016
image: IMU.jpg
---

## Overview 
The goal of this project was install an IMU on the TurtleBot and 
fuse the IMU sensor data with existing odometry data to gather a more accurate pose estimate.  In doing so, I was able to develop knowledge, experience, and skills pertaining to the following topics:

* ROS Nav Stack
  *  Mapping
  * Localization
  * Local and Global Planning
* 3D Printing
* IMU Calibration
* Sensor Fusion Through Extended Kalman Filters (EKF)




### Hardware

* TurtleBot 2
* Razor 9DOF IMU


<img style=" float:left; display:inline" src="/TimHerrmannPortfolio/public/images/tbot.png" height="200" alt="TurtleBot 2"/>

<img style=" float:left; display:inline" src="/TimHerrmannPortfolio/public/images/IMU.jpg" width="200" alt="Razor 9DOF IMU"/>


<br><br><br><br><br><br><br><br><br><br><br>


### 3D Printing and IMU Mounting
When mounting the IMU on the TurtleBot, an attempt was made to make the IMU as close as possible to coaxial with the TurtleBot base in order to minmize IMU translation due to pure rotation of the robot.  To do this, a customer 3D mounting bracket was printed using the Ultimaker 2 3D printer.

<img style=" float:left; display:inline" src="/TimHerrmannPortfolio/public/images/printer.JPG" width="200" alt="Ultimaker 2"/>
<img style=" float:left; display:inline" src="/TimHerrmannPortfolio/public/images/bracket.JPG" width="200" alt="Bracket"/>
<br><br><br><br><br><br><br><br><br>
<img style=" float:left; display:inline" src="/TimHerrmannPortfolio/public/images/mountedbracket.JPG" width="200" alt="Bracket With IMU"/>
<img style=" float:left; display:inline" src="/TimHerrmannPortfolio/public/images/fullmount.JPG" width="200" alt="Fully Mounted IMU"/>
<br><br><br><br><br><br><br><br><br><br><br>
LINK .STL FILE

###Setup and Calibration
ROS Drivers, as well as full calibration procedures for the Razor 9DOF IMU can be downloaded from <http://wiki.ros.org/razor_imu_9dof/>
Sample calibration results: PUT A LINK HERE

### Sensor Integration
IMU and Odometry Integration was performed using the ROS package 'Robot_Localization'.  This package uses and Extended Kalman Filter to fuse multiple sensor streams into a pose estimate.

Fused Sensor Components:

* Odometry
  * x position
  * y position
  * yaw
  * x velocity
  * y velocity
  * yaw velocity

* IMU
  * yaw
  * x acceleration

Full Robot_Localization launch file:

Diagonal Covariance Matrix Values [x,y,z,roll,pitch,yaw]:

Odometry [x,y,z,roll,pitch,yaw]: [.1, .1, INF, INF, INF, .05]

FILL THIS IN!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
IMU [x:


### Results
The robot was driven thorugh a series of motions, and using an overhead camera and the <a href="https://github.com/NU-MSR/overhead_mobile_tracker">overhead_mobile_tracker</a> package developed by Jarvis Shultz, a ground truth pose was measured and compared to pose output by /odom on it's own, and the pose output by the fused sensor data on the /odometry/filtered topic.  The results show a significant improvement in pose accuracy in both translation and rotation.


      
### Video
<iframe width="420" height="315" src="https://www.youtube.com/embed/DTr0OkBim4M" frameborder="0" allowfullscreen></iframe>


### Github Link:
<https://github.com/therrma2/Baxter-Pick-And-Place>