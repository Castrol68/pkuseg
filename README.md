# PKUSeg
##语义分割工具https://www.yanxishe.com/tweet/38841?from=timeline
## Introduction
yuy
PKUSeg is an open source semantic segmentation toolbox based on PyTorch, which is maintained 
by EECS of Peking University. Maintainers are all from Key Laboratory of Machine Perception (MOE).


## Major features

- **Modular design and easy to use and deploy**  
   We develop this tool for easier experiments and deployment．
- **All kinds of models for semantic segmentation**  
   We implement many state-of-the-art models in research papers. We not only release codes, but also training checkpoints.
- **State-of-the-art results on multiple datasets**  
   We achieve the state-of-the-art results on multiple datasets including Pascal VOC, Cityscapes, Pascal Context
   and ADE20K．

## Implemented Papers
- PSPNet: Pyramid Scene Parsing Network **[CVPR2017](https://arxiv.org/pdf/1612.01105.pdf)**
- DeepLabV3: Rethinking Atrous Convolution for Semantic Image Segmentation **[CVPR2017](https://arxiv.org/pdf/1706.05587.pdf)**
- DeepLabV3+: Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation **[ECCV2018](http://openaccess.thecvf.com/content_ECCV_2018/papers/Liang-Chieh_Chen_Encoder-Decoder_with_Atrous_ECCV_2018_paper.pdf)**
- DenseASPP: DenseASPP for Semantic Segmentation in Street Scenes **[CVPR2018](http://openaccess.thecvf.com/content_cvpr_2018/papers/Yang_DenseASPP_for_Semantic_CVPR_2018_paper.pdf)**
- DANet: Dual Attention Network for Scene Segmentation **[CVPR2019](https://arxiv.org/pdf/1809.02983.pdf)**
- EMANet: Expectation-Maximization Attention Networks for Semantic Segmentation
 **[ICCV2019](https://arxiv.org/abs/1907.13426)**

## Performances with PKUSeg
All the performances showed below fully reimplemented the papers' results.

#### PASCAL VOC

- Single Scale Whole Image Test: Base LR 0.01, Crop Size 513

| Model | Backbone | Train | Test | mIOU | BS | Iters | Scripts |
|:--------|:---------|:------|:------|:------|:------|:------|:------|
| [PSPNet]() | [3x3-Res101]() | train | val | 78.75 | 16 | 3W | [PSPNet]() |
| [DeepLabV3]() | [3x3-Res101]() | train | val | 78.95 | 16 | 3W | [DeepLabV3]() |
| [EMANet]() | [3x3-Res101]() | train | val | 79.79 | 16 | 3W | [EMANet]() |

#### Cityscapes

- Single Scale Whole Image Test: Base LR 0.01, Crop Size 769

| Model | Backbone | Train | Test | mIOU | BS | Iters | Scripts |
|:--------|:---------|:------|:------|:------|:------|:------|:------|
| [PSPNet]() | [3x3-Res101]() | train | val | 78.20 | 8 | 4W | [PSPNet]() |
| [DeepLabV3]() | [3x3-Res101]() | train | val | 79.13 | 8 | 4W | [DeepLabV3]() |

#### ADE20K

- Single Scale Whole Image Test: Base LR 0.02, Crop Size 520

| Model | Backbone | Train | Test | mIOU | PixelACC | BS | Iters | Scripts |
|:--------|:---------|:------|:------|:------|:------|:------|:------|:------|
| [PSPNet]() | [3x3-Res50]() | train | val | 41.52 | 80.09 | 16 | 15W | [PSPNet]() |
| [DeepLabv3]() | [3x3-Res50]() | train | val | 42.16 | 80.36 | 16 | 15W | [DeepLabV3]() |
| [PSPNet]() | [3x3-Res101]() | train | val | 43.60 | 81.30 | 16 | 15W | [PSPNet]() |
| [DeepLabv3]() | [3x3-Res101]() | train | val | 44.13 | 81.42 | 16 | 15W | [DeepLabV3]() |


## License

This project is released under the Apache 2.0 license.
