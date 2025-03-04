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

<p>I am currently pursuing my Ph.D. at the <a href="https://wp.nyu.edu/arpl/">Agile Robotics and Perception Lab</a> (ARPL) at New York University, under the guidance of Prof. <a href="https://engineering.nyu.edu/faculty/giuseppe-loianno">Giuseppe Loianno</a>. 
My research focuses on developing adaptive control systems for autonomous robots, integrating deep learning with control theory to solve real-world challenges. I hold Bachelor's and Master's degrees in Computer Engineering from the University of Padova, with research experience at the Robotics and Perception Group in Zurich and industry experience as a software engineer at Flexsight.</p>

## Research
### Reactive Collision Avoidance
<img src="/images/reactive_collision_avoidance.gif" alt="Quadrotor navigating through obstacles using real-time reactive collision avoidance framework" style="width:100%">
<p>In dynamic environments, real-time collision avoidance is essential for safe robot navigation. Our framework integrates perception, planning, and control, using monocular depth estimation (MDE) to refine noisy RGB-D data in real-time. With nonlinear model predictive control (NMPC) and adaptive control barrier functions (CBFs), the system reacts to high-risk collision points in milliseconds, enabling agile navigation without prior tuning. Extensive tests show its ability to generalize across unknown environments, ensuring safe, real-time flight.</p>

### Dynamics Learning
<img src="/images/dynamics_learning.gif" alt="By combining online learning with uncertainty-aware model predictive control, the learned dynamics actively adapt to multiple challenging operating conditions, enabling unprecedented flight control." style="width:100%">
<p>Model-based control needs an accurate system dynamics model to safely and precisely control robots in complex environments. This model should adapt to changing conditions. Our research introduces a self-supervised learning method that actively models nonlinear robotic systems' dynamics. We combine offline learning from past data and online learning from current interactions, making the process highly sample-efficient and adaptive. We also design an uncertainty-aware model predictive controller that considers data uncertainty to choose optimal control actions, improving both performance and learning efficiency.</p>

### Visual Tracking
<img src="/images/visual_tracking.gif" alt="Demonstrating our system's ability to detect, track, and navigate toward a running moving target in challenging outdoor environments." style="width:100%">
<p>Visual control allows quadrotors to navigate using real-time sensory data, but challenges like generalization, reliability, and real-time response remain. Our research addresses these issues with a new perception framework using foundation models for universal object detection and tracking. This framework, combined with a multi-layered tracker, ensures continuous target visibility despite motion blur, light changes, and occlusions. We also introduce a model-free visual controller for resilient tracking. Our system works efficiently with limited hardware, using only an onboard camera and an inertial measurement unit.</p>

### Perpetual Autonomy
<img src="/images/perpetual_autonomy.gif" alt="AutoCharge, an autonomous charging system for quadrotors that is capable of universal, highly efficient, and robust charging." style="width:100%">
<p>Battery endurance is a major challenge for long-term autonomy and long-range aerial robot operations. Our solution, AutoCharge, addresses this with an autonomous charging system for quadrotors. AutoCharge combines a portable ground station with a lightweight, flexible charging tether for universal, efficient, and robust charging. We designed circular magnetic connectors for precise, orientation-agnostic connections between the ground station and tether. An electromagnet on the ground station increases tolerance to localization and control errors during docking, ensuring smooth undocking after charging.</p>

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
