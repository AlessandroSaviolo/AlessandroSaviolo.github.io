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
p.aboutme {
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

<p class="aboutme">I am currently pursuing my Ph.D. at the <a href="https://wp.nyu.edu/arpl/">Agile Robotics and Perception Lab (ARPL)</a> at New York University, under the esteemed guidance of <a href="https://engineering.nyu.edu/faculty/giuseppe-loianno">Prof. Giuseppe Loianno</a>. 
I hold a Bachelor's and Master's degree in Computer Engineering from the University of Padova. During my Master's program, I had the enriching experience of spending a semester at National Chao Tung University in Taiwan. Furthermore, I was honored to receive a scholarship through the Swiss European Mobility Programme, which allowed me to engage in a six-month research project at the Robotics and Perception Group in Zurich. Following the completion of my Master's degree, I spent nine months as a full-time software engineer at Flexsight, a cutting-edge start-up specializing in artificial vision and autonomous perception solutions.</p>

## Research

### Dynamics learning
<figure>
<img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
<figcaption>Figure 1. Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h. We automatically find a controller configuration that can fly such a high-speed maneuver with a novel sampling-based method called AutoTune. To get a better sense of the speed achieved by the quadrotor, please watch the <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">supplementary video</a>.</figcaption>
</figure>

Model-based control requires an accurate model of the system dynamics for precisely and safely controlling the robot in complex and dynamic environments. Moreover, in the presence of variations in the operating conditions, the model should be continuously refined to compensate for dynamics changes. In this research, we present a self-supervised learning approach that actively models the dynamics of nonlinear robotic systems. We combine offline learning from past experience and online learning from current robot interaction with the unknown environment. These two ingredients enable a highly sample-efficient and adaptive learning process, capable of accurately inferring model dynamics in real-time even in operating regimes that greatly differ from the training distribution. Moreover, we design an uncertainty-aware model predictive controller that is heuristically conditioned to the aleatoric (data) uncertainty of the learned dynamics. This controller actively chooses the optimal control actions that (i) optimize the control performance and (ii) improve the efficiency of online learning sample collection. We demonstrate the effectiveness of our method through a series of challenging real-world experiments using a quadrotor system. Our approach showcases high resilience and generalization capabilities by consistently adapting to unseen flight conditions, while it significantly outperforms classical and adaptive control baselines.

### Visual tracking


### Perpetual autonomy


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
