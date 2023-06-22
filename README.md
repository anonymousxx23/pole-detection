### Introduction
This repository presents a new dataset benchmark in the field of electricity. We present a comprehensive novel object detection dataset. The dataset comprises of various components of electrical poles, including cable, post, insulator, harrow, lightning, transformer, and IACM 
### Environment
- Python 3.10
- Pytorch 2.0
  - We carry out all experiments with an NVIDIA T40 GPU on Google Colab.
### Pole dataset
  - Class Balance
<img width="984" alt="image" src="https://github.com/anonymousxx23/pole-detection/assets/135847537/eb8074d1-4cc3-4c97-ae28-5d3702dcb354">

  - Dimension Insights
<img width="820" alt="image" src="https://github.com/anonymousxx23/pole-detection/assets/135847537/9766ea74-9b34-42c5-ac6f-b76330118d10">

  - Annotation Heatmap
<img width="418" alt="image" src="https://github.com/anonymousxx23/pole-detection/assets/135847537/7efd0789-2d13-4e7a-943d-56b6890d4c61">

  - Histogram of object
<img width="478" alt="image" src="https://github.com/anonymousxx23/pole-detection/assets/135847537/9c4b5bf7-889a-468d-88fd-8214813a9cc5">

  - Object Statistics
<img width="301" alt="image" src="https://github.com/anonymousxx23/pole-detection/assets/135847537/23eca2f9-3b37-4d75-a958-5576fa8b9e45">

  - You can access to the dataset by using this link below https://drive.google.com/drive/folders/19Xkiff4YVUQi-X_PaQ9_27lny9MBAaN2
### Usage

### Experiment result for YOLO-V8
| Resizing | Data Augmentation | Epochs | Batch size  | mAP | Time |
| ----- | ----- | ----- |----- |----- |----- | 
| None | None | 20 | 16 |0.699 | 30m0s |
| 640 | 90 degree rotate(x2) | 15 | 32 |0.662 | 4m48s |
| 640 | 90 degree rotate(x2) | 15 | 16 |0.659 | 7m14s |
### Experiment result for DETR
| Resizing | Data Augmentation | Epochs | Batch size  | mAP | Time |
| ----- | ----- | ----- |----- |----- |----- | 
| No | 90 degree rotate(x2) | 10 | 4 |0.162 | 60m0s |
| 640 | 90 degree rotate(x2) | 10 | 8 |0.108 | 25m0s |
| 840 | 90 degree rotate(x2) + Crop(x2) | 15 | 4 |0.156 | 23m2s |

### Experiment result for YOLO-NAS
| Resizing | Data Augmentation | Epochs | Batch size  | mAP | Time |
| ----- | ----- | ----- |----- |----- |----- | 
| None | 90 degree rotate(x2) + Flip(x2) | 20 | 4 |0.700 | 50m0s |
| 840 | 90 degree rotate(x2) + Crop(x2) | 20 | 8 |0.648 | 45m0s |
| 840 | No | 30 | 8 |0.467 | 40m01s |

### TODO

