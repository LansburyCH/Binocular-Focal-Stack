# Binocular-Focal-Stack
### [Download Dataset](https://drive.google.com/file/d/1-VrIrWSKtJbEVhFFGJ3Nu608D0jnPJH8/view)
This repository contains the binocular focal stack dataset in the paper: [Deep eyes: Joint depth inference using monocular and
binocular cues](https://www.sciencedirect.com/science/article/pii/S0925231220313746). The dataset is generated based on [FlyingThings3D](https://lmb.informatik.uni-freiburg.de/resources/datasets/SceneFlowDatasets.en.html#downloads).<br><br>

## Data Layout
```
binocular_focal_stack_clean/
    train/                                                # Training scenes
        [scene_id]_[focal_slice_id]_[L/R]_image.png           # Image for a focal slice
    test/                                                 # Testing scenes (same layout as ./train/)
binocular_focal_stack_noise/
    train/                                                # Training scenes
        [scene_id]_[focal_slice_id]_[L/R]_image.png           # Image for a focal slice, with Poisson noise added
    test/                                                 # Testing scenes (same layout as ./train/)
color_depth_pair/
    train/                                                # Training scenes
        [scene_id]_color_[L/R].png                            # All-focus color image
        [scene_id]_depth_[L/R].png                            # GT disparity image
    test/                                                 # Testing scenes (same layout as ./train/)
```
For the disparity images, an intensity of ```255``` corresponds to a disparity of ```100``` pixels.

## Citation
If you find our dataset or paper useful, please consider citing:
```
@article{chen2020deep,
  title={Deep eyes: Joint depth inference using monocular and binocular cues},
  author={Chen, Zhang and Guo, Xinqing and Li, Siyuan and Yang, Yang and Yu, Jingyi},
  journal={Neurocomputing},
  year={2020},
  publisher={Elsevier}
}
```
