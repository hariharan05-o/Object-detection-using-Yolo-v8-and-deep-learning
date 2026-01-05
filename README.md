# Object-detection-using-Yolo-v8-and-deep-learning
Project Overview

This project implements a Real-Time Object Detection System using Deep Learning to identify and locate 20 common real-world objects from images and video streams. The system uses the YOLOv8 (You Only Look Once) object detection algorithm, which performs object localization and classification in a single forward pass, enabling high-speed and accurate detection suitable for real-time applications.

The model detects objects such as person, laptop, mobile phone, bottle, chair, car, dog, cat, and other everyday items. For each detected object, a bounding box and confidence score are displayed. The project also focuses on handling datasets with nested directory structures, making the solution robust and adaptable to real-world data formats.

Setup and Execution Steps
1. Environment Setup

Platform: Google Colab / Local Machine

Language: Python 3.x

Install required libraries:

pip install ultralytics opencv-python matplotlib

2. Dataset Preparation

Upload train.zip and test.zip to Colab

The dataset may contain nested folders

A preprocessing script recursively scans all folders, collects images and labels, and reorganizes them into YOLO-compatible format:

dataset/
├── train/
│   ├── images/
│   └── labels/
├── test/
│   ├── images/
│   └── labels/

3. Training the Model

A data.yaml file defines dataset paths and class names

YOLOv8 is trained using:

Image size: 640×640

Epochs: 20

Batch size: 16

4. Evaluation and Testing

Model performance is evaluated using Precision, Recall, F1-score, and mAP

Predictions are generated on test images and video inputs

Model and Approach Used :

Model: YOLOv8 (Ultralytics)

Framework: PyTorch

Approach:

One-stage object detection

End-to-end training and inference

Automated dataset restructuring for nested directories

Real-time inference on images and videos

YOLOv8 enables fast and accurate detection by performing classification and bounding box regression simultaneously.

Challenges Faced :

Dataset contained nested and inconsistent folder structures

YOLO requires a strict directory format

FileNotFound errors during training

Handling missing or mismatched image–label pairs

Optimizing training parameters for real-time performance

These issues were resolved by implementing a recursive dataset preprocessing pipeline.

What I Learned from This Assignment :

Fundamentals of object detection and YOLO architecture

Dataset preparation and annotation formats

Handling real-world data inconsistencies

Training and evaluating deep learning models

Understanding evaluation metrics like Precision, Recall, and mAP

Building scalable and real-time computer vision systems

Conclusion :

This project successfully demonstrates a real-time object detection system using YOLOv8. It combines robust dataset preprocessing, deep learning-based training, and efficient inference, making it suitable for real-world applications such as surveillance, smart monitoring, and intelligent video analytics.

