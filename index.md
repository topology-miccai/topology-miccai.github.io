---
layout: default
---

<h1 style="text-align: center;">Overview</h1>

A segmentation algorithm, even with high per-pixel accuracy, could make errors on fine-scale structures, such as small instances, instances with multiple connected components, and thin connections. Such fine-scale structures may be crucial in analyzing the functionality of the objects. For example, small pixel-level errors disconnecting the segmentation of thin parts such as ropes and handles may lead to significant mistakes in the planning of robot actions, e.g., dragging or grasping. In biomedical imaging, the correct delineation of thin objects such as neuron membranes and vessels is crucial in providing accurate quantification of the underlying system. A broken connection or a missing component could cause catastrophic functional mistakes.

This tutorial aims to cover recent advances to solve the problem from the topology perspective. We will first discuss several interesting topology-aware loss functions, which help to learn to segment with correct topology for different kinds of images with fine-scale structures. Besides focusing on the topology of images with only one foreground class, we also introduce new losses to encode topological interactions among different classes (e.g., containment and exclusion). Furthermore, different from pixel-wise feature representations, we discuss direct modeling and reasoning about the structures by adopting probabilistic models. For each research sub-topic, we will give a concrete introduction of the contained problems/tasks, and the current research progress. We hope the audience, not only the graduate students but also the researchers new in this area, can benefit from this tutorial and learn the principle problems and cutting-edge approaches of topological analysis for biomedical images.

## Topology-preserving deep image segmentation
Image segmentation, i.e., assigning labels to all pixels of an input image, is crucial in many computer vision tasks. State-of-the-art deep segmentation methods learn high-quality feature representations through an end-to-end trained deep network and achieve satisfactory per-pixel accuracy. However, these segmentation algorithms are still prone to make errors on fine-scale structures, such as small object instances, instances with multiple connected components, and thin connections. These fine-scale structures may be crucial in analyzing the functionality of the objects. For example, accurate extraction of thin parts such as ropes and handles is crucial in planning robot actions, e.g., dragging or grasping. In biomedical images, correct delineation of thin objects such as neuron membranes and vessels is crucial in providing accurate morphological and structural quantification of the underlying system. A broken connection or a missing component may only induce marginal per-pixel error but can cause catastrophic functional mistakes.

## Learning topological interactions for multi-class medical image segmentation
Deep learning methods have achieved impressive performance for multi-class medical image segmentation. However, they are limited in their ability to encode topological interactions among different classes
(e.g., containment and exclusion). These constraints naturally arise in biomedical images and can be crucial in improving segmentation quality. In this paper, we introduce a novel topological interaction module to encode the topological interactions into a deep neural network. The implementation is completely convolution-based and thus can be very efficient. This empowers us to incorporate the constraints into end-to-end training and enrich the feature representation of neural networks.

## Learning probabilistic topological representations
Accurate delineation of fine-scale structures is a very important yet challenging problem. Existing methods use topological information as an additional training loss, but are ultimately making pixel-wise predictions. In this paper, we propose the first deep learning-based method to learn topological/structural representations. We use discrete Morse theory and persistent homology to construct a one-parameter family of structures as the topological/structural representation space. Furthermore, we learn a probabilistic model that can perform inference tasks in such a topological/structural representation space. Our method generates true structures rather than pixel maps, leading to better topological integrity in automatic segmentation tasks. It also facilitates semi-automatic interactive annotation/proofreading via the sampling of structures and structure-aware uncertainty.

* * *

<h1 style="text-align: center;">Schedule and material</h1>

Time zone: PDT

| Time |                           Topic                          | Slides | Presenter |
|:----:|:--------------------------------------------------------:|:------:|:---------:|
| TBD  |     Overview, motivation and theoretical foundations     |  TBD   |    TBD    |
| TBD  |     Topological analysis methodology I (segmentation)    |  TBD   |    TBD    |
| TBD  | Topological analysis methodology II (un/semi-supervised) |  TBD   |    TBD    |
| TBD  |                           Break                          |  TBD   |    TBD    |
| TBD  |               Graph learning with topology               |  TBD   |    TBD    |
| TBD  |                       Applications                       |  TBD   |    TBD    |


* * *

<h1 style="text-align: center;">Organizers</h1>

<table class="tg">
<tbody>
  <tr>
    <td class="tg-pb0m"><img src="/imgs/circle-cc.png" width="80%"></td>
    <td class="tg-pb0m"><img src="/imgs/circle-bm.png" width="80%"></td>
  </tr>
  <tr>
    <td class="tg-c3ow"><a href="https://chaochen.github.io/">Chao Chen</a></td>
    <td class="tg-c3ow"><a href="https://www.dqbm.uzh.ch/en/research/menze.html">Bjoern Menze</a></td>
  </tr>
  <tr>
    <td class="tg-pb0m"><img src="/imgs/circle-xh.png" width="80%"></td>
    <td class="tg-pb0m"><img src="/imgs/circle-sg.png" width="80%"></td>
  </tr>
  <tr>
    <td class="tg-c3ow"><a href="https://huxiaoling.github.io/">Xiaoling Hu</a></td>
    <td class="tg-c3ow"><a href="https://saumya-gupta-26.github.io/">Saumya Gupta</a></td>
  </tr>
</tbody>
</table>

