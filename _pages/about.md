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
<p>
I am a Ph.D. candidate in Electrical and Computer Engineering at New York University (NYU), where I work in the Agile Robotics and Perception Lab (ARPL). I am passionate about building autonomous systems that operate safely and reliably in the real world. My work focuses on perception and optimal control for high-speed navigation in complex, GPS-denied environments, with an emphasis on rapid adaptation and robust generalization across diverse conditions. Before starting my PhD, I studied computer engineering in Padova with research experiences in Taiwan and Switzerland, and worked as a research engineer at FlexSight on autonomous navigation for agricultural and medical robots. My research has been validated through DARPA and Army Research Lab field trials, published in leading IEEE venues, and resulted in multiple journal articles and U.S. patents.
</p>

# Research
<p>
  Autonomous drones are becoming indispensable in critical missions such as search and rescue and disaster response. Yet today’s systems still require expert human pilots because autonomy fails where it matters most: in complex, GPS-denied, and rapidly changing environments. GPS signals vanish, maps become outdated, and controllers tuned in the lab collapse when conditions shift. During my PhD, I rebuilt the autonomy stack around a simple premise: 
  <i>
  enable safe and agile flight by removing assumptions about operating conditions, environment maps, and external infrastructure, and instead grounding navigation in adaptation, reactivity, and direct onboard sensing.
  </i>
</p>

<div style="display:flex; align-items:center; gap:20px; margin:40px 0;">
  <div style="flex:1;">
    <video autoplay loop muted playsinline style="width:100%; max-width:400px; height:auto;">
      <source src="/images/dynamics_learning.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  <div style="flex:2;">
    <p><b>Adaptive dynamics and control</b>.
    Quadrotor dynamics change continuously with wind, payload variations, and hardware wear. These effects are difficult to capture with traditional physics-based models that assume fixed and known conditions. The first step in my research was to remove this assumption and design a system that learns and adapts its dynamics online. I developed a physics-informed model that corrects itself in real time from prediction errors, allowing the controller to remain accurate as conditions evolve. To further accelerate learning, I introduced an uncertainty-aware strategy that guides the controller toward regions of the state space that are most informative, producing more stable gradients and faster adaptation. As a result, the vehicle can stabilize within seconds, even when carrying a 30% heavier payload, flying with swapped propellers, or facing strong gusts of wind.
    </p>
  </div>
</div>

<div style="display:flex; align-items:center; gap:20px; margin:40px 0;">
  <div style="flex:2;">
    <p><b>Reactive collision avoidance</b>. 
    Accurate dynamics provide the foundation for stable flight, but they are not enough to guarantee safety when maps quickly become outdated. In cluttered and rapidly changing environments, a map can be obsolete the moment it is built, leaving the vehicle exposed to collisions. To address this, I replaced the conventional map–plan–track pipeline with a reactive collision-avoidance strategy that enforces safety directly from perception. Raw stereo depth is densified with monocular depth estimation and scale alignment to recover reliable geometry. From this, the system computes time-to-collision and extracts only the most critical points, which are injected as control barrier function constraints into the controller. Updated at every perception cycle, these constraints allow the quadrotor to react instantly to obstacles while maintaining real-time performance.
    </p>
  </div>
  <div style="flex:1;">
    <video autoplay loop muted playsinline style="width:100%; max-width:400px; height:auto;">
      <source src="/images/reactive_collision_avoidance.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<div style="display:flex; align-items:center; gap:20px; margin:40px 0;">
  <div style="flex:1;">
    <video autoplay loop muted playsinline style="width:100%; max-width:400px; height:auto;">
      <source src="/images/visual_tracking.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  <div style="flex:2;">
    <p><b>Instantaneous relative navigation</b>. 
    Even with adaptation and reactivity, any autonomy stack ultimately fails if localization drifts. In GPS-denied flight, global horizontal position and yaw are unobservable, which causes objectives defined in a world frame to collapse over time. My solution was to abandon the global frame altogether and introduce instantaneous relative navigation. Instead of relying on absolute position, the vehicle fixes its frame to gravity, and plans only from directly observable quantities such as attitude, altitude, velocity, and objects in view. In search mode, this allows the quadrotor to traverse unknown environments without accumulating drift. Once a target is detected, the frame is anchored to it, and the system transitions seamlessly into pursuit. In large-scale field trials, the vehicle tracked ground targets at more than 90 km/h and 60° pitch angles, consistently reacquiring them even under intermittent detections and degraded sensing.
    </p>
  </div>
</div>

<p>
Together, these advances form an autonomy stack that is adaptive, reactive, and relative. By continuously updating its dynamics, guaranteeing safety directly from perception, and navigating without reliance on global references, the system achieves reliable high-speed flight in environments where traditional pipelines fail. Validated on embedded compute in forests and urban compounds, my PhD research demonstrates that safe and agile autonomy is not just possible in controlled settings but deployable in the real world.
</p>

## Latest News
<p class="aboutme">
<ul style="list-style-type:square">
  <li><b>May, 2025</b>. Will present in person at ICRA 2025 conference in Atlanta ✈️</li>
  <li><b>Jan, 2025</b>. <a href="https://arxiv.org/abs/2409.11962">Paper article</a> accepted at ICRA 2025 🦾</li>
  <li><b>Jan, 2025</b>. <a href="https://arxiv.org/abs/2409.17379">Paper article</a> accepted at ICRA 2025 🦾</li>
  <li><b>May, 2024</b>. Will present in person at ICRA 2024 conference in Yokohama ✈️</li>
  <li><b>Jan, 2024</b>. <a href="https://arxiv.org/abs/2310.04781">Paper article</a> accepted at ICRA 2024 🦾</li>
  <li><b>Nov, 2023</b>. <a href="https://arxiv.org/abs/2210.12583">Journal article</a> accepted at Transactions on Robotics 2023 🦾</li>
  <li><b>Oct, 2023</b>. <a href="https://arxiv.org/abs/2310.04781">Paper article</a> featured on <a href="https://spectrum.ieee.org/video-friday-strandbeest-2">IEEE Spectrum</a> 📺</li>
  <li><b>Oct, 2023</b>. <a href="https://alessandrosaviolo.github.io/">Paper article</a> accepted at ICAR 2023 🦾</li>
  <li><b>Jun, 2023</b>. <a href="https://arxiv.org/abs/2306.05111">AutoCharge</a> featured on <a href="https://spectrum.ieee.org/video-friday-spot-levels-up">IEEE Spectrum</a> 📺</li>
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
