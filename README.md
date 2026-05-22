# LLNVIR Dataset

**LLNVIR** is a low-light night-vision and infrared multispectral object detection dataset collected in real extremely low-light environments. It is designed to support research on weakly aligned multispectral object detection, cross-modal fusion, image registration, and robust visual perception under challenging nighttime conditions.

This dataset is introduced in our paper:

> **W-WTDet: A Weakly Aligned Multispectral Object Detection Network Guided by Wavelet Transform**

## Overview

Multispectral object detection has shown strong potential in challenging visual environments by exploiting complementary information from different sensing modalities. However, most existing visible-infrared datasets assume well-aligned image pairs and mainly focus on general low-light scenes.

In real-world heterogeneous sensor systems, especially under extremely low illumination, accurate pixel-level alignment is difficult due to sensor parallax, field-of-view differences, focal-plane inconsistency, and asynchronous acquisition. To address this gap, we construct **LLNVIR**, a weakly aligned night-vision and infrared dataset collected under extremely low-light conditions.

## Key Features

- **Extremely low-light environments**: Most scenes are captured under illumination below **0.01 lux**, with some scenes below **0.001 lux**.
- **Night-vision and infrared modalities**: Each sample contains a paired low-light night-vision image and infrared image.
- **Weakly aligned image pairs**: The dataset preserves realistic cross-modal misalignment caused by heterogeneous sensors.
- **Real-world scenarios**: Images are collected from multiple practical nighttime environments, including:
  - University campuses
  - Indoor basements
  - Urban roads
  - Forests and farmlands
- **Object detection annotations**: The dataset provides bounding-box annotations for pedestrian and vehicle detection.
- **YOLO-format labels**: Annotations are provided in standard YOLO format for easy use with mainstream object detection frameworks.

## Dataset Statistics

| Item | Description |
|---|---|
| Number of image pairs | 8,164 |
| Modalities | Low-light night vision / Infrared |
| Image resolution | 640 × 512 |
| Number of categories | 2 |
| Categories | person, car |
| Number of instances | 26,571 |
| Pedestrian instances | 15,373 |
| Vehicle instances | 11,198 |
| Annotation format | YOLO format |
| Alignment type | Weakly aligned |

## Dataset Structure

After downloading and extracting the dataset, the directory is organized as follows:

```text
LLNVIR/
├── images/
│   ├── train/
│   │   ├── night_vision/
│   │   │   ├── 000001.jpg
│   │   │   ├── 000002.jpg
│   │   │   └── ...
│   │   └── infrared/
│   │       ├── 000001.jpg
│   │       ├── 000002.jpg
│   │       └── ...
│   ├── val/
│   │   ├── night_vision/
│   │   └── infrared/
│   └── test/
│       ├── night_vision/
│       └── infrared/
│
├── labels/
│   ├── train/
│   │   ├── 000001.txt
│   │   ├── 000002.txt
│   │   └── ...
│   ├── val/
│   └── test/
│
├── ImageSets/
│   ├── train.txt
│   ├── val.txt
│   └── test.txt
│
└── README.md
