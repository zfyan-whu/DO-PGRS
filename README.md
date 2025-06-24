# Official github repository DO-PGRS

DO-PGRS is a public dataset which is a collection of images on power grids. This is the official repository of the paper and dataset


## Download
The repository includes:
* The original images of DO-PGRS dataset with rich annotation in COCO format. The dataset images here: https://drive.google.com/drive/folders/1JtFw5H_gaHoUG_18BoJSk7s1KJ46BWYx?usp=drive_link
* Weights of training models based on different detectors.

## 🔭 Introduction

<p align="center">
  <img src="Figures/Overview.png" alt="Network" width="100%">
</p>
<p align="justify">
DO-PGRS is an open source data platform that includes a large amount of multi-source inspection data.
</p>

## Evaluation on the DO-PGRS (UAV).

|Dectors| weights|
|:-----:|-----:|      
|YOLOv7 | [YOLOv7.pth](https://drive.google.com/file/d/104TyTCVwBWVvNhCpb6wuBRtEcZRjPze6/view?usp=drive_link)|
|YOLOv8 | [YOLOv8.pth](https://drive.google.com/file/d/1Fb7LV-C84TPSbvm87z3EBqGyVSlB0BoN/view?usp=drive_link) |
|RT-DETR | [RT-DETR.pth](https://drive.google.com/file/d/1cEZPSU9PJkvqpZPSIs7WV7EXDQb75Ibp/view?usp=drive_link) 

others will come soon...

## Evaluation on the DO-PGRS (Satellite).
|Dectors| weights|
|:-----:|-----:|  
|Faster R-CNN (Swin-T) | [Faster R-CNN(Swin-T).pth](https://drive.google.com/uc?export=download&confirm=no_antivirus&id=1arVhEIz_DQ-1wALSk9S3TJwCFzOWPNik)|

others will come soon，ConvNext,LCKNet...

## Results:
Average Precision for Different Deep Learning Models on the DO-PGRS dataset is reported in the following table
<p align="center">
  <img src="Figures/Quantitative evaluation on the OD-PGRS (UAV).png" alt="Network" width="100%">
</p>
<p align="justify">
  
<p align="center">
  <img src="Figures/Visualization.png" alt="Network" width="80%">
</p>
<p align="justify">


## Contact:
For questions about our paper or code, please contact zhengfeiyan@whu.edu.cn.

## 🔗 Acknowledgments
We sincerely thank the excellent projects:
- [ultralytics](https://github.com/ultralytics/ultralytics);
- [Swin-Transformer](https://github.com/microsoft/Swin-Transformer);
- [mmdetection](https://github.com/microsoft/Swin-Transformer).
