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
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/DragGAN.pdf) 
\
2023-05-18\
**Authors:** Xingang Pan, Ayush Tewari, Thomas Leimkühler, Lingjie Liu, Abhimitra Meka, Christian Theobalt
<details span>
<summary>Abstract</summary>
Synthesizing visual content that meets users' needs often requires flexible and precise controllability of the pose, shape, expression, and layout of the generated objects. Existing approaches gain controllability of generative adversarial networks (GANs) via manually annotated training data or a prior 3D model, which often lack flexibility, precision, and generality. In this work, we study a powerful yet much less explored way of controlling GANs, that is, to "drag" any points of the image to precisely reach target points in a user-interactive manner, as shown in Fig.1. To achieve this, we propose DragGAN, which consists of two main components including: 1) a feature-based motion supervision that drives the handle point to move towards the target position, and 2) a new point tracking approach that leverages the discriminative GAN features to keep localizing the position of the handle points. Through DragGAN, anyone can deform an image with precise control over where pixels go, thus manipulating the pose, shape, expression, and layout of diverse categories such as animals, cars, humans, landscapes, etc. As these manipulations are performed on the learned generative image manifold of a GAN, they tend to produce realistic outputs even for challenging scenarios such as hallucinating occluded content and deforming shapes that consistently follow the object's rigidity. Both qualitative and quantitative comparisons demonstrate the advantage of DragGAN over prior approaches in the tasks of image manipulation and point tracking. We also showcase the manipulation of real images through GAN inversion.

![DragGAN](./imgs/DragGAN.png)
</details>

---

### DragDiffusion: Harnessing Diffusion Models for Interactive Point-based Image Editing
![Publication](https://img.shields.io/badge/2024-CVPR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2306.14435-b31b1b.svg)](https://arxiv.org/abs/2306.14435) 
[![GitHub stars](https://img.shields.io/github/stars/Yujun-Shi/DragDiffusion?logo=github&label=Stars)](https://github.com/Yujun-Shi/DragDiffusion)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://yujun-shi.github.io/projects/dragdiffusion.html)
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/DragDiffusion.pdf) 
\
2023-06-26\
**Authors:** Yujun Shi, Chuhui Xue, Jun Hao Liew, Jiachun Pan, Hanshu Yan, Wenqing Zhang
<details span>
<summary>Abstract</summary>
Precise and controllable image editing is a challenging task that has attracted significant attention. Recently, DragGAN enables an interactive point-based image editing framework and achieves impressive editing results with pixel-level precision. However, since this method is based on generative adversarial networks (GAN), its generality is upper-bounded by the capacity of the pre-trained GAN models. In this work, we extend such an editing framework to diffusion models and propose DragDiffusion. By leveraging large-scale pretrained diffusion models, we greatly improve the applicability of interactive point-based editing in real world scenarios. While most existing diffusion-based image editing methods work on text embeddings, DragDiffusion optimizes the diffusion latent to achieve precise spatial control. Although diffusion models generate images in an iterative manner, we empirically show that optimizing diffusion latent at one single step suffices to generate coherent results, enabling DragDiffusion to complete high-quality editing efficiently. Extensive experiments across a wide range of challenging cases (e.g., multi-objects, diverse object categories, various styles, etc.) demonstrate the versatility and generality of DragDiffusion.

![DragDiffusion](./imgs/DragDiffusion.png)
</details>

---

### DragonDiffusion: Enabling Drag-style Manipulation on Diffusion Models
![Publication](https://img.shields.io/badge/2024-ICLR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2307.02421-b31b1b.svg)](https://arxiv.org/abs/2307.02421) 
[![GitHub stars](https://img.shields.io/github/stars/MC-E/DragonDiffusion?logo=github&label=Stars)](https://github.com/MC-E/DragonDiffusion)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://mc-e.github.io/project/DragonDiffusion/)
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/DragonDiffusion.pdf) 
\
2023-07-05\
**Authors:** Chong Mou, Xintao Wang, Jiechong Song, Ying Shan, Jian Zhang
<details span>
<summary>Abstract</summary>
Despite the ability of existing large-scale text-to-image (T2I) models to generate high-quality images from detailed textual descriptions, they often lack the ability to precisely edit the generated or real images. In this paper, we propose a novel image editing method, DragonDiffusion, enabling Drag-style manipulation on Diffusion models. Specifically, we construct classifier guidance based on the strong correspondence of intermediate features in the diffusion model. It can transform the editing signals into gradients via feature correspondence loss to modify the intermediate representation of the diffusion model. Based on this guidance strategy, we also build a multi-scale guidance to consider both semantic and geometric alignment. Moreover, a cross-branch self-attention is added to maintain the consistency between the original image and the editing result. Our method, through an efficient design, achieves various editing modes for the generated or real images, such as object moving, object resizing, object appearance replacement, and content dragging. It is worth noting that all editing and content preservation signals come from the image itself, and the model does not require fine-tuning or additional modules.

![DragonDiffusion](./imgs/DragonDiffusion.png)
</details>

## Editing Result Improvement

### FreeDrag: Feature Dragging for Reliable Point-based Image Editing
![Publication](https://img.shields.io/badge/2024-CVPR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2307.04684-b31b1b.svg)](https://arxiv.org/abs/2307.04684) 
[![GitHub stars](https://img.shields.io/github/stars/LPengYang/FreeDrag?logo=github&label=Stars)](https://github.com/LPengYang/FreeDrag)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://lin-chen.site/projects/freedrag)
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/FreeDrag.pdf) 
\
2023-07-10\
**Authors:** Pengyang Ling, Lin Chen, Pan Zhang, Huaian Chen, Yi Jin, Jinjin Zheng
<details span>
<summary>Abstract</summary>
To serve the intricate and varied demands of image editing, precise and flexible manipulation in image content is indispensable. Recently, Drag-based editing methods have gained impressive performance. However, these methods predominantly center on point dragging, resulting in two noteworthy drawbacks, namely "miss tracking", where difficulties arise in accurately tracking the predetermined handle points, and "ambiguous tracking", where tracked points are potentially positioned in wrong regions that closely resemble the handle points. To address the above issues, we propose FreeDrag, a feature dragging methodology designed to free the burden on point tracking. The FreeDrag incorporates two key designs, i.e., template feature via adaptive updating and line search with backtracking, the former improves the stability against drastic content change by elaborately controls feature updating scale after each dragging, while the latter alleviates the misguidance from similar points by actively restricting the search area in a line. These two technologies together contribute to a more stable semantic dragging with higher efficiency. Comprehensive experimental results substantiate that our approach significantly outperforms pre-existing methodologies, offering reliable point-based editing even in various complex scenarios.

![FreeDrag](./imgs/FreeDrag.png)
</details>

---
### The Blessing of Randomness: SDE Beats ODE in General Diffusion-Based Image Editing (SDE-Drag)
![Publication](https://img.shields.io/badge/2024-ICLR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2311.01410-b31b1b.svg)](https://arxiv.org/abs/2311.01410) 
[![GitHub stars](https://img.shields.io/github/stars/ML-GSAI/SDE-Drag?logo=github&label=Stars)](https://github.com/ML-GSAI/SDE-Drag)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://ml-gsai.github.io/SDE-Drag-demo/)
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/SDE-Drag.pdf) 
\
2023-11-02\
**Authors:** Shen Nie, Hanzhong Allan Guo, Cheng Lu, Yuhao Zhou, Chenyu Zheng, Chongxuan Li
<details span>
<summary>Abstract</summary>
We present a unified probabilistic formulation for diffusion-based image editing, where a latent variable is edited in a task-specific manner and generally deviates from the corresponding marginal distribution induced by the original stochastic or ordinary differential equation (SDE or ODE). Instead, it defines a corresponding SDE or ODE for editing. In the formulation, we prove that the Kullback-Leibler divergence between the marginal distributions of the two SDEs gradually decreases while that for the ODEs remains as the time approaches zero, which shows the promise of SDE in image editing. Inspired by it, we provide the SDE counterparts for widely used ODE baselines in various tasks including inpainting and image-to-image translation, where SDE shows a consistent and substantial improvement. Moreover, we propose SDE-Drag -- a simple yet effective method built upon the SDE formulation for point-based content dragging. We build a challenging benchmark (termed DragBench) with open-set natural, art, and AI-generated images for evaluation. A user study on DragBench indicates that SDE-Drag significantly outperforms our ODE baseline, existing diffusion-based methods, and the renowned DragGAN. Our results demonstrate the superiority and versatility of SDE in image editing and push the boundary of diffusion-based editing methods.

![SDEDrag](./imgs/SDEDrag.png)
</details>

---

### StableDrag: Stable Dragging for Point-based Image Editing
![Publication](https://img.shields.io/badge/2024-ECCV-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2403.04437-b31b1b.svg)](https://arxiv.org/abs/2403.04437) 
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://stabledrag.github.io/)
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/StableDrag.pdf) 
\
2024-03-07\
**Authors:** Yutao Cui, Xiaotong Zhao, Guozhen Zhang, Shengming Cao, Kai Ma, Limin Wang
<details span>
<summary>Abstract</summary>
Point-based image editing has attracted remarkable attention since the emergence of DragGAN. Recently, DragDiffusion further pushes forward the generative quality via adapting this dragging technique to diffusion models. Despite these great success, this dragging scheme exhibits two major drawbacks, namely inaccurate point tracking and incomplete motion supervision, which may result in unsatisfactory dragging outcomes. To tackle these issues, we build a stable and precise drag-based editing framework, coined as StableDrag, by designing a discirminative point tracking method and a confidence-based latent enhancement strategy for motion supervision. The former allows us to precisely locate the updated handle points, thereby boosting the stability of long-range manipulation, while the latter is responsible for guaranteeing the optimized latent as high-quality as possible across all the manipulation steps. Thanks to these unique designs, we instantiate two types of image editing models including StableDrag-GAN and StableDrag-Diff, which attains more stable dragging performance, through extensive qualitative experiments and quantitative assessment on DragBench.

![StableDrag](./imgs/StableDrag.png)
</details>

---

### Drag Your Noise: Interactive Point-based Editing via Diffusion Semantic Propagation
![Publication](https://img.shields.io/badge/2024-CVPR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2404.01050-b31b1b.svg)](https://arxiv.org/abs/2404.01050) 
[![GitHub stars](https://img.shields.io/github/stars/haofengl/DragNoise?logo=github&label=Stars)](https://github.com/haofengl/DragNoise)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://vcai.mpi-inf.mpg.de/projects/DragGAN/)
\
2024-04-01\
**Authors:** Haofeng Liu, Chenshu Xu, Yifei Yang, Lihua Zeng, Shengfeng He
<details span>
<summary>Abstract</summary>
Point-based interactive editing serves as an essential tool to complement the controllability of existing generative models. A concurrent work, DragDiffusion, updates the diffusion latent map in response to user inputs, causing global latent map alterations. This results in imprecise preservation of the original content and unsuccessful editing due to gradient vanishing. In contrast, we present DragNoise, offering robust and accelerated editing without retracing the latent map. The core rationale of DragNoise lies in utilizing the predicted noise output of each U-Net as a semantic editor. This approach is grounded in two critical observations: firstly, the bottleneck features of U-Net inherently possess semantically rich features ideal for interactive editing; secondly, high-level semantics, established early in the denoising process, show minimal variation in subsequent stages. Leveraging these insights, DragNoise edits diffusion semantics in a single denoising step and efficiently propagates these changes, ensuring stability and efficiency in diffusion editing. Comparative experiments reveal that DragNoise achieves superior control and semantic retention, reducing the optimization time by over 50% compared to DragDiffusion.

![DragNoise](./imgs/DragNoise.png)
</details>

---

### Localize, Understand, Collaborate: Semantic-Aware Dragging via Intention Reasoner
![Publication](https://img.shields.io/badge/2024-NeurIPS-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2406.00432-b31b1b.svg)](https://arxiv.org/abs/2406.00432) 
[![GitHub stars](https://img.shields.io/github/stars/cuixing100876/LucidDrag-NeurIPS2024?logo=github&label=Stars)](https://github.com/cuixing100876/LucidDrag-NeurIPS2024)
\
2024-06-01\
**Authors:** Xing Cui, Peipei Li, Zekun Li, Xuannan Liu, Yueying Zou, Zhaofeng He
<details span>
<summary>Abstract</summary>
Flexible and accurate drag-based editing is a challenging task that has recently garnered significant attention. Current methods typically model this problem as automatically learning "how to drag" through point dragging and often produce one deterministic estimation, which presents two key limitations: 1) Overlooking the inherently ill-posed nature of drag-based editing, where multiple results may correspond to a given input, as illustrated in Fig.1; 2) Ignoring the constraint of image quality, which may lead to unexpected distortion. To alleviate this, we propose LucidDrag, which shifts the focus from "how to drag" to "what-then-how" paradigm. LucidDrag comprises an intention reasoner and a collaborative guidance sampling mechanism. The former infers several optimal editing strategies, identifying what content and what semantic direction to be edited. Based on the former, the latter addresses "how to drag" by collaboratively integrating existing editing guidance with the newly proposed semantic guidance and quality guidance. Specifically, semantic guidance is derived by establishing a semantic editing direction based on reasoned intentions, while quality guidance is achieved through classifier guidance using an image fidelity discriminator. Both qualitative and quantitative comparisons demonstrate the superiority of LucidDrag over previous methods.


![LucidDrag](./imgs/LucidDrag.png)
</details>

## Performance Improvement
### Diffeditor: Boosting accuracy and flexibility on diffusion-based image editing
![Publication](https://img.shields.io/badge/2024-CVPR-43aa8b) 
[![arXiv](https://img.shields.io/badge/arXiv-2402.02583-b31b1b.svg)](https://arxiv.org/abs/2402.02583) 
[![GitHub stars](https://img.shields.io/github/stars/MC-E/DragonDiffusion?logo=github&label=Stars)](https://github.com/MC-E/DragonDiffusion)
[![Webpage](https://img.shields.io/badge/Project-Page-3cba54?style=flat&logo=Google%20chrome&logoColor=white)](https://mc-e.github.io/project/DragonDiffusion/)
[![PDF](https://img.shields.io/badge/PDF-File-4287f5.svg)](./papers/DiffEditor.pdf) 
\
2024-02-04\
**Authors:** Chong Mou, Xintao Wang, Jiechong Song, Ying Shan, Jian Zhang
<details span>
<summary>Abstract</summary>
Large-scale Text-to-Image (T2I) diffusion models have revolutionized image generation over the last few years. Although owning diverse and high-quality generation capabilities, translating these abilities to fine-grained image editing remains challenging. In this paper, we propose DiffEditor to rectify two weaknesses in existing diffusion-based image editing: (1) in complex scenarios, editing results often lack editing accuracy and exhibit unexpected artifacts; (2) lack of flexibility to harmonize editing operations, e.g., imagine new content. In our solution, we introduce image prompts in fine-grained image editing, cooperating with the text prompt to better describe the editing content. To increase the flexibility while maintaining content consistency, we locally combine stochastic differential equation (SDE) into the ordinary differential equation (ODE) sampling. In addition, we incorporate regional score-based gradient guidance and a time travel strategy into the diffusion sampling, further improving the editing quality. Extensive experiments demonstrate that our method can efficiently achieve state-of-the-art performance on various fine-grained image editing tasks, including editing within a single image (e.g., object moving, resizing, and content dragging) and across images (e.g., appearance replacing and object pasting).


![DiffEditor](./imgs/DiffEditor.png)
</details>

---


EasyDrag: Efficient Point-based Manipulation on Diffusion Models
LightningDrag: Lightning Fast and Accurate Drag-based Image Editing Emerging from Videos
FastDrag: Manipulate Anything in One Step
InstantDrag: Improving Interactivity in Drag-based Image Editing
## Novel View Perspective
Readout Guidance: Learning Control from Diffusion Features
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
