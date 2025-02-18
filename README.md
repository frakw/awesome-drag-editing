# Awesome Drag Editing Resources [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
 A collection of papers and resources for drag editing
## Table of contents
- [Seminal Papers](#seminal-papers)
- [Editing Result Improvement](#editing-result-improvement)
- [Performance Improvement](#performance-improvement)
- [Novel View Perspective](#novel-view-perspective)
- [Novel View Application](#novel-view-application)
- [Uncategory Papers](#uncategory-papers)
- [Datasets](#datasets)
- [Software & Tools](#software--tools)
- [Tutorials & Videos](#tutorials--videos)
## Seminal Papers
### Drag Your GAN: Interactive Point-based Manipulation on the Generative Image Manifold (DragGAN)
![Publication](https://img.shields.io/badge/2023-SIGGRAPH-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2305.10973-b31b1b.svg)](https://arxiv.org/abs/2305.10973) 
[![GitHub stars](https://img.shields.io/github/stars/XingangPan/DragGAN?logo=github&label=Stars)](https://github.com/XingangPan/DragGAN)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://vcai.mpi-inf.mpg.de/projects/DragGAN/)
\
2023-05-18\
**Authors:** Xingang Pan, Ayush Tewari, Thomas Leimkühler, Lingjie Liu, Abhimitra Meka, Christian Theobalt
<details span>
<summary>Abstract</summary>
Synthesizing visual content that meets users' needs often requires flexible and precise controllability of the pose, shape, expression, and layout of the generated objects. Existing approaches gain controllability of generative adversarial networks (GANs) via manually annotated training data or a prior 3D model, which often lack flexibility, precision, and generality. In this work, we study a powerful yet much less explored way of controlling GANs, that is, to "drag" any points of the image to precisely reach target points in a user-interactive manner, as shown in Fig.1. To achieve this, we propose DragGAN, which consists of two main components including: 1) a feature-based motion supervision that drives the handle point to move towards the target position, and 2) a new point tracking approach that leverages the discriminative GAN features to keep localizing the position of the handle points. Through DragGAN, anyone can deform an image with precise control over where pixels go, thus manipulating the pose, shape, expression, and layout of diverse categories such as animals, cars, humans, landscapes, etc. As these manipulations are performed on the learned generative image manifold of a GAN, they tend to produce realistic outputs even for challenging scenarios such as hallucinating occluded content and deforming shapes that consistently follow the object's rigidity. Both qualitative and quantitative comparisons demonstrate the advantage of DragGAN over prior approaches in the tasks of image manipulation and point tracking. We also showcase the manipulation of real images through GAN inversion.

![DragGAN](./imgs/DragGAN.png)
</details>

### DragDiffusion: Harnessing Diffusion Models for Interactive Point-based Image Editing
![Publication](https://img.shields.io/badge/2024-CVPR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2306.14435-b31b1b.svg)](https://arxiv.org/abs/2306.14435) 
[![GitHub stars](https://img.shields.io/github/stars/Yujun-Shi/DragDiffusion?logo=github&label=Stars)](https://github.com/Yujun-Shi/DragDiffusion)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://yujun-shi.github.io/projects/dragdiffusion.html)
\
2023-06-26\
**Authors:** Yujun Shi, Chuhui Xue, Jun Hao Liew, Jiachun Pan, Hanshu Yan, Wenqing Zhang
<details span>
<summary>Abstract</summary>
Precise and controllable image editing is a challenging task that has attracted significant attention. Recently, DragGAN enables an interactive point-based image editing framework and achieves impressive editing results with pixel-level precision. However, since this method is based on generative adversarial networks (GAN), its generality is upper-bounded by the capacity of the pre-trained GAN models. In this work, we extend such an editing framework to diffusion models and propose DragDiffusion. By leveraging large-scale pretrained diffusion models, we greatly improve the applicability of interactive point-based editing in real world scenarios. While most existing diffusion-based image editing methods work on text embeddings, DragDiffusion optimizes the diffusion latent to achieve precise spatial control. Although diffusion models generate images in an iterative manner, we empirically show that optimizing diffusion latent at one single step suffices to generate coherent results, enabling DragDiffusion to complete high-quality editing efficiently. Extensive experiments across a wide range of challenging cases (e.g., multi-objects, diverse object categories, various styles, etc.) demonstrate the versatility and generality of DragDiffusion.

![DragDiffusion](./imgs/DragDiffusion.png)
</details>

### DragonDiffusion: Enabling Drag-style Manipulation on Diffusion Models
![Publication](https://img.shields.io/badge/2024-ICLR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2307.02421-b31b1b.svg)](https://arxiv.org/abs/2307.02421) 
[![GitHub stars](https://img.shields.io/github/stars/MC-E/DragonDiffusion?logo=github&label=Stars)](https://github.com/MC-E/DragonDiffusion)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://vcai.mpi-inf.mpg.de/projects/DragGAN/)
\
2023-07-05\
**Authors:** Chong Mou, Xintao Wang, Jiechong Song, Ying Shan, Jian Zhang
<details span>
<summary>Abstract</summary>
Despite the ability of existing large-scale text-to-image (T2I) models to generate high-quality images from detailed textual descriptions, they often lack the ability to precisely edit the generated or real images. In this paper, we propose a novel image editing method, DragonDiffusion, enabling Drag-style manipulation on Diffusion models. Specifically, we construct classifier guidance based on the strong correspondence of intermediate features in the diffusion model. It can transform the editing signals into gradients via feature correspondence loss to modify the intermediate representation of the diffusion model. Based on this guidance strategy, we also build a multi-scale guidance to consider both semantic and geometric alignment. Moreover, a cross-branch self-attention is added to maintain the consistency between the original image and the editing result. Our method, through an efficient design, achieves various editing modes for the generated or real images, such as object moving, object resizing, object appearance replacement, and content dragging. It is worth noting that all editing and content preservation signals come from the image itself, and the model does not require fine-tuning or additional modules.

![DragonDiffusion](./imgs/DragonDiffusion.png)
</details>

## Editing Result Improvement
The Blessing of Randomness: SDE Beats ODE in General Diffusion-based Image Editing
<br>
Dragondiffusion: Enabling drag-style manipulation on diffusion models
<br>
Localize, Understand, Collaborate: Semantic-Aware Dragging via Intention Reasoner
FreeDrag: Feature Dragging for Reliable Point-based Image Editing
StableDrag: Stable Dragging for Point-based Image Editing
Drag Your Noise: Interactive Point-based Editing via Diffusion Semantic Propagation
## Performance Improvement
LightningDrag: Lightning Fast and Accurate Drag-based Image Editing Emerging from Videos
FastDrag: Manipulate Anything in One Step
InstantDrag: Improving Interactivity in Drag-based Image Editing
EasyDrag: Efficient Point-based Manipulation on Diffusion Models
Diffeditor: Boosting accuracy and flexibility on diffusion-based image editing
Readout Guidance: Learning Control from Diffusion Features
## Novel View Perspective
RegionDrag: Fast Region-Based Image Editing with Diffusion Models
## Novel View Application
DragVideo: Interactive Drag-style Video Editing
Drag3D: DragGAN meets GET3D
Edit One for All: Interactive Batch Image Editing
Dragapart: Learning a part-level motion prior for articulated objects
## Uncategory Papers
GeoDiffuser: Geometry-Based Image Editing with Diffusion Models
Move Anything with Layered Scene Diffusion
## Datasets
DragBench
https://github.com/Yujun-Shi/DragDiffusion/releases/tag/v0.1.1
## Software & Tools
## Tutorials & Videos
