---
layout: default
---

<h1 style="text-align: center;">Schedule and material</h1>

**Date/Time**: Oct 12 Thursday 08:30 AM - 12:30 PM PDT

**Venue**: Vancouver Convention Center East Building Level 1 - Meeting Room 3

**Zoom**: [Link](https://us02web.zoom.us/j/89550470833?pwd=bzdFTlJNWUxWeDlyTlp1OGc4bDZrUT09) 

**Slides**: The slides are hosted [here](https://drive.google.com/drive/folders/1YypeRgtjy3Jc-fg7PY2Y5LsQPFzussk6?usp=sharing)

**Workshop**: [The First Workshop on Topology- and Graph-Informed Imaging Informatics (TGI3)](First_TGI_2024.md)

[The Second Workshop on Topology- and Graph-Informed Imaging Informatics (TGI3)](Second_TGI_2025.md)

|     Time      |                           Topic                           |       Presenter      |
|:-------------:|:---------------------------------------------------------:|:--------------------:|
| 08:30 - 08:45 |               Opening Remarks, and Overview               |       Chao Chen      |
| 08:45 - 09:30 |          Topology-Aware Deep Image Segmentation           |      Xiaoling Hu     |
| 09:30 - 10:15 |     Discrete Morse Theory and Topological Uncertainty     |     Saumya Gupta     |
| 10:15 - 10:45 |                       Coffee Break                        |           -          |
| 10:45 - 11:15 |           Topological Analysis and Applications           |       Chao Chen      |
| 11:15 - 11:45 |           Topology in Medical Image Segmentation          |     Bjoern Menze     |
| 11:45 - 11:55 |                           Break                           |           -          |
| 11:55 - 12:25 |                       Betti Matching                      | Johannes C. Paetzold |
| 12:25 - 12:30 |                      Closing Remarks                      |       Chao Chen      |

* * *

<h1 style="text-align: center;">Overview</h1>

A segmentation algorithm, even with high per-pixel accuracy, could make errors on fine-scale structures, such as small instances, instances with multiple connected components, and thin connections. Such fine-scale structures may be crucial in analyzing the functionality of the objects. For example, small pixel-level errors disconnecting the segmentation of thin parts such as ropes and handles may lead to significant mistakes in the planning of robot actions, e.g., dragging or grasping. In biomedical imaging, the correct delineation of thin objects such as neuron membranes and vessels is crucial in providing accurate quantification of the underlying system. A broken connection or a missing component could cause catastrophic functional mistakes.

This tutorial aims to cover recent advances to solve the problem from the topology perspective. We will first discuss several interesting topology-aware loss functions, which help to learn to segment with correct topology for different kinds of images with fine-scale structures. Besides focusing on the topology of images with only one foreground class, we also introduce new losses to encode topological interactions among different classes (e.g., containment and exclusion). Furthermore, different from pixel-wise feature representations, we discuss direct modeling and reasoning about the structures by adopting probabilistic models. For each research sub-topic, we will give a concrete introduction of the contained problems/tasks, and the current research progress. We hope the audience, not only the graduate students but also the researchers new in this area, can benefit from this tutorial and learn the principle problems and cutting-edge approaches of topological analysis for biomedical images.

## Topology-Aware Deep Image Segmentation
Image segmentation, i.e., assigning labels to all pixels of an input image, is crucial in many computer vision tasks. State-of-the-art deep segmentation methods learn high-quality feature representations through an end-to-end trained deep network and achieve satisfactory per-pixel accuracy. However, these segmentation algorithms are still prone to make errors on fine-scale structures, such as small object instances, instances with multiple connected components, and thin connections. These fine-scale structures may be crucial in analyzing the functionality of the objects. For example, accurate extraction of thin parts such as ropes and handles is crucial in planning robot actions, e.g., dragging or grasping. In biomedical images, correct delineation of thin objects such as neuron membranes and vessels is crucial in providing accurate morphological and structural quantification of the underlying system. A broken connection or a missing component may only induce marginal per-pixel error but can cause catastrophic functional mistakes.

## Topology-Aware Uncertainty Estimation
Accurate delineation of fine-scale structures is a very important yet challenging problem. Existing methods use topological information as an additional training loss, but are ultimately making pixel-wise predictions. Motivated by this, we propose the first deep learning-based method to learn topological/structural representations. We use discrete Morse theory and persistent homology to construct a one-parameter family of structures as the topological/structural representation space. Furthermore, we learn a probabilistic model that can perform inference tasks in such a topological/structural representation space. Our method generates true structures rather than pixel maps, leading to better topological integrity in automatic segmentation tasks. It also facilitates semi-automatic interactive annotation/proofreading via the sampling of structures and structure-aware uncertainty.

## Topological Data Analysis and Applications
Topological data analysis plays an important role in more general scenarios, including pathology image analysis and graph neural networks (GNNs), which represent cutting-edge approaches at the intersection of mathematics, computer science, and medical imaging. TDA allows us to uncover hidden patterns and structures within data by leveraging concepts from algebraic topology. As these fields continue to advance, we can anticipate exciting breakthroughs and novel applications that will reshape the way we understand and utilize data.

* * *

<h1 style="text-align: center;">Organizers</h1>

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:#ffffff;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:20px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:#ffffff;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:20px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-pb0m{border-color:#ffffff;text-align:center;vertical-align:bottom}
.tg .tg-c3ow{border-color:#ffffff;text-align:center;vertical-align:top}
</style>

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
    <td class="tg-pb0m"><img src="/imgs/circle-jp.png" width="80%"></td>
    <td class="tg-pb0m"><img src="/imgs/circle-sg.png" width="80%"></td>
  </tr>
  <tr>
    <td class="tg-c3ow"><a href="https://huxiaoling.github.io/">Xiaoling Hu</a></td>
    <td class="tg-c3ow"><a href="https://scholar.google.de/citations?user=7Bv7PmgAAAAJ&hl=de">Johannes C. Paetzold</a></td>
    <td class="tg-c3ow"><a href="https://saumya-gupta-26.github.io/">Saumya Gupta</a></td>
  </tr>
</tbody>
</table>

