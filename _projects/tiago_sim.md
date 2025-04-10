---
layout: page
title: Automonmous Robot Manipulator
description: CSCI3302 Final project 
img: assets/img//tiago/tiago.png
importance: 4
category: School
related_publications: false
---

## Project Overview

This project showcases the design and implementation of a **fully autonomous mobile manipulator** using the TIAGo robot platform.  
The robot is capable of **scanning**, **mapping**, **navigating**, and **retrieving objects** in a simulated 3D supermarket environment, combining **perception**, **path planning**, and **manipulation**.

The core focus was on developing robust autonomy using **LiDAR-based SLAM**, **RRT path planning**, and **inverse kinematics** — with 90% object retrieval accuracy.

---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tiago/rrt_robo.jpg" title="rrt path algorithm" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tiago/mapping_robo.jpg" title="Mapping" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Programmed a TIAGo robot to autonomously scan, map, and retrieve objects from a 3D supermarket environment with 90% accuracy.
</div>

---

## Key Features

- Developed a **2D occupancy map** of the supermarket using LiDAR for precise localization and navigation.  
- Implemented **Color Blob Detection** via OpenCV to identify and localize shelf items visually.  
- Used the **RRT (Rapidly-exploring Random Tree) algorithm** to compute efficient, collision-free paths in dynamic environments.  
- Applied **Inverse Kinematics** to control the robot’s 6-DOF arm for object manipulation in Cartesian space.  
- Integrated **perception, planning, and control** into a cohesive behavior tree for full autonomy.

---

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tiago/picking_robo.jpg" title="Picking Objects" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
  Combining path planning, vision, and manipulation — the TIAGo robot autonomously retrieves items from the shelf in simulation.
</div>

---
## Project Demo

Watch the full demonstration below:

<div class="project-video mt-4">
  <div class="embed-responsive embed-responsive-16by9">
    <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/K8VR4sO6eGA"  
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
    </iframe>
  </div>
</div>

---

## Technical Stack

- **Languages:** Python, Bash
- **Libraries & Tools:** ROS2, Webots, OpenCV, NumPy
- **Concepts:** SLAM, RRT*, Inverse Kinematics, Sensor Fusion, Behavior Trees

---

## Project Repository

<div class="project-repo mt-4">
  <p>View the full code and documentation for this project on <a href="https://github.com/Ales4999/CSCI3302_LabTeam" target="_blank">GitHub</a>.</p>
</div>
