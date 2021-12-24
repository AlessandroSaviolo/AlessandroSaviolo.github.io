---
title: ""
permalink: /HumanBodySegmentation/
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

<p class="aligncenter"><a href="https://antonilo.github.io/">Antonio Loquercio</a>*, <a href="https://alessandrosaviolo.github.io/">Alessandro Saviolo</a>*, <a href="http://rpg.ifi.uzh.ch/people_scaramuzza.html">Davide Scaramuzza</a></p>

<p class="aligncenter"><a href="https://arxiv.org/abs/2103.10698">Paper</a> <a href="https://github.com/uzh-rpg/mh_autotune">Code</a> <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">Video</a></p>

<figure>
  <img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
  <figcaption>Figure 1. Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h. We automatically find a controller configuration that can fly such a high-speed maneuver with a novel sampling-based method called AutoTune. To get a better sense of the speed achieved by the quadrotor, please watch the <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">supplementary video</a>.</figcaption>
</figure>

<p class="description"><b>Abstract.</b> Due to noisy actuation and external disturbances, tuning controllers for high-speed flight is very challenging. In this paper, we ask the following questions: How sensitive are controllers to tuning when tracking high-speed maneuvers? What algorithms can we use to automatically tune them? To answer the first question, we study the relationship between parameters and performance and find out that the faster the maneuver, the more sensitive a controller becomes to its parameters. To answer the second question, we review existing methods for controller tuning and discover that prior works often perform poorly on the task of high-speed flight. Therefore, we propose AutoTune, a sampling-based tuning algorithm specifically tailored to high-speed flight. In contrast to previous work, our algorithm does not assume any prior knowledge of the drone or its optimization function and can deal with the multi-modal characteristics of the parameters' optimization space. We thoroughly evaluate AutoTune both in simulation and in the physical world. In our experiments, we outperform existing tuning algorithms by up to 90 % in trajectory completion. The resulting controllers are tested in the AirSim Game of Drones competition, where we outperform the winner by up to 25% in lap-time. Finally, we validate AutoTune in real-world flights in one of the world’s largest motion-capture systems. In these experiments, we outperform human experts on the task of parameter tuning for trajectory tracking, achieving flight speeds over 50 km/h.</p>

<figure>
  <img src="/images/autotune_2.gif" alt="Trajectory completion (%) as a function of two parameters of a model-predictive controller." style="width:100%">
  <figcaption>Figure 2. Trajectory completion (%) as a function of two parameters of a model-predictive controller. The trajectory completion measures the percentage of trajectory successfully tracked by the controller. The high speed and high angular accelerations required by time-optimal trajectories make the controller extremely sensitive to its parameters. Visualizations generated with the Loss Landscape Explorer App created by <a href="https://losslandscape.com/">Javier Ideami @ losslandscape.com</a>.</figcaption>
</figure>

## Introduction
