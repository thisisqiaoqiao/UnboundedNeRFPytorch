
Weekly Classified Neural Radiance Fields - semantic ![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)
====================================================================================================================================================================
## Filter by classes: 
 [all](../weekly_nerf.md) | [dynamic](./dynamic.md) | [editing](./editing.md) | [fast](./fast.md) | [generalization](./generalization.md) | [human](./human.md) | [video](./video.md) | [lighting](./lighting.md) | [reconstruction](./reconstruction.md) | [texture](./texture.md) | [semantic](./semantic.md) | [pose-slam](./pose-slam.md) | [others](./others.md) 
## Aug21 - Aug27, 2022
  - [DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation](https://dreambooth.github.io/) | [code]
    > Large text-to-image models achieved a remarkable leap in the evolution of AI, enabling high-quality and diverse synthesis of images from a given text prompt. However, these models lack the ability to mimic the appearance of subjects in a given reference set and synthesize novel renditions of them in different contexts. In this work, we present a new approach for "personalization" of text-to-image diffusion models (specializing them to users' needs). Given as input just a few images of a subject, we fine-tune a pretrained text-to-image model (Imagen, although our method is not limited to a specific model) such that it learns to bind a unique identifier with that specific subject. Once the subject is embedded in the output domain of the model, the unique identifier can then be used to synthesize fully-novel photorealistic images of the subject contextualized in different scenes. By leveraging the semantic prior embedded in the model with a new autogenous class-specific prior preservation loss, our technique enables synthesizing the subject in diverse scenes, poses, views, and lighting conditions that do not appear in the reference images. We apply our technique to several previously-unassailable tasks, including subject recontextualization, text-guided view synthesis, appearance modification, and artistic rendering (all while preserving the subject's key features). Project page: this https URL
## Aug14 - Aug20, 2022
## Aug7 - Aug13, 2022
## Jul31 - Aug6, 2022
  - [NeSF: Neural Semantic Fields for Generalizable Semantic Segmentation of 3D Scenes](https://research.google/pubs/pub51563/) | [code]
    > We present NeSF, a method for producing 3D semantic fields from pre-trained density fields and sparse 2D semantic supervision. Our method side-steps traditional scene representations by leveraging neural representations where 3D information is stored within neural fields. In spite of being supervised by 2D signals alone, our method is able to generate 3D-consistent semantic maps from novel camera poses and can be queried at arbitrary 3D points. Notably, NeSF is compatible with any method producing a density field, and its accuracy improves as the quality of the pre-trained density fields improve. Our empirical analysis demonstrates comparable quality to competitive 2D and 3D semantic segmentation baselines on convincing synthetic scenes while also offering features unavailable to existing methods.
## Jul24 - Jul30, 2022
## Previous weeks
  - [Putting NeRF on a Diet: Semantically Consistent Few-Shot View Synthesis, ICCV2021](https://www.ajayj.com/dietnerf) | [***``[code]``***](https://github.com/ajayjain/DietNeRF)
    > We present DietNeRF, a 3D neural scene representation estimated from a few images. Neural Radiance Fields (NeRF) learn a continuous volumetric representation of a scene through multi-view consistency, and can be rendered from novel viewpoints by ray casting. While NeRF has an impressive ability to reconstruct geometry and fine details given many images, up to 100 for challenging 360° scenes, it often finds a degenerate solution to its image reconstruction objective when only a few input views are available. To improve few-shot quality, we propose DietNeRF. We introduce an auxiliary semantic consistency loss that encourages realistic renderings at novel poses. DietNeRF is trained on individual scenes to (1) correctly render given input views from the same pose, and (2) match high-level semantic attributes across different, random poses. Our semantic loss allows us to supervise DietNeRF from arbitrary poses. We extract these semantics using a pre-trained visual encoder such as CLIP, a Vision Transformer trained on hundreds of millions of diverse single-view, 2D photographs mined from the web with natural language supervision. In experiments, DietNeRF improves the perceptual quality of few-shot view synthesis when learned from scratch, can render novel views with as few as one observed image when pre-trained on a multi-view dataset, and produces plausible completions of completely unobserved regions.
  - [Unsupervised Discovery of Object Radiance Fields, ICLR2022](https://arxiv.org/abs/2107.07905) | [code]
    > We study the problem of inferring an object-centric scene representation from a single image, aiming to derive a representation that explains the image formation process, captures the scene's 3D nature, and is learned without supervision. Most existing methods on scene decomposition lack one or more of these characteristics, due to the fundamental challenge in integrating the complex 3D-to-2D image formation process into powerful inference schemes like deep networks. In this paper, we propose unsupervised discovery of Object Radiance Fields (uORF), integrating recent progresses in neural 3D scene representations and rendering with deep inference networks for unsupervised 3D scene decomposition. Trained on multi-view RGB images without annotations, uORF learns to decompose complex scenes with diverse, textured background from a single image. We show that uORF performs well on unsupervised 3D scene segmentation, novel view synthesis, and scene editing on three datasets.
  - [In-Place Scene Labelling and Understanding with Implicit Scene Representation, ICCV2021(oral)](https://shuaifengzhi.com/Semantic-NeRF/) | [***``[code]``***](https://github.com/Harry-Zhi/semantic_nerf/)
    > Semantic labelling is highly correlated with geometry and radiance reconstruction, as scene entities with similar shape and appearance are more likely to come from similar classes. Recent implicit neural reconstruction techniques are appealing as they do not require prior training data, but the same fully self-supervised approach is not possible for semantics because labels are human-defined properties.