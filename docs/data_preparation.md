# Dataset Preparation

## Dataset structure

It is recommended to symlink the dataset root to `$neural_map_prior/data/nuscenes`, `$neural_map_prior` means the repo
root. If your folder structure is different from the following, you may need to change the corresponding paths in config
files.

```
neural_map_prior
├── mmdet3d
├── tools
├── projects
│   ├── nmp
│   ├── configs
├── data
│   ├── nuscenes
│   │   ├── maps
│   │   ├── samples <-- key frames
│   │   ├── sweeps  <-- frames without annotation
│   │   ├── v1.0-test <-- metadata
|   |   ├── v1.0-trainval <-- metadata and annotations
│   │   ├── nuScences_map_trainval_infos_train.pkl <-- train annotations
│   │   ├── nuScences_map_trainval_infos_val.pkl <-- val annotations
```

## Download and prepare the nuScenes dataset

Download nuScenes V1.0 full dataset data [HERE](https://www.nuscenes.org/download), including the map extensions. Data
creation should be under the GPU environment.
Prepare nuscenes data by running

```bash
#python tools/create_data.py nuscenes --root-path ./data/nuscenes --out-dir ./data/nuscenes --extra-tag nuscenes
python tools/data_converter/nuscenes_converter.py --data-root your/dataset/nuScenes/
```

You can either use our provided
files [nuScences_map_trainval_infos_train.pkl](https://drive.google.com/file/d/18P8LZcEVxGYAvMQpEROrF0pnpu62ffvD/view?usp=drive_link)
and [nuScences_map_trainval_infos_val.pkl](https://drive.google.com/file/d/1H6HfnNqmKBFvNIivApcsRUCgPtxgIq7A/view?usp=drive_link).
Copy the infos file into `$neural_map_prior/data/nuscenes/`.