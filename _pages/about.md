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
I am a Senior Autonomy Engineer at Plus, where I work on advanced perception and control systems for autonomous long-haul trucks. I recently completed my Ph.D. in Electrical and Computer Engineering at New York University, where I conducted research in the Agile Robotics and Perception Lab (ARPL). My work focuses on building autonomous systems that operate safely and reliably in the real world, with an emphasis on perception and optimal control for high-speed navigation in complex, GPS-denied environments. Before my Ph.D., I studied computer engineering in Padova with research experiences in Taiwan and Switzerland, and worked as a research engineer at FlexSight, developing navigation systems for agricultural and medical robots. My research has been validated through DARPA and Army Research Lab field trials, published in leading IEEE venues, and resulted in multiple journal articles and U.S. patents.
</p>

## Ph.D. Research
<p>
  Autonomous drones are becoming indispensable in critical missions such as search and rescue and disaster response. Yet today’s systems still require expert human pilots because autonomy fails where it matters most: in complex, GPS-denied, and rapidly changing environments. GPS signals vanish, maps become outdated, and controllers tuned in the lab collapse when conditions shift. During my Ph.D., I rebuilt the autonomy stack around a simple premise: 
</p>
<div style="text-align:center; margin:20px 0;">
  <i>
    Enabling safe and agile autonomy in unknown environments by adapting to shifting conditions, reacting instantly to obstacles, and relying only on what the robot can directly observe.
  </i>
</div>

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
<ul class="aboutme" style="list-style-type:square">
  <li><b>Jan 2026</b> — Paper accepted at ICRA 2026  
      (<a href="https://arxiv.org/pdf/2509.19452">arXiv</a>) 🦾</li>
  <li><b>Nov 2025</b> — Journal paper accepted at Transactions on Field Robotics  
      (<a href="https://arxiv.org/pdf/2506.18689">arXiv</a>) 🦾</li>
  <li><b>Oct 2025</b> — Joined <a href="https://plus.ai/">PlusAI</a></li>
  <li><b>Oct 2025</b> — PhD defense: <i>Adaptive and Reactive Visual Autonomy for Safe Agile Flight in Unstructured Environments</i></li>
  <li><b>May 2025</b> — Oral presentation at ICRA 2025 (Atlanta, USA) ✈️</li>
  <li><b>Jan 2025</b> — Paper accepted at ICRA 2025  
      (<a href="https://arxiv.org/abs/2409.11962">arXiv</a>) 🦾</li>
  <li><b>Jan 2025</b> — Paper accepted at ICRA 2025  
      (<a href="https://arxiv.org/abs/2409.17379">arXiv</a>) 🦾</li>
  <li><b>May 2024</b> — Oral presentation at ICRA 2024 (Yokohama, Japan) ✈️</li>
  <li><b>Jan 2024</b> — Paper accepted at ICRA 2024  
      (<a href="https://arxiv.org/abs/2310.04781">arXiv</a>) 🦾</li>
  <li><b>Nov 2023</b> — Journal paper accepted at Transactions on Robotics  
      (<a href="https://arxiv.org/abs/2210.12583">arXiv</a>) 🦾</li>
  <li><b>Oct 2023</b> — Paper featured on  
      <a href="https://spectrum.ieee.org/video-friday-strandbeest-2">IEEE Spectrum</a> 📺</li>
  <li><b>Oct 2023</b> — Paper accepted at ICAR 2023 🦾</li>
  <li><b>Jun 2023</b> — AutoCharge featured on  
      <a href="https://spectrum.ieee.org/video-friday-spot-levels-up">IEEE Spectrum</a> 📺</li>
  <li><b>May 2023</b> — Oral presentation at ICRA 2023 (London, UK) ✈️</li>
  <li><b>May 2023</b> — Recipient of the Dr. Li Annual ECE Publication Award 🏆</li>
  <li><b>Mar 2023</b> — Journal paper accepted at Annual Reviews in Control  
      (<a href="https://www.sciencedirect.com/science/article/pii/S1367578823000135">link</a>) 🦾</li>
  <li><b>Jan 2023</b> — AutoCharge and GaPT accepted at ICRA 2023 🦾🦾</li>
  <li><b>Oct 2022</b> — Virtual presentation at IROS 2022 📺</li>
  <li><b>Jun 2022</b> — PI-TCN accepted at RAL + IROS 2022 🦾</li>
  <li><b>May 2022</b> — Oral presentation at ICRA 2022 (Philadelphia, USA) ✈️</li>
  <li><b>Jan 2022</b> — AutoTune accepted at RAL + ICRA 2022 🦾</li>
  <li><b>Aug 2021</b> — Joined Agile Robotics and Perception Lab</li>
</ul>
