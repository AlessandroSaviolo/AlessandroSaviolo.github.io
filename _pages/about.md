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
My research focuses on enabling quadrotors to fly fast, safely, and reliably in environments that are unknown, cluttered, and unstructured.  
The central theme of my dissertation is that three common assumptions in aerial robotics—fixed dynamics models, map-based planning, and reliance on global position—break down in practice. My work explicitly challenges these assumptions and proposes scalable, real-time alternatives that work in the wild.</p>

## Breaking Three Assumptions

### **Dynamics are fixed and known**
<img src="/images/dynamics_learning.gif" alt="Adaptive dynamics learning in flight" style="width:100%">
<p>Traditional control pipelines assume the robot’s dynamics can be modeled once offline and then trusted during operation. In reality, factors such as unmodeled aerodynamics, wind gusts, payload changes, and even minor damage can quickly invalidate these models.  
I developed a hybrid physics–informed neural network with <b>online adaptation</b>, which continuously refines the model in real time. This feeds into an uncertainty-aware NMPC that accounts for model confidence. The result is agile, stable flight even as conditions evolve, without the need for re-tuning or human intervention.</p>

### **Maps are complete and reliable**
<img src="/images/reactive_collision_avoidance.gif" alt="Reactive avoidance without mapping" style="width:100%">
<p>Most autonomy frameworks build a map first and then plan within it. While effective in structured spaces, this approach is too slow and brittle in dense forests, narrow passages, or dynamic settings.  
I proposed a perception–control loop that bypasses mapping entirely. By completing sparse depth in real time and embedding <b>control barrier functions</b> within an NMPC, the system reacts to collision risks at millisecond timescales. This enables split-second maneuvers and safe navigation where conventional pipelines fail, proving that high-speed flight without explicit mapping is not only possible but more robust.</p>

### **Global positioning is always available**
<img src="/images/visual_tracking.gif" alt="Tracking and navigation without global position" style="width:100%">
<p>Navigation is often framed around global references: GPS, motion capture, or high-quality VIO/SLAM. But outdoors under tree cover, indoors without infrastructure, or in adversarial conditions, these signals are unreliable or unavailable.  
I introduced a <b>local-frame instantaneous relative navigation</b> method that discards global horizontal position and absolute yaw entirely. The quadrotor navigates and tracks using only relative perception and onboard inertial sensing, enabling reliable pursuit and coordination even when global positioning fails.</p>

## Broader Vision
<p>Together, these three threads converge toward a new paradigm for **aerial autonomy at the edge of feasibility**: adaptive (dynamics learned and refined online), reactive (decisions made without explicit maps), and relative (navigation independent of global references).  
This framework has been validated across forest trails, urban mazes, container compounds, and military-grade test sites, advancing both the scientific foundation and the operational deployment of agile aerial robots. Applications include high-speed search and rescue, persistent surveillance, and resilient human–robot teaming in the field.</p>

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
