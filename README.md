# Localization_ROS2_iCreateRobot
Data Fusion Architecture - Localization Problem with ROS2 and iCreate robot

<img src="one.jpeg" alt="Alt text" width="500" height="300" align="center">

## Problem statement
This project aims to create a localization system using bayesian statistics: Particle Filter and Kalman Filter. The localisation software should be created in python and implementing bayesian interference for the sensor system of the iCreate3 robot. 

## Hypothesis
Using the sensor data from the internal measuring usint (imu) and the wheel encoders should allow the computation of position and orientation estimates. This can be used in combination with a particle filter to estimate the position of the robot. The robots existing odometry can be used to check the validity of the implemented localisation system.

## Main part
Extract data and calculation of the velocity(from imu, encoders and fused in Kalman Filter) leads to this result:

<img src="fused.png" alt="Alt text" width="600" height="300" align="center">

As a result we can see that Encoder Velocity is more stable and consistent. IMU velocity - while times goes the error is growing. The fused velocity that shows more flexible and adaptive pattern.

Getting all the calculation together and applying in Particle Filter:

<img src="result.png" alt="Alt text" width="600" height="300" align="center">
