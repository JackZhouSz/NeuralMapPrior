# Getting started with Neural Map Prior

## Training

Neural map prior incorporates BEVFormer with ResNet101 backbone as the baseline, using the weight initialization from
the ckpts/r101_dcn_fcos3d_pretrain.pth files. It can be downloaded from [here]().

### Multi-GPU training

To train neural_map_prior with 8 GPUs, run:

```bash
bash tools/dist_train.sh $CONFIG 8
```

### Single GPU training

```bash
python tools/train.py $CONFIG
```

## Evaluation

### Multi-GPU evaluation

To evaluate neural_map_prior with 8 GPU, run:

```bash
bash tools/dist_test.sh $YOUR_CONFIG $YOUR_CKPT 8 --eval iou
```

### Single GPU evaluation

```bash
python tools/test.py $YOUR_CONFIG $YOUR_CKPT --eval iou
```

## Visualization

To visualize the predictions, run:

```bash
python project/neural_map_prior/map_tiles/lane_render.py
```
