# Neural Map Prior for Autonomous Driving (CVPR 2023)

### [arXiv Paper](https://arxiv.org/abs/2304.08481) | [CVF Paper](https://openaccess.thecvf.com/content/CVPR2023/papers/Xiong_Neural_Map_Prior_for_Autonomous_Driving_CVPR_2023_paper.pdf) | [Webpage](https://tsinghua-mars-lab.github.io/neural_map_prior/) | [5-min video](https://www.youtube.com/watch?v=FpzxaBVw3L0)

[Xuan Xiong](), [Yicheng Liu](https://scholar.google.com.hk/citations?hl=en&user=vRmsgQUAAAAJ), [Tianyuan Yuan](), [Yue Wang](https://people.csail.mit.edu/yuewang/), [Yilun Wang](https://scholar.google.com.hk/citations?user=nUyTDosAAAAJ&hl=en/), [Hang Zhao](http://people.csail.mit.edu/hangzhao/)

## Introduction

A neural representation of HD maps to improve local map inference performance for autonomous driving.

This repo is official implementation of "Neural Map Prior for Autonomous
Driving". Our main contributions are:

* __A novel mapping paradigm__: integrates the __maintenance of global maps__ and
  the __inference of online local maps__.
* __Efficient fusion modules__:  __current-to-prior attention__ and __gated recurrent unit__ modules facilitate
  the efficient fusion of global and local map features.
* __Easy integration with HD map learning methods__: Neural Map Prior can be easily applied to various map segmentation
  and detection methods. Moreover, our approach demonstrates significant advancements in challenging scenarios,
  such as __bad weather conditions__ and __longer perception ranges__.
* __Sparse map tiles__: a memory-efficient approach for storing neural representations of city-scale HD maps.

Notes

* The most challenging part of the training and testing process is distributing the appropriate map tile to each GPU and
  keeping samples in the same map tiles updated on the same GPU map. This process includes two steps:
    1. Determine the map tile for each GPU. This can be done with some functions in `map_tiles/lane_render.py`.
    2. Rewrite the sampler so that each GPU can only sample the samples in the map tile assigned to it. This can be done
       in `data_samplers.py`.

## Model Zoo

## Installation

Please check [installation](docs/installation.md) for installation and [data_preparation](docs/data_preparation.md) for
preparing the nuScenes dataset.

[//]: # (* As part of this code release we have installed this software and run the training and evaluation scripts on a new AWS)

[//]: # (instance to verify the installation process described below.)

## Getting Started

Please check [getting_started](docs/getting_started.md) for training, evaluation, and visualization of neural_map_prior.

## Architecture

![visualization](figs/arch.png "Results on nuScenes")

## Acknowledgements

We would like to thank all who contributed to the open-source projects listed below. Our project would be impossible to
get done without the inspiration of these outstanding researchers and developers.

* BEV
  Perception: [BEVFormer](https://github.com/fundamentalvision/BEVFormer), [Lift, Splat, Shoot](https://github.com/nv-tlabs/lift-splat-shoot)
* HD Map
  Learning: [HDMapNet](https://github.com/Tsinghua-MARS-Lab/HDMapNet), [VectorMapNet](https://github.com/Mrmoore98/VectorMapNet_code/tree/mian)
* Vision Transformer: [Swin Transformer](https://github.com/microsoft/Swin-Transformer)
* [open-mmlab](https://github.com/open-mmlab)

The designate `project/neural_map_prior` as a module is inspired by the implementations
of [DETR3D](https://github.com/WangYueFt/detr3d).

## Citation

Please consider citing our paper in your publications if it helps your research.

```
@inproceedings{xiong2023neuralmapprior,
  author  = {Xiong, Xuan and Liu, Yicheng and Yuan, Tianyuan and Wang, Yue and Wang, Yilun and Zhao Hang},
  title   = {Neural Map Prior for Autonomous Driving},
  journal = {Proceedings of the IEEE/CVF International Conference on Computer Vision (CVPR)},
  year    = {2023}
}
```

## License

This project is released under the Apache 2.0 license - see the [LICENSE](LICENSE) file for details.

