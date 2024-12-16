---
title: "Level-1 ADAS"
collection: projects
category: projects
permalink: /project/Level-1-ADAS
excerpt: 'Level-1 Advanced Driver Assistance System'
date: 2023-10-01
des : 2023 , Pouya Fanavaran Kosar - SAIPA CO.

---


## 1. Introduction

<div style="text-align: justify;">
This project was conducted in collaboration with PFK, a leading knowledge-based enterprise, and SAIPA, the largest automobile manufacturer in Iran. The goal was to develop the country’s first Level-1 Advanced Driver Assistance System (ADAS). As a research-based initiative, the project emphasized enhancing road and vehicle safety through the integration of several key features, including Forward Collision Warning (FCW), Lane Departure Warning (LDW), and High Beam Assistance (HBA). This marked SAIPA's first entry into ADAS technology and represented a significant milestone for Iran's automotive industry.
</div>

<div style="text-align: justify;">
The system successfully passed testing scenarios, achieving high-performance marks. This report outlines the design and development of the system, with a particular focus on my contributions to the CNN-based classification and decision-making algorithms for High Beam Assistance (HBA), as well as the DeepStream-based vehicle and pedestrian detection for Forward Collision Warning (FCW). Additionally, it discusses the challenges encountered during the project and the innovative solutions that were implemented to address them.
</div>

## 2. System Overview

### 2.1 High Beam Assist (HBA)

<div style="text-align: justify;">
The HBA system improves night-driving safety by automatically managing the vehicle's high beams.
</div>

<div style="text-align: justify;">
- **Goal**: To classify lights into three categories:
  1. Vehicle front lights
  2. Vehicle rear lights
  3. Road lights and random light reflections
</div>

<div style="text-align: justify;">
- **Implementation**: A custom Convolutional Neural Network (CNN) model was developed for light classification and optimized for real-time inference on NVIDIA Jetson Nano hardware.
</div>

### 2.2 Forward Collision Warning (FCW)

<div style="text-align: justify;">
The FCW system alerts drivers to potential collisions by detecting vehicles in real time.
</div>

<div style="text-align: justify;">
- **Goal**: To achieve reliable vehicle detection with a frame rate exceeding 15 FPS on Jetson Nano.
- **Implementation**: NVIDIA's DeepStream library was used to deploy a pre-trained TrafficCamNet model, which performed well without requiring additional re-training.
</div>

<div style="text-align: justify;">
Both systems were designed to balance accuracy, speed, and hardware efficiency, making them suitable for practical, real-time applications.
</div>

## 3. Methodology

### 3.1 High Beam Assist (HBA)

#### Dataset Creation and Annotation

<div style="text-align: justify;">
- A custom dataset was created due to the lack of pre-existing datasets for this application.
- Using the CVAT annotation tool, objects like streetlights, traffic signs, and vehicle lights were labeled. This dataset was tailored to local driving conditions.
</div>

#### CNN Architecture and Training

<div style="text-align: justify;">
- The CNN model consisted of multiple convolutional layers, optimized for classification accuracy and real-time inference.
- The training process included:
  - **Preprocessing**: Resizing and normalizing images for model input.
  - **Optimization**: Techniques like model pruning and quantization were applied to reduce the model's size and

<img src="/images/hba-1.jpg" alt="HBA" style="width: 95%; height: auto; display: block; margin: 0 auto;">

<img src="/images/hba-7.PNG" alt="HBA" style="width: 95%; height: auto; display: block; margin: 0 auto;">





