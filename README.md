## Rural road extraction from remote sensing images based on multi-view contextual information and multi-stage features

## Introduction

The following samples present challenges in the extraction of rural roads from remote sensing images.:

![Introduction](/Image/image.png)

## Dataset

- Supported Remote Sensing Datasets
  - [DeepGlobe Roads Dataset](https://www.kaggle.com/datasets/balraj98/deepglobe-road-extraction-dataset) 
  - [Massachusetts Road Dataset](https://www.cs.toronto.edu/~vmnih/data/)
  - More datasets will be supported in the future.

## Overview framework of UMFormer

We aim to design a precise semantic segmentation network for remote sensing images. Inspired by the self-attention mechanism and Mamba, we propose UMFormer, a network that fuses these two techniques within an encoder-decoder framework to address the aforementioned challenges. UMFormer combines the respective advantages of CNN, self-attention mechanism and Mamba to create a hybrid network effectively.

![Overview Framework of UMFormer](/Image/CRRENet.jpg)


## Comparison of network parameters

In the context of remote sensing image semantic segmentation, the parameter size, complexity and speed of the network are also crucial evaluation indicators. In response, a comparison is made between UMFormer and efficient semantic segmentation networks, including the number of model parameters (M), the floating point operation count (FLOPs) and the frames per second (FPS).

![Comparison of network parameters](/Image/Comparison-of-network-parameters.jpg)

## Numerical results
|   Method   |  Dataset  |  F1  |  OA  | mIoU |
|:----------:|:---------:|:----:|:----:|-----:|
|  UMFormer  |   UAVid   | 79.3 | 85.7 | 67.7 |
|  UMFormer  | Vaihingen | 90.7 | 93.0 | 83.3 |
|  UMFormer  |  Potsdam  | 92.0 | 90.9 | 85.5 |


## Visualization

### UAVid
Visualization of the UAVid validation set. The first column represents the original images. The second column represents the ground truth. The third column represents the UNetFormer segmentation results. The fourth column represents the segmentation results of our method.
![UAVid](/Image/uavid.jpg)

### Vaihingen
Visualization of the Vaihingen validation set. The columns from left to right are: original images, ground truth, segmentation results of ABCNet, segmentation results of UNetFormer, segmentation results of Mamba-UNet, segmentation results of ours.
![UAVid](/Image/vaihingen.jpg)

### Potsdam
Visualization of the Potsdam validation set. The columns from left to right are: original images, ground truth, segmentation results of MAResU-Net, segmentation results of UNetFormer, segmentation results of Swin-UMamba, segmentation results of ours.
![UAVid](/Image/potsdam.jpg)

## Acknowledgement

Our code is based on the following previous work：  

[UNetformer](https://github.com/WangLibo1995/GeoSeg)  
[Visio Mamba](https://github.com/hustvl/Vim)  
[VM-UNet](https://github.com/JCruan519/VM-UNet/tree/main)

