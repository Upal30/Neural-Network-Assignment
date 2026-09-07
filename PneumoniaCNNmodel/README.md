# Pneumonia Detection using CNN (Chest X-Ray Classification)

## Overview

This project focuses on developing a deep learning model to classify chest X-ray images into two categories:

- NORMAL
- PNEUMONIA

The objective is to build a Convolutional Neural Network (CNN)-based medical image classification system that can automatically identify pneumonia from chest X-ray images.

A transfer learning approach using MobileNetV2 was implemented to achieve better performance and faster training.

---

## Dataset Description

The dataset contains pediatric chest X-ray images collected from clinical patients.

The images are organized into:

- Training set
- Validation set
- Testing set

Classes:

1. NORMAL
2. PNEUMONIA

Dataset contains:

- 5,863 JPEG X-Ray images
- Anterior-posterior chest X-ray views
- Two-class classification problem

---

## Project Workflow

The complete workflow followed in this project:

1. Dataset loading and exploration
2. Image preprocessing
3. Data augmentation
4. Transfer learning using MobileNetV2
5. Model training
6. Performance evaluation
7. Model saving

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Image resizing to 224 × 224 pixels
- Pixel value normalization using MobileNetV2 preprocessing
- Batch processing
- Data augmentation:

  - Random horizontal flipping
  - Random rotation
  - Random zoom

These techniques help improve model generalization and reduce overfitting.

---

## Model Architecture

The proposed model uses MobileNetV2 as the feature extraction backbone.

Architecture:

input Image
|
↓
Image Preprocessing
(Resize to 224×224 + Normalization)
|
↓
Data Augmentation
(Random Flip, Rotation, Zoom)
|
↓
MobileNetV2
(Pre-trained Image Feature Extractor)
|
↓
Global Average Pooling Layer
|
↓
Dense Layer (128 neurons)
|
↓
Dropout Layer (0.4)
|
↓
Output Layer
(Sigmoid Activation)
|
↓
Classification
NORMAL / PNEUMONIA


### Model Components:

- **MobileNetV2:** Extracts important visual features from chest X-ray images.
- **Global Average Pooling:** Reduces feature dimensions and prevents overfitting.
- **Dense Layer:** Learns complex patterns from extracted features.
- **Dropout Layer:** Improves generalization by reducing overfitting.
- **Sigmoid Output Layer:** Produces probability for binary classification.

The final model predicts whether a chest X-ray image belongs to:

- **NORMAL**
- **PNEUMONIA**
