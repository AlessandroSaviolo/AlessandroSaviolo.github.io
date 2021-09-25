---
title: "PCMPC: Perception-Constrained Model Predictive Control for Quadrotors with Suspended Loads using a Single Camera and IMU"
<!--collection: publications-->
permalink: /publications/PCMPC2021ICRA
---

<b>Authors: </b> Guanrui Li\*, Alex Tunchez\*, Giuseppe Loianno

<head>
<style>
* {
  box-sizing: border-box;
}

.column {
  float: left;
  width: 50.0%;
  padding: 5px;
}

.example-cover img {
  height: 280px;
  object-fit: cover;
}

.row::after {
  content: "";
  clear: both;
  display: table;
}
  
</style>
</head>

<body>
  
<div class="row">
  <div class="column">
    <img src="https://lguanrui.github.io/images/pcmpc2021icra.jpg" alt="icra2021" style="width:100%">
  </div>
  <div class="column">
    <iframe height="300px" src="https://www.youtube.com/embed/BBWt1xG7Rrw">
    </iframe>
  </div>
</div>
  
</body>

## Abstract
In this paper, we address the Perception-Constrained Model Predictive Control (PCMPC) and state estimation problems for quadrotors with cable suspended payloads using a single camera and Inertial Measurement Unit (IMU). We design a receding--horizon control strategy for cable suspended payloads directly formulated on the system manifold configuration space \text{$SE(3)\times S^2$}. The approach concurrently takes into account the system dynamics, actuator limits and the camera's Field Of View (FOV) constraint to guarantee the payload's visibility during motion. The monocular camera, IMU, and vehicle's motor speeds are jointly combined to provide an estimate of states of the vehicle in 3D space as well as the payload's state and the cable direction and velocity. The proposed control and state estimation solution runs in real-time at 500 Hz on a small quadrotor equipped with a limited computational unit. The approach is validated through experimental results considering a cable suspended payload trajectory tracking problem at different speeds.

