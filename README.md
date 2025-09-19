# Neural Radiant Field (NeRF) and relative researches

1. [NeRF: representing scenes as neural radiance fields for view synthesis](https://arxiv.org/abs/2003.08934)
, 2021
Orignial paper that propose 3D scene rendering using neural network to learn radiant field

2. [FastNeRF: High-Fidelity Neural Rendering at 200FPS](https://openaccess.thecvf.com/content/ICCV2021/html/Garbin_FastNeRF_High-Fidelity_Neural_Rendering_at_200FPS_ICCV_2021_paper.html), 2021
To accelerate the reduce the size of MLP, it factorized the orginal NeRF to NeRF_pos, NeRF_dir and then use cache to accelrate the rendering time in testing mode.

3. [NeRF--: Neural Radiance Fields Without Known Camera Parameters](https://nerfmm.active.vision/),2021
This paper show joinoptimization between three MLP: mlp camera focal lens, mlp camera pos, mlp nerf. This algorithm doesn't need COLMAP or other algorithms to estimate camera parameters (intrinsics and 6DoF poses). 

4. [Instant Neural Graphics Primitives with a Multiresolution Hash Encoding](https://arxiv.org/abs/2201.05989),2022
It reduce the size of MLP significantly by encoding the 5D input into hash table. The elements in the hash table represent s the features in multiple resolutions and therefore, the rendering can be much faster while we train these features.

5.

6

## Usage

**Dataset:** [Download the training and testing datasets](https://drive.google.com/drive/folders/1eO7DXFhWWpauC-9LDhOimtIKxY3yRCIm?usp=sharing).

```commandline
$ pip3 install -r requirements.txt
$ python3 ngp.py
```

## Results

#### Novel views rendered from the optimized model

 ![](novel_views/img_0.png)              |  ![](novel_views/img_60.png) 
:-------------------------:|:-------------------------:
![](novel_views/img_120.png)  |  ![](novel_views/img_180.png)


## What is not implemented

- Ray marching
- Occupancy grid