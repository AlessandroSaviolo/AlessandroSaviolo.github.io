---
title: ""
permalink: /PI-TCN/
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

<p class="title">Physics-Inspired Temporal Learning of Quadrotor Dynamics for Accurate Model Predictive Trajectory Tracking</p>

<p class="aligncenter"><a href="https://alessandrosaviolo.github.io/">Alessandro Saviolo</a>, <a href="https://lguanrui.github.io/">Guanrui Li</a>, <a href="https://scholar.google.it/citations?user=W8f0d6oAAAAJ&hl=en">Giuseppe Loianno</a></p>

<figure>
<img src="/images/pitcn_1.jpg" alt="Long-exposure photo showing multiple laps over Lemniscate trajectory when using the nominal (NOM) and the proposed (PI-TCN) dynamics." style="width:100%">
<figcaption>Figure 1. Long-exposure photo showing multiple laps over Lemniscate trajectory when using the nominal (NOM) and the proposed (PI-TCN) dynamics. The reference trajectory (white) is approximately projected on the image based on real-world experiments for illustrative purposes.</figcaption>
</figure>

<p class="description"><b>Abstract.</b> Accurately modeling quadrotor's system dynamics is critical for guaranteeing agile, safe, and stable navigation. The model needs to capture the system behavior in multiple flight regimes and operating conditions, including those producing highly nonlinear effects such as aerodynamic forces and torques, rotor interactions, or possible system configuration modifications. Classical approaches rely on handcrafted models and struggle to generalize and scale to capture these effects. In this paper, we present a novel Physics-Inspired Temporal Convolutional Network (PI-TCN) approach to learning quadrotor's system dynamics purely from robot experience. Our approach combines the expressive power of sparse temporal convolutions and dense feed-forward connections to make accurate system predictions. In addition, physics constraints are embedded in the training process to facilitate the network's generalization capabilities to data outside the training distribution. Finally, we design a model predictive control approach that incorporates the learned dynamics for accurate closed-loop trajectory tracking fully exploiting the learned model predictions in a receding horizon fashion. Experimental results demonstrate that our approach accurately extracts the structure of the quadrotor's dynamics from data, capturing effects that would remain hidden to classical approaches. To the best of our knowledge, this is the first time physics-inspired deep learning is successfully applied to temporal convolutional networks and to the system identification task, while concurrently enabling predictive control.</p>
