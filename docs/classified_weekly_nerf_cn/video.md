
每周分类神经辐射场 - video ![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)
==================================================================================================================================
## 按类别筛选: 
 [全部](../weekly_nerf_cn.md) | [动态](./dynamic.md) | [编辑](./editing.md) | [快速](./fast.md) | [泛化](./generalization.md) | [人体](./human.md) | [视频](./video.md) | [光照](./lighting.md) | [重建](./reconstruction.md) | [纹理](./texture.md) | [语义](./semantic.md) | [姿态-SLAM](./pose-slam.md) | [其他](./others.md) 
## Aug21 - Aug27, 2022
## Aug14 - Aug20, 2022
  - [通过多平面图像的 3D 对象运动估计动态场景的时间视图合成, ISMAR2022](https://arxiv.org/abs/2208.09463) | [***``[code]``***](https://github.com/NagabhushanSN95/DeCOMPnet)
    > 在低计算设备上以图形方式渲染高帧率视频的挑战可以通过对未来帧的定期预测来解决，以增强虚拟现实应用程序中的用户体验。这是通过时间视图合成 (TVS) 的问题来研究的，其目标是在给定前一帧以及前一帧和下一帧的头部姿势的情况下预测视频的下一帧。在这项工作中，我们考虑了用户和对象都在移动的动态场景的 TVS。我们设计了一个框架，将运动解耦为用户和对象运动，以在预测下一帧的同时有效地使用可用的用户运动。我们通过隔离和估计过去帧中的 3D 对象运动然后外推来预测对象的运动。我们使用多平面图像 (MPI) 作为场景的 3D 表示，并将对象运动建模为 MPI 表示中对应点之间的 3D 位移。为了在估计运动时处理 MPI 中的稀疏性，我们结合了部分卷积和掩蔽相关层来估计对应点。然后将预测的对象运动与给定的用户或相机运动集成以生成下一帧。使用遮蔽填充模块，我们合成由于相机和物体运动而未覆盖的区域。我们为包含 800 个全高清分辨率视频的动态场景 TVS 开发了一个新的合成数据集。我们通过对我们的数据集和 MPI Sintel 数据集的实验表明，我们的模型优于文献中的所有竞争方法。
  - [从单目视频中对动画 3D 人体进行神经捕获, ECCV2022](https://arxiv.org/abs/2208.08728) | [code]
    > 我们提出了一种从单目视频输入构建可动画 3D 人体表示的新颖范例，这样它就可以以任何看不见的姿势和视图进行渲染。我们的方法基于动态神经辐射场 (NeRF)，该动态神经辐射场 (NeRF) 由作为几何代理的基于网格的参数化 3D 人体模型装配。以前的方法通常依赖多视图视频或准确的 3D 几何信息作为附加输入；此外，大多数方法在推广到看不见的姿势时质量会下降。我们认为，泛化的关键是用于查询动态 NeRF 的良好输入嵌入：良好的输入嵌入应该定义全体积空间中的单射映射，由姿态变化下的表面网格变形引导。基于这一观察，我们建议嵌入输入查询及其与网格顶点上一组测地最近邻所跨越的局部表面区域的关系。通过包含位置和相对距离信息，我们的嵌入定义了距离保留的变形映射，并很好地推广到看不见的姿势。为了减少对额外输入的依赖，我们首先使用现成的工具初始化每帧 3D 网格，然后提出一个管道来联合优化 NeRF 并细化初始网格。大量实验表明，我们的方法可以在看不见的姿势和视图下合成合理的人类渲染结果。
  - [从全向图像中捕捉休闲室内 HDR 辐射](https://arxiv.org/abs/2208.07903) | [code]
    > 我们提出了 PanoHDR-NeRF，这是一种新颖的管道，可以随意捕获大型室内场景的合理全 HDR 辐射场，而无需精心设置或复杂的捕获协议。首先，用户通过在场景周围自由挥动现成的相机来捕捉场景的低动态范围 (LDR) 全向视频。 然后，LDR2HDR 网络将捕获的 LDR 帧提升为 HDR，随后用于训练定制的 NeRF++ 模型。 由此产生的 PanoHDR-NeRF 管道可以从场景的任何位置估计完整的 HDR 全景图。 通过对各种真实场景的新测试数据集进行实验，在训练期间未看到的位置捕获地面实况 HDR 辐射，我们表明 PanoHDR-NeRF 可以预测来自任何场景点的合理辐射。我们还表明，由 PanoHDR-NeRF 生成的 HDR 图像可以合成正确的照明效果，从而能够使用正确照明的合成对象来增强室内场景。
## Aug7 - Aug13, 2022
  - [PS-NeRV：视频的补丁风格化神经表示](https://arxiv.org/abs/2208.03742) | [code]
    > 我们研究如何使用隐式神经表示 (INR) 来表示视频。经典的 INR 方法通常利用 MLP 将输入坐标映射到输出像素。虽然最近的一些作品试图用 CNN 直接重建整个图像。然而，我们认为上述像素级和图像级策略都不利于视频数据。相反，我们提出了一种补丁解决方案 PS-NeRV，它将视频表示为补丁和相应补丁坐标的函数。它自然继承了image-wise方法的优点，并以快速的解码速度实现了出色的重建性能。整个方法包括传统的模块，如位置嵌入、MLPs 和 CNNs，同时还引入了 AdaIN 来增强中间特征。这些简单而重要的变化可以帮助网络轻松适应高频细节。大量实验证明了它在视频压缩和视频修复等视频相关任务中的有效性。
## Jul31 - Aug6, 2022
## Jul24 - Jul30, 2022
## Previous weeks
  - [用于动态场景时空视图合成的神经场景流场, CVPR2021](http://www.cs.cornell.edu/~zl548/NSFF/) | [***``[code]``***](https://github.com/zhengqili/Neural-Scene-Flow-Fields)
    > 我们提出了一种方法来执行动态场景的新颖视图和时间合成，只需要具有已知相机姿势的单目视频作为输入。为此，我们引入了神经场景流场，这是一种将动态场景建模为外观、几何和 3D 场景运动的时变连续函数的新表示。我们的表示通过神经网络进行优化，以适应观察到的输入视图。我们表明，我们的表示可用于复杂的动态场景，包括薄结构、视图相关效果和自然运动度。我们进行了许多实验，证明我们的方法明显优于最近的单目视图合成方法，并展示了各种真实世界视频的时空视图合成的定性结果。
  - [来自多视图视频的神经 3D 视频合成, CVPR2022(oral)](https://neural-3d-video.github.io/) | [code]
    > 我们提出了一种新颖的 3D 视频合成方法，能够以紧凑但富有表现力的表示形式表示动态真实世界场景的多视图视频记录，从而实现高质量的视图合成和运动插值。我们的方法将静态神经辐射场的高质量和紧凑性带到了一个新的方向：无模型的动态设置。我们方法的核心是一种新颖的时间条件神经辐射场，它使用一组紧凑的潜在代码来表示场景动态。为了利用视频相邻帧之间的变化通常很小且局部一致的事实，我们提出了两种有效训练神经网络的新策略：1）有效的分层训练方案，以及 2）选择根据输入视频的时间变化进行训练的下一条光线。结合起来，这两种策略显着提高了训练速度，导致训练过程快速收敛，并获得高质量的结果。我们学习的表示非常紧凑，能够表示由 18 个摄像机录制的 10 秒 30 FPS 多视图视频，模型大小仅为 28MB。我们证明了我们的方法可以以超过 1K 的分辨率渲染高保真广角新颖视图，即使对于高度复杂和动态的场景也是如此。我们进行了广泛的定性和定量评估，表明我们的方法优于当前的技术水平。项目网站：https://neural-3d-video.github.io。
  - [动态单目视频的动态视图合成, ICCV2021](https://free-view-video.github.io/) | [***``[code]``***](https://github.com/gaochen315/DynamicNeRF)
    > 我们提出了一种算法，用于在给定动态场景的单目视频的任意视点和任何输入时间步长处生成新视图。我们的工作建立在神经隐式表示的最新进展的基础上，并使用连续和可微的函数来建模时变结构和场景的外观。我们联合训练一个时不变的静态 NeRF 和一个时变的动态 NeRF，并学习如何以无监督的方式混合结果。然而，从单个视频中学习这个隐式函数是非常不适定的（与输入视频匹配的解决方案有无限多）。为了解决歧义，我们引入了正则化损失以鼓励更合理的解决方案。我们展示了从随意捕获的视频中进行动态视图合成的广泛定量和定性结果。
  - [使用分层神经表示的可编辑自由视点视频, SIGGRAPH2021](https://jiakai-zhang.github.io/st-nerf/) | [***``[code]``***](https://jiakai-zhang.github.io/st-nerf/#code)
    > 生成自由视点视频对于沉浸式 VR/AR 体验至关重要，但最近的神经学进展仍然缺乏编辑能力来操纵大型动态场景的视觉感知。为了填补这一空白，在本文中，我们提出了第一种仅使用稀疏的 16 个摄像头为大规模动态场景生成可编辑照片般逼真的自由视点视频的方法。我们方法的核心是一种新的分层神经表示，其中包括环境本身的每个动态实体都被制定为称为 ST-NeRF 的时空相干神经分层辐射表示。这种分层表示支持对动态场景的完全感知和真实操作，同时仍支持大范围的自由观看体验。在我们的 ST-NeRF 中，动态实体/层被表示为连续函数，以连续和自监督的方式实现动态实体的位置、变形以及外观的解耦。我们提出了一个场景解析 4D 标签映射跟踪来显式地解开空间信息，以及一个连续变形模块来隐式地解开时间运动。进一步引入了一种对象感知体绘制方案，用于重新组装所有神经层。我们采用了一种新颖的分层损失和运动感知光线采样策略，以实现对具有多个表演者的大型动态场景的有效训练，我们的框架进一步实现了各种编辑功能，即操纵规模和位置，复制或重新定时单个神经层在保持高度真实感的同时创造众多视觉效果。大量实验证明了我们的方法在为动态场景生成高质量、照片般逼真和可编辑的自由视点视频方面的有效性。