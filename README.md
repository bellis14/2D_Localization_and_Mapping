# 2D SLAM Rover

## Objective
Create a low power mobile system with the functionality to simultaneously localize itself within its environment and generate 2D maps in real-time using laser scan data. 

## Description
The system is divided into three main parts, mobility, mapping, and visualization. The mapping portion is where real-time simultaneous localization and map processing is done to generate 2D maps with the aid of Google Cartographer, ROS, and 360 LiDAR. The mobility of the system is provided by the Sphero rover which is controlled remotely through the Sphero app via Bluetooth to manuever the system throughout its environment. As the rover advances through an area the 360 LiDAR mounted on top of the rover sends laser scan data to the Raspberry Pi via USB and the data gets processed by the Google Cartographer SLAM algorithm. When the data gets processed the map is displayed using ROS's 3D visualization tool called rviz. The map processing is done on the Raspberry Pi while the visualization is captured on a laptop, using a master/slave configuration through ROS on the same wifi network. Combined together the system can localize itselfs within its environment and generate a 2D map in real time on a small low power device.

## Project Build
![](project_images/project_build.JPEG)

## Software 
- Robot Operating System (ROS)
- Google Cartographer
- Ubuntu 20.04 Server version
- SolidWorks

## Hardware
- Raspberry Pi 4 with 4GB of RAM
- RPLidar A1M8
- 5V 3A power supply
- Sphero Rover
- 3D Printed Mount

## Improvements
The rover experiences poor map quality when the rover rotates and spins around. The map quality seen below was obtained by minimizing the amount of rotation. Given more time a inertial measurement unit (IMU) would have potentially resolved this issue and even enhanced the quality of the maps altogether.

## Map Quality
![](map_images/STC_First_Floor.png)
![](map_images/STC_Third_Floor.png)
![](map_images/Apartment_Plan.png)
![](map_images/Apartment_Floor_Plan.png)

## Accomplishments
This project won 1st place at the 2021 Fall Research and Creative Works Conference at Brigham Young University Idaho 

## Video Demonstration
https://youtu.be/31oRrxS-QlA


