# **Beneath The Surface: Enhancing Scene Perception through Unified Semantic Segmentation and Depth Estimation**

A multi-task learning framework that integrates depth estimation, semantic segmentation, and edge detection, leveraging the **MTI-Net** architecture and the **NYU Depth V2 Dataset**.

---

## **Table of Contents**

1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Dataset](#dataset)  
4. [Installation](#installation)  

---

## **Introduction**

This project aims to enhance scene perception through a unified multi-task learning framework that improves depth boundary sharpness, segmentation consistency, and computational efficiency. The approach combines guided attention mechanisms and structured loss functions for depth estimation, semantic segmentation, and edge detection.

---

## **Features**

- **Multi-Task Learning (MTL):** Joint training for depth estimation, semantic segmentation, and edge detection.  
- **MTI-Net Backbone:** Enhanced task interaction layers for improved prediction quality.  
- **Structured Depth Loss:** A novel loss function balancing sharpness and smoothness.  
- **Guided Attention Mechanisms:** Cross-task guidance for boundary clarity.  
- **Efficient Training:** Optimized for computational efficiency with shared representations.  

---

## **Dataset**

The project uses the **NYU Depth V2 Dataset**, a benchmark dataset for indoor scene understanding with:  
- **1,449 RGB-D images** with dense depth maps.  
- **40 semantic categories** for pixel-wise segmentation.  
- Captured in diverse indoor environments using Microsoft Kinect.

**Preprocessing steps include:**  
- Resizing images to `256x256`.  
- Normalization of RGB images and depth maps.  
- Data augmentation with random flipping, cropping, and color jittering.  

---

## **Installation**

### **Prerequisites**
- Python 3.8 or higher  
- PyTorch 1.12 or higher  
- NVIDIA CUDA for GPU acceleration (optional)  

### **Setup**
1. Place the provided Jupyter Notebook file in a working directory of your choice.  
2. Dataset shoul be available in the folder `nyu-organised`, if not download the preprocessed dataset from [Google Drive](https://drive.google.com/drive/folders/186uoCtSf38EpnrUD7glfHV7WC-DXqpXW?usp=drive_link) and place it in the same directory as the notebook.  
   - **If the link is unavailable** or you wish to reproduce the preprocessing steps, download the `nyu_depth_v2_labeled.mat` file from [NYU Depth V2 Dataset](http://horatio.cs.nyu.edu/mit/silberman/nyu_depth_v2/nyu_depth_v2_labeled.mat) and place it in the working directory.  
3. If preprocisng the `.mat` file, run the selected cells in the notebook under the **Pre-Processing Section**:  
   - **First cell:** For just preprocessing the dataset.  
   - **Second cell:** If you want to include a train-test split in addition to preprocessing.  
4. Once preprocessing is complete, ensure that the `nyu-organised` subdirectory is present and complete. This subdirectory will contain the organized dataset.  
5. Execute the notebook sections in the following order:  
   - **Model Training**  
   - **Visual Results**  
   - **Testing**  

Each section is designed to be executed with a single command for convenience.  

---
