---
layout: page
title: Kinematics Optimization for Redundant Manipulators
description: Kinematics optimization for redundant manipulators based on MATLAB Simcapse for object tracking.
img: assets/img/projects/redundant_arm/cover.png
importance: 1
category: SUSTech
---

## Motivation
The seven-degree-of-freedom redundant robotic arm not only possesses the excellent characteristics of a redundant robotic arm but also maintains the high rigidity of the robotic arm. Due to the extra degree of freedom, the seven-degree-of-freedom redundant robotic arm has good fault tolerance, singularity position avoidance, and torque optimization. By constructing an optimization model, achieving good dynamic performance of the robotic arm, it can ensure smooth joint movement while completing specific tasks under physical, hardware, and control constraints, and achieve optimization of certain variables.

The solution to Quadratic Programming (QP) problems is an important topic in the fields of mathematical programming and industrial applications. Many practical engineering problems can be converted into QP problems for solution. Therefore, QP problems and their solutions are widely and deeply researched by researchers and engineering application personnel. The algorithm for solving QP problems is widely used in many scientific fields such as power dispatch, optimal controller design, and traffic signal control.

In previous research, generally only situations subject to one or two typical constraints (such as linear equations and inequality constraints) are discussed. However, the quadratic programming problems in actual engineering applications are often subject to multiple constraints at the same time: equation constraints, inequality constraints, and double-ended constraints. This project is to convert the specific tasks of the redundant robotic arm into quadratic programming problems and achieve optimization under various constraints.

## Related Work
Redundant degree-of-freedom robots, while ensuring the end-effector motion law, use self-motion in the null space to generate different configurations, thus enabling the robot to use the redundant degrees of freedom to avoid obstacles, overcome singularity, improve flexibility, and achieve better dynamic performance. Because of their inherent advantages, redundant robots are attracting more and more attention, and many scholars have conducted extensive research on this topic, achieving impressive results. The main content of the research includes: how to use the extra degrees of freedom of redundant robots to improve the robot's kinematic and dynamic characteristics, such as increasing flexibility, avoiding obstacles, overcoming singularity, optimizing auxiliary operation indicators under the main motion task, and optimizing joint speed, acceleration, torque, energy, etc.

## My Task

For a specific task (the object is moved along the specified planned trajectory, a 7DOF redundant robotic arm end is equipped with a camera, the camera normal needs to face the moving object and track it in real time, under the physical constraints of joint angles, angular velocity, etc., while ensuring that the camera moves at the minimum speed in Cartesian space), using the existing 7DOF robotic arm model, in the simulation environment of Matlab simulation tool Simscape Multibody, set up an object trajectory planning framework, write 7DOF kinematics code and implement the inverse kinematics framework, and convert this specific task into a quadratic problem and implement the code and successful simulation in the simulation environment. At the same time, in some unsolvable situations during the camera view tracking process, introduce slack variables and define task priorities (high priority is camera view tracking objects, low priority task is to optimize end speed, ensure minimum), and finally successfully implement the optimization of the quadratic in the specific task of the redundant robotic arm.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/redundant_arm/slack_var.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/redundant_arm/end_vel.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     (Left) Figure a: Adding slack variable to the qp model. (Right) Figure b: Speed of the end-effector camera.
</div>


According to the target task, the target function defined is the speed of the end camera, and the control quantity is the joint angular velocity. After quadratic programming, the optimized target function is shown in Figure b, and the first two seconds of Figure b correspond to the situation where QP has no solution under constraints, that is, the slack variable in the first two seconds of Figure a is not zero. Above is the change of the two values in the simulation results after QP solving under the conditions of high priority for the camera view tracking objects, low priority for optimizing the end speed, and the tracking object has a definite motion plan.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/task2_trap.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Task simulation in MATLAB Simscape.
</div>

