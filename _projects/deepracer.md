---
layout: page
title: Autonomous Vehicle Competition
description: A competition-grade autonomous racing platform using ROS2, LiDAR, PID, and MPC
img: /assets/img/deepracer/aws_thumb.png
importance: 1
category: School
---

## Project Overview

This project was developed as part of a competitive robotics challenge to build a custom **AWS DeepRacer** platform.  

Using a **Raspberry Pi**, **LiDAR**, **camera**, and **ROS2**, the team engineered a fully autonomous system capable of navigating a closed-loop track with real-time obstacle avoidance, robust localization, and adaptive path planning.

Our team focused on building a reliable and fast robot for the indoor track competition, prioritizing robust control, accurate localization, and real-time responsiveness.

---

## Development

We develop the **robot’s localization and control stack**, including:

- Engineering a LiDAR-based **Extended Kalman Filter (EKF)** fused with **optic flow** from the Pi Camera to estimate velocity and heading without relying on an IMU.
- Implementing **PID** and **Model Predictive Control (MPC)** strategies for high-speed maneuvering and trajectory stabilization.
- Designing the **A\*** path planning algorithm for route selection, integrating real-time obstacle detection and avoidance.
- Achieved 100% lap completion with minimal deviation and smooth turns on a tight indoor track.

---

## Hardware Integration

Building the autonomous DeepRacer platform required seamless coordination between various hardware components. The integration process included:

- **Raspberry Pi** served as the central processing unit, running ROS2 nodes for perception, planning, and control.
- **2D LiDAR** was mounted on the chassis to provide distance measurements for localization and obstacle detection. Data was published to ROS topics and fused using an EKF node.
- A **Pi Camera** was positioned forward-facing, used for optic flow estimation and basic visual localization.  
- A **custom 3D-printed sensor mount** was designed to align all sensors for minimal distortion and secure operation on the track.
- **Motor controller and wheel encoders** were configured to receive motion commands via ROS2 `cmd_vel` topics, enabling velocity and turn rate execution.

This modular hardware setup enabled us to test and tune components individually, then synchronize them for full autonomy in real-time racing conditions.

---

## Key Features

- LiDAR-driven **EKF localization**, improved by 80% using optic flow for poor-man’s IMU estimation.
- Dual-controller design using **PID** and **MPC** for comparison, improving **trajectory stability by 60%**.
- Real-time **path planning** using A* on a pre-mapped environment with dynamic obstacle avoidance.
- Modular **ROS2-based architecture**, supporting flexible debugging and visualization tools.
- Completed full laps with **100% reliability** in a constrained indoor environment.

---

## Technical Stack

- **Hardware:** Raspberry Pi, 2D LiDAR, Pi Camera, custom sensor mount  
- **Software:** ROS2 (Foxy), Python, OpenCV, NumPy, FFmpeg, Linux  
- **Control Systems:** EKF, PID, MPC  
- **Planning:** A*, real-time obstacle detection and avoidance  
- **Tools:** RViz, ROS2 Nodes, Custom Visualizers, Git

---

## Visuals

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/deepracer/aws_logo.png" title="Path Planning Map View" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/deepracer/aws_robo.png" title="Custom DeepRacer Hardware" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

---

## Competition Context

This work was completed for **CSCI 5302: Advanced Robotics** at CU Boulder.  
The robot was evaluated based on performance in the **indoor track competition**, with objectives including fast lap time, successful obstacle avoidance, and stable localization without GPS or traditional IMUs.

Our solution focused on minimal sensor use, prioritizing algorithmic efficiency, redundancy, and reliability.