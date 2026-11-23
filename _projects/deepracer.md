---
layout: page
title: Autonomous Vehicle Competition
description: Team-built autonomous DeepRacer-style car using ROS 2, camera line following and PID control
img: /assets/img/deepracer/aws_thumb.png
importance: 1
category: School
---

## Project Overview

Final project for **CSCI 4302/5302 Advanced Robotics** at CU Boulder (Spring 2025), built by a team of five ("How Hard Can It Be"). Each team built a vehicle that drives a closed-loop indoor track fully autonomously, judged on average lap time and on the challenge features it completes.

We chose four challenges worth 9 points: **camera-based line following** (5), **stop-sign detection** (2), **two different control approaches** (1) and a **vehicle telemetry visualizer** (1).

We deliberately kept the design simple. Instead of computationally heavy methods such as SLAM or an EKF, the car follows blue tape marking the track centre, and a tuned **PID** controller does the steering.

---

## My role

I built the **telemetry visualizer**: a ROS 2 node that subscribes to the robot's topics and draws a live dashboard with:
- the lidar point map around the robot
- the camera feed with the line-detection overlay
- throttle and steering commands
- a line-error graph showing how far the car is from the line

The team used it to tune the controller and debug the robot by comparing what we expected with what the robot was doing.

---

## How it works

- **Perception:** the camera frame goes through an HSV mask that isolates the blue tape. Line detection computes a "line error" (distance between the frame centre and the path line) and detects corners ahead of sharp turns.
- **Control:** a PID steering node with tuned gains and a second-order derivative estimate. A velocity-scaling rule slows the car on sharp turns. A bang-bang controller was the comparison baseline; it oscillated and was dropped.
- **Stop signs:** a red colour mask plus contour area and side-length checks detect the sign. A state machine stops, waits, then continues.
- **ROS 2 topics:** `image_raw` → line error → `cmd_vel` to the servo driver; the lidar `scan` topic feeds obstacle handling.

---

## Hardware

- Raspberry Pi 4 (8 GB) on a laser-cut base plate, PCA9685 servo hat (I2C) for throttle and steering
- RPLiDAR A1, Raspberry Pi Camera v2 on an adjustable mount
- Two power supplies (2S LiPo for the motors, a separate battery for the Pi)
- Rebuilt frame and lidar mount so the battery sits below the Pi for stability

---

## What we learned

The heuristic, vision-only approach worked in the controlled track but struggled at higher speeds because of sensor noise and throttle nonlinearities. A successive-loop-closure controller (lidar wall-centering outside, camera line-following inside) was explored but not finished in time. The next step would be proper state estimation (for example an EKF) and SLAM.

---

## Technical Stack

- **Software:** ROS 2, Python, OpenCV, NumPy, Matplotlib, Linux
- **Control:** PID (primary), bang-bang (baseline), velocity scaling
- **Hardware:** Raspberry Pi 4, RPLiDAR A1, Pi Camera v2, PCA9685

---

## Visuals

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/deepracer/aws_logo.png" title="AWS DeepRacer" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/deepracer/aws_robo.png" title="Our team's vehicle" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
