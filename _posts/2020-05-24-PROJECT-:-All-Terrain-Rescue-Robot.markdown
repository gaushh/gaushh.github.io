---
layout: post
title: PROJECT - All Terrain Rescue Robot
date: 2020-05-24 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: rakshak1.jpeg # Add image post (optional)
tags: [robotics computervision, arduino] # add tag
---
In this project we built an all-terrain mobile robot for environmental observation, surveillance and human assistance. This robot has been designed and configured to drive over just about any terrain and hence can be used for surveillance and most practical applications. This robot is Radio Controlled and has been upgraded with various sensors for better functioning. 

We built this project as a part of a competetion in our prefinal year and bagged second prize among 700 odd students. 

### METHODOLOGY
- The objective is to design a prototype of an All terrain rescue robot, and to integrate electronics with mechanical designs . 
- The proposed robot is to be fabricated with 6 wheels which are controlled by BLDC (Brushless DC) motors and coded using Arduino UNO.

### MECHANICAL STRUCTURE
- **Omni-terrain manoeuvrability** - Inspiration was taken by Martian rover Curiosity, which establishes the 'rocker-bogie suspension system. The primary mechanical feature of the robot is its true-blue allwheel-drive capability, which is achieved by 6 motors powering the six wheels of the robot.
- **Rocker-bogie suspension** - The rocker-bogie design has no springs or stub axles for each wheel, allowing the rover to climb over obstacles (such as rocks) that are up to twice the wheel's diameter in size while keeping all six wheels on the ground. 
- **Chassis** - Chassis is split in two parts, "front rocker" and "rear bogie". Entire frame, axles designed using PVC pipes.
- Brushless DC motors have been used for movement. The motors have 6mm shaft diameter and have maximum capacity of 30 RPM.

![Rocker Bogie mechanism]({{site.baseurl}}/assets/img/Rocker_bogie.gif)

### Hardware Architecture
Three possible modes of Communication
- **Bluetooth Module (HC-05)**: It is interfaced with the Arduino and the mobile phone app.
- **Transmitter-Receiver**: It uses RF module that sends and receive the radio signals
- **Ultra Sonic Sensor (HC-SR04)**: makes the Robot autonomous and collision-proof
- **Motors** : 12 v, 6 mm shaft diameter  brushless dc motor.
- **Wheels** : 125 mm, width of 60 mm, shaft diameter of 6mm.

### Software Architecture
Software architecture of our robot was designed keeping in mind it’s varied applications and to successfully implement it into the hardware part. Heart of the software  architecture lies in it’s processor which in our case is arduino uno which supports the following applications
