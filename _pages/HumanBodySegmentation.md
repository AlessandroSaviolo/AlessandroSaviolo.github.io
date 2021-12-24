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

<p class="title">Learning to Segment Human Body Parts with Synthetically Trained Deep Convolutional Networks</p>

<p class="aligncenter">
<a href="https://alessandrosaviolo.github.io/">Alessandro Saviolo</a>, 
<a href="https://www.dei.unipd.it/persona/b483a1d44fdd99885ddc88730c4c7ffb">Matteo Bonotto</a>, 
<a href="https://scholar.google.com/citations?user=JF4C6kQAAAAJ&hl=en">Daniele Evangelista</a>,
<a href="https://scholar.google.it/citations?user=rhFQhAEAAAAJ&hl=it">Marco Imperoli</a>,

<a href="https://www.linkedin.com/in/jacopolazzaro/?originalSubdomain=it">Jacopo Lazzaro</a>, 
<a href="https://scholar.google.com/citations?user=Zd2MrfUAAAAJ&hl=en">Emanuele Menegatti</a>,
<a href="https://scholar.google.it/citations?user=-kX87sgAAAAJ&hl=en">Alberto Pretto</a>

<p class="aligncenter"><a href="https://arxiv.org/abs/2102.01460">Paper</a> <a href="https://github.com/AlessandroSaviolo/HBPSegmentation">Code</a>

<figure>
  <img src="/images/humanbodysegmentation_1.gif" alt="Our quadrotor flies a time-optimal trajectory with speeds over 50 km/h." style="width:100%">
  <figcaption>Figure 1. Human arm segmentation. The proposed method learns to extract human body parts in simulation and can be directly applied to the real world. The methodology is robust to changes in background and illumination conditions.</figcaption>
</figure>

<p class="description"><b>Abstract.</b> This paper presents a new framework for human body part segmentation based on Deep Convolutional Neural Networks trained using only synthetic data. The proposed approach achieves cutting-edge results without the need of training the models with real annotated data of human body parts. Our contributions include a data generation pipeline, that exploits a game engine for the creation of the synthetic data used for training the network, and a novel pre-processing module, that combines edge response maps and adaptive histogram equalization to guide the network to learn the shape of the human body parts ensuring robustness to changes in the illumination conditions. For selecting the best candidate architecture, we perform exhaustive tests on manually annotated images of real human body limbs. We further compare our method against several high-end commercial segmentation tools on the body parts segmentation task. The results show that our method outperforms the other models by a significant margin. Finally, we present an ablation study to validate our pre-processing module.</p>





