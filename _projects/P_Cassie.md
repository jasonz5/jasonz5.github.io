---
layout: page
title: Simulated Cassie Robot with Gait Design and Path Planning
description: 
img: assets/projects/cassie/cover.png
importance: 2
category: Projects
---

This is the course project of Walking Robot, supervised by Prof. Chenglong Fu at SUSTech. For more information, view [Porject Report](/assets/projects/cassie/report.pdf) (currentlly only Chinese version).

### Introduction

Cassie is a robot which was designed based on the joints that birds usually have. Based on Cassie's open-source robot urdf model on GitHub, this paper first introduces the structure of the robot, and applies the 3d linear inverted pendulum model to the gait planning of the robot, and uses pybullet to demonstrate the robot's ability to walk upright, climb stairs and turn around. In short of the time our group are not able to complete the controller that enable the robot to stand on the ground. So we complete our path planning on the open-source model developed by Caltech. Our group compared the global path planning algorithm and the local path planning algorithm of mobile robot. After locating the obstacles by computer vision, the artificial potential field method is used to plan the path independently, and the application of obstacle avoidance algorithm for robot around the pile are realized on Gazebo platform (Ubuntu).

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/projects/cassie/2d_lip.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
     Two-dimensional inverted pendulum: The simplest model of a bipedal walking robot, consisting of a point mass and a massless, extendable leg. Its deflection angle &theta is based on the vertical axis, with the clockwise direction being positive.
</div>

### Results

The following videos show the walking forward and stair climbing of cassie robot based on Pybullet.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/projects/cassie/video/forward1.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/projects/cassie/video/forward2.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Straight Walking
</div>


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/projects/cassie/video/climb1.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/projects/cassie/video/climb2.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Stair Climbing
</div>
