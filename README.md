

# JumpingGS
JumpingGS: Level-jump 3D Gaussian Representation for Delicate Textures in Aerial Large-scale Scene Rendering

![figure1](https://github.com/hoodpy/JumpingGS/blob/main/static/image0.png)

## Source data, code, trained model

If you require the data, code, and trained model (56GB in total), please contact me via email: jiongming@whu.edu.cn

All data is available for free use. Please indicate your organization or college in your email. The compressed file "large_scale_undistorted_photos.zip" needs to be unzipped and placed in v32/data.

The six aerial scenes in the paper were retrained to obtain the models we uploaded. Performance metrics are summarized below.

| Scene  | PSNR | SSIM | LPIPS | Scene  | PSNR | SSIM | LPIPS |
| ------ | ---- | ---- | ----- | ------ | ---- | ---- | ----- |
| Building | 26.60 | 0.8522 | 0.0983 | Rubble | 29.44 | 0.8592 | 0.1086 |
| Residence | 26.16 | 0.8576 | 0.1181 | Sciart | 29.96 | 0.9030 | 0.0931 |
| Campus | 26.72 | 0.8214 | 0.1646 | Matrixcity | 30.02 | 0.8938 | 0.0871 |

## Set up

require cuda 11.8

    cd v32
    conda create -n jumpinggs python==3.11.7
    conda activate jumpinggs
    python -m pip install --upgrade pip
    pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cu118
    pip install submodules/diff-gaussian-rasterization --no-build-isolation
    pip install submodules/simple-knn --no-build-isolation
    pip install ConfigArgParse
    pip install einops
    pip install matplotlib
    pip install open3d
    pip install opencv-python
    pip install plyfile
    pip install scipy
    pip install tensorboardX
    pip install torch_scatter
    pip install tqdm
    pip install scikit-image
    pip install scikit-learn
    pip install lpips
    pip install numpy==1.26.0

## Comparison in Mill-19 scenes
![figure2](https://github.com/hoodpy/JumpingGS/blob/main/static/image1.png)

## Comparison in Urban3D scenes
![figure3](https://github.com/hoodpy/JumpingGS/blob/main/static/image2.png)

## Comparison in MatrixCity
![figure4](https://github.com/hoodpy/JumpingGS/blob/main/static/image3.png)

## BibTeX
@article{10.1145/3763347,<br>
author = {Qin, Jiongming and Zhou, Kaixuan and Jiang, Yu and Zhu, Huizhi and Luo, Fei and Xiao, Chunxia},<br>
title = {JumpingGS: Level-jump 3D Gaussian Representation for Delicate Textures in Aerial Large-scale Scene Rendering},<br>
year = {2025},<br>
issue_date = {December 2025},<br>
publisher = {Association for Computing Machinery},<br>
address = {New York, NY, USA},<br>
volume = {44},<br>
number = {6},<br>
issn = {0730-0301},<br>
url = {https://doi.org/10.1145/3763347},<br>
doi = {10.1145/3763347},<br>
journal = {ACM Trans. Graph.},<br>
month = dec,<br>
articleno = {273},<br>
numpages = {15}}
