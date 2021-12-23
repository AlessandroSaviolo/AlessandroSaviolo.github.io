---
title: ""
permalink: /Autotune/
author_profile: true
---

<head>
<style>
p.title {
  text-align: center;
  font-weight: bold;
  font-size: 30px;
}
p.authors {
  text-align: center;
}
p.description {
  text-align: justify;
}
</style>
</head>

<p class="title">AutoTune: Controller Tuning for High-Speed Flight</p>

<p class="authors">Antonio Loquercio*, Alessandro Saviolo*, Davide Scaramuzza</p>

<p class="description">Due to noisy actuation and external disturbances, tuning controllers for high-speed flight is very challenging. In this paper, we ask the following questions: How sensitive are controllers to tuning when tracking high-speed maneuvers? What algorithms can we use to automatically tune them? To answer the first question, we study the relationship between parameters and performance and find out that the faster the maneuver, the more sensitive a controller becomes to its parameters. To answer the second question, we review existing methods for controller tuning and discover that prior works often perform poorly on the task of high-speed flight. Therefore, we propose AutoTune, a sampling-based tuning algorithm specifically tailored to high-speed flight. In contrast to previous work, our algorithm does not assume any prior knowledge of the drone or its optimization function and can deal with the multi-modal characteristics of the parameters' optimization space. We thoroughly evaluate AutoTune both in simulation and in the physical world. In our experiments, we outperform existing tuning algorithms by up to 90% in trajectory completion. The resulting controllers are tested in the AirSim Game of Drones competition, where we outperform the winner by up to 25% in lap-time. Finally, we validate AutoTune in real-world flights in one of the world’s largest motion-capture systems. In these experiments, we outperform human experts on the task of parameter tuning for trajectory tracking, achieving flight speeds over 50 km/h.</p>
  


## Pre-Prints

<ul style="list-style-type:square">

<li>
<div class="title">AutoTune: Controller Tuning for High-Speed Flight</div>
<div class="description">A. Loquercio*, <u>A. Saviolo*</u>, D. Scaramuzza</div>
<div class="description"><a href="https://arxiv.org/abs/2103.10698">Project Page</a></div>

<div class="description"><a href="https://arxiv.org/abs/2103.10698">Paper</a> <a href="https://github.com/uzh-rpg/mh_autotune">Code</a> <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">Video</a></div>
</li>

</ul>
