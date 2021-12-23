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
p.links {
  text-align: center;
}
</style>
</head>

<p class="title">AutoTune: Controller Tuning for High-Speed Flight</p>

<p class="authors">Antonio Loquercio*, Alessandro Saviolo*, Davide Scaramuzza</p>

<img src="/images/autotune_1.jpeg" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h.">

<p class="description">Due to noisy actuation and external disturbances, tuning controllers for high-speed flight is very challenging. In this paper, we ask the following questions: How sensitive are controllers to tuning when tracking high-speed maneuvers? What algorithms can we use to automatically tune them? To answer the first question, we study the relationship between parameters and performance and find out that the faster the maneuver, the more sensitive a controller becomes to its parameters. To answer the second question, we review existing methods for controller tuning and discover that prior works often perform poorly on the task of high-speed flight. Therefore, we propose AutoTune, a sampling-based tuning algorithm specifically tailored to high-speed flight. In contrast to previous work, our algorithm does not assume any prior knowledge of the drone or its optimization function and can deal with the multi-modal characteristics of the parameters' optimization space. We thoroughly evaluate AutoTune both in simulation and in the physical world. In our experiments, we outperform existing tuning algorithms by up to 90% in trajectory completion. The resulting controllers are tested in the AirSim Game of Drones competition, where we outperform the winner by up to 25% in lap-time. Finally, we validate AutoTune in real-world flights in one of the world’s largest motion-capture systems. In these experiments, we outperform human experts on the task of parameter tuning for trajectory tracking, achieving flight speeds over 50 km/h.</p>

<p class="links"><a href="https://arxiv.org/abs/2103.10698">Paper</a> <a href="https://github.com/uzh-rpg/mh_autotune">Code</a> <a href="https://www.youtube.com/watch?v=m2q_y7C01So&ab_channel=UZHRoboticsandPerceptionGroup">Video</a></p>

## Introduction

Flying high-speed trajectories with a quadrotor requires the platform's controller to be meticulously tuned. The complex relationship between parameters and performance is caused by unavoidable factors such as noisy actuation, imperfect modeling, and external disturbances. The higher the speed, the more complex the relationship between controller parameters and final performance is. This behaviour is empirically shown by the figure below.

<div class="row">
  <div class="column">
    <img src="/images/autotune_2.png" alt="Trajectory completion (%) as a function of two parameters of a model-predictive controller." style="width:100%">
  </div>
  <div class="column">
    <img src="/images/autotune_3.png" alt="Trajectory completion (%) as a function of two parameters of a model-predictive controller." style="width:100%">
  </div>
</div>

The figure illustrates the trajectory completion (%) as a function of two parameters of a model-predictive controller, where the trajectory completion measures the percentage of trajectory successfully tracked by the controller. The high speed and high angular accelerations required by time-optimal trajectories make the controller extremely sensitive to its parameters.

## Challenges

<ul style="list-style-type:square">

<li>The objective function (i.e. the relationship between controller parameters and performance) is highly non-convex;</li>
<li>The tuning process only relies on noisy evaluations of the objective function at adaptively chosen parameters, but not to the function itself or its gradients;</li>
<li>Different parts of the trajectory, e.g. a sharp turn or a straight-line acceleration, generally require different controller behaviors, hence dynamically changing parameters.</li>

</ul>

## Related Work

The traditional approach for automatic tuning and adaptive control, generally known as MIT rule, requires to express the desired performance metric, e.g. the average tracking error over the entire maneuver, as a quadratic function of controller parameters, and then optimizes the controller with gradient-based optimization. However, expressing the long-term performance on a high-speed maneuver with respect to the parameters of a receding horizon controller is generally intractable. Indeed, it requires to know a priori the exact model of the quadrotor and the disturbances acting on it during flight, e.g. noisy actuation and aerodynamic effects. Instead of analytically computing it, another line of work proposes to iteratively estimate the optimization function, and use the estimate to find optimal parameters. However, these methods make over-simplifying assumptions on the objective function, e.g. convexity or relative Gaussianity between observations. Such assumptions are generally not suited for controller tuning to high-speed flight, where the function is highly non-convex. To remove any assumption, model-free methods propose to directly search for optimal parameters using sampling. Such methods are however built on heuristics not necessarily suited to high-speed flight and generally require thousands of iterations to converge.

## Contribution

In this paper, we propose a novel sampling-based algorithm specifically tailored to the problem of high-speed flight, rooted in statistical theory: AutoTune. Given an initial, low-performance controller, AutoTune optimizes its parameters to maximize a user-defined metric, e.g. track completion. In contrast to traditional adaptive control, e.g. the MIT rule, it does not require to analytically express the optimization function with respect to the controller parameters, nor assumptions about the optimization function. Similarly to model-free sampling-based methods, AutoTune does neither require prior knowledge of the platform model and external disturbances. However, to make sampling computationally tractable, our approach uses Metropolis-Hastings sampling (M-H) and several strategies specifically tailored to the problem of high-speed flight. Specifically, motivated by the observation that different parts of a trajectory require different controller behaviors, we propose a strategy to break down a trajectory into components with different behaviors, e.g. sharp descent or planar acceleration. Despite controller parameters being different for each component, they are all optimized jointly to favor optimality over the entire trajectory. In addition, to speed up convergence, we train a regressor to predict good initialization parameters.
















