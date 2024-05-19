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

<p>I am currently pursuing my Ph.D. at the <a href="https://wp.nyu.edu/arpl/">Agile Robotics and Perception Lab</a> (ARPL) at New York University, under the esteemed guidance of Prof. <a href="https://engineering.nyu.edu/faculty/giuseppe-loianno">Giuseppe Loianno</a>. 
I hold a Bachelor's and Master's degree in Computer Engineering from the University of Padova. During my Master's program, I had the enriching experience of spending a semester at National Chao Tung University in Taiwan. Furthermore, I was honored to receive a scholarship through the Swiss European Mobility Programme, which allowed me to engage in a six-month research project at the Robotics and Perception Group in Zurich. Following the completion of my Master's degree, I spent nine months as a full-time software engineer at Flexsight, a cutting-edge start-up specializing in artificial vision and autonomous perception solutions.</p>

## Research

### Dynamics learning
<img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
<p>Model-based control needs an accurate system dynamics model to safely and precisely control robots in complex environments. This model should adapt to changing conditions. Our research introduces a self-supervised learning method that actively models nonlinear robotic systems' dynamics. We combine offline learning from past data and online learning from current interactions, making the process highly sample-efficient and adaptive. We also design an uncertainty-aware model predictive controller that considers data uncertainty to choose optimal control actions, improving both performance and learning efficiency.</p>

### Visual tracking
<img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
<p>Visual control allows quadrotors to navigate using real-time sensory data, but challenges like generalization, reliability, and real-time response remain. Our research addresses these issues with a new perception framework using foundation models for universal object detection and tracking. This framework, combined with a multi-layered tracker, ensures continuous target visibility despite motion blur, light changes, and occlusions. We also introduce a model-free visual controller for resilient tracking. Our system works efficiently with limited hardware, using only an onboard camera and an inertial measurement unit.</p>

### Perpetual autonomy
<img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
<p>Battery endurance is a major challenge for long-term autonomy and long-range aerial robot operations. Our solution, AutoCharge, addresses this with an autonomous charging system for quadrotors. AutoCharge combines a portable ground station with a lightweight, flexible charging tether for universal, efficient, and robust charging. We designed circular magnetic connectors for precise, orientation-agnostic connections between the ground station and tether. An electromagnet on the ground station increases tolerance to localization and control errors during docking, ensuring smooth undocking after charging. We validated AutoCharge in a 10-hour continuous quadrotor flight experiment, demonstrating reliable and repeatable docking and undocking, enabling perpetual flight missions.</p>

## Latest News

<p class="aboutme">
<ul style="list-style-type:square">
  <li><b>May, 2024</b>. Will present in person at ICRA Agile Robotics workshop ✈️</li>
  <li><b>May, 2024</b>. Will present in person at ICRA Aerial Robotics workshop ✈️</li>
  <li><b>May, 2024</b>. Will present in person at ICRA 2024 conference in Yokohama ✈️</li>
  <li><b>Jan, 2024</b>. <a href="https://arxiv.org/abs/2310.04781">Paper article</a> accepted at ICRA 2024 🦾</li>
  <li><b>Nov, 2023</b>. <a href="https://arxiv.org/abs/2210.12583">Journal article</a> accepted at Transactions on Robotics 2023 🦾</li>
  <li><b>Oct, 2023</b>. <a href="https://arxiv.org/abs/2310.04781">Paper article</a> featured on <a href="https://spectrum.ieee.org/video-friday-strandbeest-2">IEEE Spectrum</a> 📺</li>
  <li><b>Oct, 2023</b>. <a href="https://alessandrosaviolo.github.io/">Paper article</a> accepted at ICAR 2023 🦾</li>
  <li><b>Jun, 2023</b>. <a href="https://arxiv.org/abs/2306.05111">AutoCharge</a> featured on <a href="https://spectrum.ieee.org/video-friday-spot-levels-up">IEEE Spectrum</a> 📺</li>
  <li><b>May, 2023</b>. Will present in person at ICRA Energy Efficient Aerial Robotic Systems workshop ✈️</li>
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
