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
  <img src="/images/humanbodysegmentation_1.gif" alt="Human arm segmentation." style="width:100%">
  <figcaption>Figure 1. Human arm segmentation. The proposed method learns to extract human body parts in simulation and can be directly applied to the real world. The methodology is robust to changes in background and illumination conditions.</figcaption>
</figure>

<p class="description"><b>Abstract.</b> This paper presents a new framework for human body part segmentation based on Deep Convolutional Neural Networks trained using only synthetic data. The proposed approach achieves cutting-edge results without the need of training the models with real annotated data of human body parts. Our contributions include a data generation pipeline, that exploits a game engine for the creation of the synthetic data used for training the network, and a novel pre-processing module, that combines edge response maps and adaptive histogram equalization to guide the network to learn the shape of the human body parts ensuring robustness to changes in the illumination conditions. For selecting the best candidate architecture, we perform exhaustive tests on manually annotated images of real human body limbs. We further compare our method against several high-end commercial segmentation tools on the body parts segmentation task. The results show that our method outperforms the other models by a significant margin. Finally, we present an ablation study to validate our pre-processing module.</p>


## Introduction

<p class="description">The ability to extract human body parts from the foreground space of images is an essential requirement for many robotics and perception applications such as human-robot interaction, surgical robotics and medical images analysis, self-perception in mixed reality, and 3D human body reconstruction. A collaborative robot, for example, should be able to localize the arms of the human operator with whom it is collaborating, just as a surgical robot must be able to accurately locate the limb on which it is operating. In egocentric vision systems, hand position recognition is a key capability, for example, to detect which objects come into contact with it. 3D human body reconstruction systems must be able to distinguish which parts of the input images belong to the human body, and which parts must not be considered in the reconstruction.</p>

<p class="description">The body parts localization task can be addressed as a semantic segmentation problem. Semantic segmentation aims to provide a per-pixel classification of the input image. In the specific case of human body segmentation, there are two classes involved: pixels that belong to human limbs and those that do not. Semantic segmentation of naked human body parts can be obtained, for instance, by exploiting skin color detection and segmentation techniques. Unfortunately, such color-based systems suffer from severe robustness problems due to the variability of skin tone, the variability of light conditions, and the complexity of backgrounds, which can be mistaken for portions of the skin.</p>

<p class="description">Convolutional Neural Networks (CNNs) are convenient and effective methods for addressing the general problem of semantic segmentation. Multiple powerful networks have been proposed to obtain superior segmentation results. Unfortunately, these segmentation techniques require thousands of annotated images to be properly trained. Manually labeling the entire dataset is challenging and extremely time-consuming. Furthermore, the quality of the segmentation result in the case of human body parts obtained by most CNN-based systems is fair but certainly not adequate for many of the applications listed above. Background removal systems can be used for body part localization as well: unfortunately, such systems either require a rich prior knowledge about the scene to build an accurate background model or are too general and struggle to adapt to specific tasks. Other techniques, such as background subtraction in a green screen setting, allow to speed up the annotation process. However, they may come at the cost of the unrealistic feature of green color bleeding at the annotation boundaries.</p>

<figure>
  <img src="/images/humanbodysegmentation_2.png" alt="The proposed shape-aware segmentation framework." style="width:100%">
  <figcaption>Figure 2. The proposed shape-aware segmentation framework.</figcaption>
</figure>

<p class="description"><b>Contributions.</b> This paper proposes a new framework for body part segmentation that aims to overcome the limitations listed above. The proposed framework has been specifically trained to obtain highly accurate segmentation masks from images of naked human limbs without the need for any real data annotation since it only relies on synthetically generated data and a custom pre-processing of the network's input. Our system is based on a pipeline that includes a state-of-the-art semantic segmentation architecture and a custom pre-processing module that feeds the segmentation network with a specific input tensor built by concatenating the edge response map and two equalized versions of the original input image. The pre-processing module is designed to polarize the network to focus on the shape of the objects of interest (human limbs in our case) rather than the skin tone (intensity or color) or its characteristic texture. This simple modification greatly increases the level of segmentation accuracy compared to the same network fed with raw input images. Moreover, to emphasize skin tone independence, we performed all the experiments considering gray-level images. Our system also does not require any manually annotated data for training. The data are automatically generated by rendering, with a game engine, synthetic photo-realistic views of human limbs: such images are provided with ground truth segmentation masks (i.e., the annotations) at no additional cost. The geometric properties of human limbs (e.g., scale, deformation) and the scene configuration (e.g., illumination, camera positions) are defined by a set of parameters. By randomly choosing a combination of these parameters within predefined ranges, our data generation pipeline can generate multiple unique synthetic images and their corresponding annotations. We report an exhaustive performance evaluation, focusing on the arm segmentation use case. Experiments have been performed on a custom-built, manually labeled dataset that includes several views of real human arms. Our experiments aim both to validate the architectural choices and to show that our system overcomes by a large margin several state-of-the-art segmentation architectures in the specific human limb segmentation task. Furthermore, we compare our method against several cutting-edge commercial foreground segmentation networks on the body parts segmentation task, and demonstrate that the considered networks are too generic to produce accurate segmentation results.</p>



















