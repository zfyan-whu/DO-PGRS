# OD-RSPG: Object Detection in Remote Sensing Data for Power Grid Inspection, A Survey and Benchmark

OD-RSPG is a public dataset which is a collection of Unmanned Aerial Vehicle (UAV) and satellte imagery images on
power grids. This is the official repository of paper [OD-RSPG: Object Detection in Remote Sensing Data for Power Grid Inspection, A Survey and Benchmark]


## 🔭 Introduction
The repository includes:
* The original images of OD-RSPG dataset with rich annotation in COCO format. The dataset images here: https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1Yz59yXCiPKS0_X4K3x9mW22NLnxjvrr0.
* Weights of training models based on different detectors.

## 🔭 Introduction

<p align="center">
  <img src="pic/overview.png" alt="Network" width="80%">
</p>
<p align="justify">
OD-RSPG dataset comprises UAV oblique imagery and satellite imagery captured along multiple transmission lines, spanning voltage levels from 110 kV to 500 kV. It includes six categories of power components and one category of external object, totaling 2,411 images and 27,082 instances.
</p>

## Evaluation on the OD-PGRS (UAV).

|Dectors| weights|
|:-------------:| -----:|      
|YOLOv5s | [yolact_img640_secondval_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1arVhEIz_DQ-1wALSk9S3TJwCFzOWPNik)|
|YOLOv7 | [yolact_img550_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1mKYRP7LOVgrFN5Vsug-tyI6XDEZ8c62k) |
|RT-DETR | [yolact_img700_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1y8g-KepFdcSBWKRdHTHB8vygjKsFTyKr) |
|Dynamic R-CNN | [yolact_img700_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1y8g-KepFdcSBWKRdHTHB8vygjKsFTyKr) |
others will come soon...

## Evaluation on the OD-PGRS (Satellite).
|Dectors| weights|
|:-------------:| ------------- |:-------------:| -----:|      
|S2ANet | [yolact_img640_secondval_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1arVhEIz_DQ-1wALSk9S3TJwCFzOWPNik)|
|ConvNext  | [yolact_img550_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1mKYRP7LOVgrFN5Vsug-tyI6XDEZ8c62k) |
|LCKNet | [yolact_img700_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1y8g-KepFdcSBWKRdHTHB8vygjKsFTyKr) |
others will come soon...

## Results:
Average Precision for Different Deep Learning Models on the OD-PGRS dataset is reported in the following table

## Contact:
For questions about our paper or code, please contact zhengfeiyan@whu.edu.cn.

## 🔗 Acknowledgments
We sincerely thank the excellent projects:
- [ultralytics](https://github.com/ultralytics/ultralytics) 
- [ikd-Tree](https://github.com/hku-mars/ikd-Tree) for point cloud map management;
- [GTSAM](https://github.com/borglab/gtsam) for IMU pre-integration and factor graph optimization;
- [Ceres](https://github.com/ceres-solver/ceres-solver) for auto-diff.
- [Sopuhs](https://github.com/strasdat/Sophus)
- [PCL](https://github.com/PointCloudLibrary/pcl)
- [A-LOAM](https://github.com/HKUST-Aerial-Robotics/A-LOAM)
