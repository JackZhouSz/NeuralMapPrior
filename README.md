# Neural Map Prior for Autonomous Driving (CVPR 2023)

### [arXiv Paper](https://arxiv.org/abs/2304.08481) | [CVF Paper](https://openaccess.thecvf.com/content/CVPR2023/papers/Xiong_Neural_Map_Prior_for_Autonomous_Driving_CVPR_2023_paper.pdf) | [Webpage](https://tsinghua-mars-lab.github.io/neural_map_prior/) | [5-min video](https://www.youtube.com/watch?v=FpzxaBVw3L0)

[Xuan Xiong](), [Yicheng Liu](https://scholar.google.com.hk/citations?hl=en&user=vRmsgQUAAAAJ), [Tianyuan Yuan](), [Yue Wang](https://people.csail.mit.edu/yuewang/), [Yilun Wang](https://scholar.google.com.hk/citations?user=nUyTDosAAAAJ&hl=en/), [Hang Zhao](http://people.csail.mit.edu/hangzhao/)

## Introduction

A neural representation of HD maps to improve local map inference performance for autonomous driving.

The official implementation of the paper "Neural Map Prior for Autonomous
Driving".

## Model Zoo

## Installation

Please check [installation](docs/installation.md) for installation and [data_preparation](docs/data_preparation.md) for
preparing the nuScenes dataset.

## Getting Started

Please check [getting_started](docs/getting_started.md) for training, evaluation, and visualization of neural_map_prior.

## Architecture

![visualization](figs/arch.png "Results on nuScenes")

## Acknowledgements

This project is mainly based on the following open-sourced
projects: [open-mmlab](https://github.com/open-mmlab), [HDMapNet](https://github.com/Tsinghua-MARS-Lab/HDMapNet), [VectorMapNet](https://github.com/Mrmoore98/VectorMapNet_code/tree/mian).

The designate `project/nmp` as a module is inspired by the implementations
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

