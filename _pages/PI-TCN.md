---
title: ""
permalink: /Autotune/
author_profile: true
---

<head>
<style>
.aligncenter {
  text-align: center;
}
p.title {
  text-align: center;
  font-weight: bold;
  font-size: 30px;
}
p.description {
  text-align: justify;
}

.column {
  float: left;
  width: 50%;
  padding: 5px;
}
.row::after {
  content: "";
  clear: both;
  display: table;
}

figure {
  text-align: center;
  margin-top: 72px;
  margin-bottom: 72px;
  display: block;
}
figcaption {
  text-align: center;
  font-style: italic;
  padding: 2px;
}
</style>
</head>

<p class="title">AutoTune: Controller Tuning for High-Speed Flight</p>

<p class="aligncenter"><a href="https://alessandrosaviolo.github.io/">Alessandro Saviolo</a>, <a href="https://lguanrui.github.io/">Guanrui Li</a>, <a href="https://scholar.google.it/citations?user=W8f0d6oAAAAJ&hl=en">Giuseppe Loianno</a></p>

<p class="aligncenter"><a href="https://ieeexplore.ieee.org/document/9696365?source=authoralert">Paper</a> <a href="https://github.com/uzh-rpg/mh_autotune">Code</a> <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">Video</a></p>

<figure>
<img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
<figcaption>Figure 1. Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h. We automatically find a controller configuration that can fly such a high-speed maneuver with a novel sampling-based method called AutoTune. To get a better sense of the speed achieved by the quadrotor, please watch the <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">supplementary video</a>.</figcaption>
</figure>

<p class="description"><b>Abstract.</b> Accurately modeling of quadrotor's system dynamics is critical for guaranteeing agile, safe, and stable navigation. The model needs to capture the system behavior in multiple flight regimes and operating conditions including those producing highly nonlinear effects such as aerodynamic forces and torques, rotor interactions, or possible system configuration modifications. Classical approaches rely on handcrafted models and struggle to generalize and scale to capture these effects. In this paper, we present a novel Physics-Inspired Temporal Convolutional Network (\textit{PI-TCN}) approach to learn quadrotor's system dynamics purely from robot experience. Our approach combines the expressive power of sparse temporal convolutions and dense feed-forward connections to extract time-dependent features to make accurate system predictions. In addition, physics constraints are embedded in the training process to facilitate the network's generalization capabilities to data outside the training distribution.
Finally, we design a Model Predictive Control (MPC) approach that incorporates the learned dynamics for accurate closed-loop trajectory tracking fully exploiting the accurate learned model predictions in a receding horizon fashion. Experimental results demonstrate that our approach accurately extracts the structure of quadrotor dynamics from data, capturing effects that would remain hidden to classical approaches. To the best of our knowledge, this is the first time physics-inspired deep learning is successfully applied to temporal convolutional networks and, in particular, to the system identification task, while concurrently enabling predictive control.</p>
