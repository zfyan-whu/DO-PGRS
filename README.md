# OD-RSPG: Object Detection in Remote Sensing Data for Power Grid Inspection, A Survey and Benchmark

OD-RSPG is a public dataset which is a collection of Unmanned Aerial Vehicle (UAV) and satellte imagery images on
power grids. This is the official repository of paper [OD-RSPG: Object Detection in Remote Sensing Data for Power Grid Inspection, A Survey and Benchmark]


## 🔭 Introduction
The repository includes:
* The original images of OD-RSPG dataset with rich annotation in COCO format. [The dataset images here](comming soon...).
* Weights of training models based on different detectors.

## 🔭 Introduction

<p align="center">
  <img src="pic/overview.png" alt="Network" width="80%">
</p>
<p align="justify">
<strong>Abstract:</strong> As an effective complement to common laser scanning systems, the portable laser scanning system can acquire
point clouds flexibly and quickly. Calibration between Light detection and ranging (LiDAR) sensors and inertial
measurement units (IMU) is the prerequisite for laser scanning systems to obtain high-quality point clouds.
Related methods have been proposed in the last two decades, where the global navigation satellite system (GNSS)
or high-precision calibration fields are commonly used. However, the extrinsic self-calibration of LiDAR-IMU is
challenging, due to the large distortion in single-frame point cloud caused by rapid motion and the position
errors of IMU integration which drift quickly. At the same time, the highly dynamic motion patterns of portable
devices and the changes in the scanned scene structure are not well considered in existing LiDAR odometry
methods. To take better advantage of the characteristics of non-repetitive scanning LiDAR sensor, this paper
proposes AFLI-Calib, which utilizes adaptive frame length LiDAR odometry to perform the extrinsic self-calibration
of LiDAR-IMU. <strong>Unlike LiDAR odometry methods with a fixed frame length, the LiDAR frame
length is dynamically adjusted according to the motion state of sensors and the matching stability of scenes. </strong>The
single-frame point cloud is registered to the map through a linear-based continuous-time model, eliminating the
motion distortion correction in advance. For further optimization of trajectory and extrinsic parameters, IMU raw
measurements and LiDAR observations are involved in the multi-constraint optimization, through tightly-coupled
IMU pre-integration constraints, LiDAR point-to-plane constraints, and prior constraints. The method
is fully validated using self-collected calibration data of indoor and outdoor scenes and different motion modes.
Experiments show that on the test data, the translation parameter accuracy of the method is 0.041 m, which is
56.3% higher than the state-of-the-art method. The standard deviation is significantly reduced, with translation
deviation (0.017 m, 0.024 m, 0.022 m) and rotation deviation (0.17◦, 0.25◦, 0.15◦), which verifies the robustness
of our method. The average RMSE of distances to the reference point cloud acquired by the terrestrial laser
scanning system (TLS) is 0.042 m, showing a high accuracy calibration result. Comparative experiments with the
fixed frame length LiDAR odometry method and classical “correction-then-registration” motion distortion model
further verify the superiority and effectiveness of the proposed adaptive frame length LiDAR odometry.
</p>

## Evaluation:

|Image Size| Backbone|configs| weights|
|:-------------:| ------------- |:-------------:| -----:|      
|640 x 360 |Resnet50 | [config_img640_resnet50_aspect.py](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1ocoYiTDFBcdI8Es8dZlMbsbFGkaLKw98)| [yolact_img640_secondval_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1arVhEIz_DQ-1wALSk9S3TJwCFzOWPNik)|
|550 x 550 |Resnet50 | [config_img550_resnet50.py](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1buxmIli7cxiFwJ7krOCTOojwgDeR2AUM)   | [yolact_img550_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1mKYRP7LOVgrFN5Vsug-tyI6XDEZ8c62k) |
|700 x 700|Resnet50 | [config_img700_resnet50.py](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1NCe8W7QKlDhDF-nrH2iLAr0kiHdC6T7w)  | [yolact_img700_399_30000_resnet50.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1y8g-KepFdcSBWKRdHTHB8vygjKsFTyKr) |
|640 x 360 |Resnet101| [config_img640_resnet101_aspect.py](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1sq3WSdH-wqRLbIaZO9g4uBYA6WQec3uC)| [yolact_img640_secondval_399_45100_resnet101.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1IDfQlBJ2VAIpyaOSUs2Ecmf_rsl8nSdc) |
|550 x 550 |Resnet101| [config_img550_resnet101.py](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1XM7ryEokOe98Y6XNmx9qvuK8rPujoJvL)| [yolact_img550_399_45100_resnet101_b8.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1zP4usEnaAUeGuqq179iLocy2J5TO4eJH) |
|700 x 700 |Resnet101| [config_img700_resnet101.py](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1QfPvi2FTJv1JByqM70qM7nQjGpNI_kNi)| [yolact_img700_399_45100_resnet101_b8.pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1IDfQlBJ2VAIpyaOSUs2Ecmf_rsl8nSdc)|

## Results:

Average Precision for Different Deep Learning Models on TTPLA is reported in the following table


## Contact:
For questions about our paper or code, please contact [Zhengfei Yan](zhengfeiyan@whu.edu.cn).


## 🔗 Acknowledgments
We sincerely thank the excellent projects:
- [loam_livox](https://github.com/hku-mars/loam_livox) for inspiring the idea of the adaptive frame length
- [ikd-Tree](https://github.com/hku-mars/ikd-Tree) for point cloud map management;
- [GTSAM](https://github.com/borglab/gtsam) for IMU pre-integration and factor graph optimization;
- [Ceres](https://github.com/ceres-solver/ceres-solver) for auto-diff.
- [Sopuhs](https://github.com/strasdat/Sophus)
- [PCL](https://github.com/PointCloudLibrary/pcl)
- [A-LOAM](https://github.com/HKUST-Aerial-Robotics/A-LOAM)
