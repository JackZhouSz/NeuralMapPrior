Modified from the official
mmdet3d [getting_started.md](https://github.com/open-mmlab/mmdetection3d/blob/master/docs/en/getting_started.md).

# Prerequisites

NeuralMapPrior is developed with the following version of modules.

- Linux or macOS (Windows is not currently officially supported)
- Python 3.8.13
- PyTorch 1.9.0+cu111
- CUDA 11.2
- GCC 7.3.0
- MMCV==1.3.14
- MMDetection==2.14.0
- MMSegmentation==0.14.1
- MMDetection3D==0.17.2

# Installation

**a. Create a conda virtual environment and activate it.**

```shell
conda create --name npn python=3.8 -y
conda activate npn
```

**b. Install PyTorch and torchvision following the [official instructions](https://pytorch.org/).**

```shell
pip install torch==1.9.0+cu111 torchvision==0.10.0+cu111 -f https://download.pytorch.org/whl/torch_stable.html
```

**c. Clone the neural_map_prior repository.**

```shell
git clone --recursive git@github.com:Tsinghua-MARS-Lab/neural_map_prior.git
cd neural_map_prior
```

**d.
Install [MMCV](https://mmcv.readthedocs.io/en/latest/), [MMDetection](https://github.com/open-mmlab/mmdetection), [MMSegmentation](https://github.com/open-mmlab/mmsegmentation),
and other requirements.**

```shell
pip install -r requirements.txt
```

**d. Install [MMDetection3D](https://github.com/open-mmlab/mmdetection3d).**

```shell
cd neural_map_prior/mmdetection3d
python setup.py develop
```


