---
layout: page
title: Fully Automonmous Robot
description: CSCI3302 Final project 
img: assets/img/project_robo.jpg
importance: 1
category: work
related_publications: false
---

This project showcases the development of a fully autonomous robot capable of scanning, mapping, and retrieving objects from a simulated 3D supermarket. The project emphasizes LiDAR-based mapping and path planning using advanced robotics algorithms.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rrt_robo.jpg" title="rrt path algorithm" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mapping_robo.jpg" title="Mapping" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Programmed a TIAGo robot to autonomously scan, map, and retrieve objects from a 3D supermarket environment with 90% accuracy.
</div>

<div class="key-features mt-4">
  <h3>Key Features</h3>
  <ul>
    <li>Developed a <strong>2D map representation</strong> of the supermarket for effective navigation and <strong>path planning</strong>.</li>
    <li>Implemented <strong>Color Blob Detection</strong> using computer vision to identify objects on shelves.</li>
    <li>Utilized the <strong>RRT (Rapidly-exploring Random Tree) algorithm</strong> to compute optimal paths to target objects.</li>
    <li>Applied <strong>Inverse Kinematics (IK)</strong> for controlling the robot’s arm to retrieve objects in Cartesian space.</li>
  </ul>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/picking_robo.jpg" title="Picking Objects" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This project combines computer vision, path planning, and object retrieval to create an advanced, autonomous robot solution for real-world applications
</div>

<div class="project-video mt-4">
  <h3>Project Video</h3>
  <div class="embed-responsive embed-responsive-16by9">
    <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/K8VR4sO6eGA"  
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
    </iframe>
  </div>
</div>

<div class="project-repo mt-4">
  <h3>Project Repository</h3>
  <p>View the full code and documentation for this project on <a href="https://github.com/Ales4999/CSCI3302_LabTeam" target="_blank">GitHub</a>.</p>
</div>
