---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<head>
<style>
p {
  text-align: justify;
}
div.title {
  text-align: left;
  font-weight: bold;
}
div.description {
  text-align: left;
  opacity: 0.8;
}
@counter-style repeating-emoji {
  system: cyclic;
  symbols: "\1F431" "\1F436" "\1F984"; // unicode code point
  suffix: " ";
}
.repeating-counter-rule {
  list-style-type: repeating-emoji;
}
</style>
</head>

# Welcome!
<p>I am a Ph.D. candidate at the <a href="https://wp.nyu.edu/arpl/">Agile Robotics and Perception Lab</a> (ARPL), New York University, advised by Prof. <a href="https://engineering.nyu.edu/faculty/giuseppe-loianno">Giuseppe Loianno</a>.  
My research focuses on pushing autonomous quadrotors to operate at high speed in unknown, unstructured environments.  
The central theme of my dissertation, <i>Adaptive and Reactive Aerial Autonomy</i>, is that the assumptions underlying most autonomy stacks break down in the real world. My work challenges these assumptions and provides scalable alternatives that enable reliable autonomy in the wild.</p>

## Breaking Three Assumptions

### **Fixed Dynamics Models**
<img src="/images/dynamics_learning.gif" alt="Adaptive dynamics learning in flight" style="width:100%">
<p>Most controllers assume the system dynamics are fixed, identified offline, and valid everywhere.  
I show this assumption fails under varying aerodynamics, external disturbances, and damage.  
**Contribution:** A hybrid physics–informed neural network with online adaptation that continuously refines the dynamics model in real time, feeding an uncertainty-aware NMPC for robust performance.</p>

### **Maps Before Action**
<img src="/images/reactive_collision_avoidance.gif" alt="Reactive avoidance without mapping" style="width:100%">
<p>Conventional autonomy relies on explicit mapping before planning, which is too slow and brittle in cluttered or dynamic settings.  
**Contribution:** A perception–control pipeline that bypasses mapping, combining real-time depth completion with control barrier–function NMPC. This allows split-second reactive collision avoidance and safe flight without precomputed maps.</p>

### **Global Position is Necessary**
<img src="/images/visual_tracking.gif" alt="Tracking and navigation without global position" style="width:100%">
<p>Most navigation stacks assume access to global position (GPS, motion capture, or accurate SLAM). These signals are often unreliable or unavailable outdoors under occlusions or indoors without infrastructure.  
**Contribution:** A local-frame, instantaneous relative navigation method that discards global horizontal position and absolute yaw. The quadrotor navigates and tracks targets using only relative perception, inertial sensing, and onboard computation.</p>

## Broader Vision
<p>Together, these contributions form a new paradigm for **agile aerial autonomy**: adaptive, reactive, and relative.  
This work has been validated in forest trails, urban mazes, and military-grade test sites, advancing both the scientific understanding of autonomous flight and its deployment in real-world applications such as search and rescue, surveillance, and human–robot teaming.</p>

## Latest News
## Latest News
<p class="aboutme">
<ul style="list-style-type:square">
  <li><b>May, 2025</b>. Will present in person at ICRA 2025 conference in Atlanta ✈️</li>
  <li><b>Jan, 2025</b>. <a href="https://arxiv.org/abs/2409.11962">Paper article</a> accepted at ICRA 2025 🦾</li>
  <li><b>Jan, 2025</b>. <a href="https://arxiv.org/abs/2409.17379">Paper article</a> accepted at ICRA 2025 🦾</li>
  <li><b>May, 2024</b>. Will present in person at ICRA Agile Robotics workshop ✈️</li>
  <li><b>May, 2024</b>. Will present in person at ICRA Aerial Robotics workshop ✈️</li>
  <li><b>May, 2024</b>. Will present in person at ICRA 2024 conference in Yokohama ✈️</li>
  <li><b>Jan, 2024</b>. <a href="https://arxiv.org/abs/2310.04781">Paper article</a> accepted at ICRA 2024 🦾</li>
  <li><b>Nov, 2023</b>. <a href="https://arxiv.org/abs/2210.12583">Journal article</a> accepted at Transactions on Robotics 2023 🦾</li>
  <li><b>Oct, 2023</b>. <a href="https://arxiv.org/abs/2310.04781">Paper article</a> featured on <a href="https://spectrum.ieee.org/video-friday-strandbeest-2">IEEE Spectrum</a> 📺</li>
  <li><b>Oct, 2023</b>. <a href="https://alessandrosaviolo.github.io/">Paper article</a> accepted at ICAR 2023 🦾</li>
  <li><b>Jun, 2023</b>. <a href="https://arxiv.org/abs/2306.05111">AutoCharge</a> featured on <a href="https://spectrum.ieee.org/video-friday-spot-levels-up">IEEE Spectrum</a> 📺</li>
  <li><b>May, 2023</b>. Will present in person at ICRA Energy Efficient Aerial Robotics workshop ✈️</li>
  <li><b>May, 2023</b>. Will present in person at ICRA 2023 conference in London ✈️</li>
  <li><b>May, 2023</b>. Honored to have been awarded the Dr. Li Annual ECE Publication Award 🏆</li>
  <li><b>Mar, 2023</b>. <a href="https://www.sciencedirect.com/science/article/pii/S1367578823000135">Journal article</a> accepted at Annual Reviews in Control 2023 🦾</li>
  <li><b>Jan, 2023</b>. <a href="https://arxiv.org/abs/2306.05111">AutoCharge</a> and <a href="https://arxiv.org/abs/2303.08181">GaPT</a> accepted at ICRA 2023 conference 🦾🦾</li>
  <li><b>Oct, 2022</b>. Will present virtually at IROS 2022 conference 📺</li>
  <li><b>Jun, 2022</b>. <a href="https://alessandrosaviolo.github.io/PI-TCN/">PI-TCN</a> accepted at RAL+IROS 2022 🦾</li>
  <li><b>May, 2022</b>. Will present in person at ICRA 2022 conference in Philadelphia ✈️</li>
  <li><b>Jan, 2022</b>. <a href="https://alessandrosaviolo.github.io/Autotune/">AutoTune</a> accepted at RAL+ICRA 2022 🦾</li>
  <li><b>Aug, 2021</b>. Joined Agile Robotics and Perception Lab 👨‍🎓</li>  
</ul>
</p>
