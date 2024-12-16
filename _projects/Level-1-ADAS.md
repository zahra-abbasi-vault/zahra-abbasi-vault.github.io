---
title: "Level-1 ADAS"
collection: projects
category: projects
permalink: /project/Level-1-ADAS
excerpt: 'Level-1 Advanced Driver Assistance System'
date: 2023-10-01
des : 2023 , Pouya Fanavaran Kosar - SAIPA CO.

---

# Work Sample 1: Level-1 ADAS Project

## 1. Introduction

<p style="text-align: justify;">This project was conducted in collaboration with PFK, a leading knowledge-based enterprise, and SAIPA, the largest automobile manufacturer in Iran. The goal was to develop the country’s first Level-1 Advanced Driver Assistance System (ADAS). As a research-based initiative, the project emphasized enhancing road and vehicle safety through the integration of several key features, including Forward Collision Warning (FCW), Lane Departure Warning (LDW), and High Beam Assistance (HBA). This marked SAIPA's first entry into ADAS technology and represented a significant milestone for Iran's automotive industry.</p>

<p style="text-align: justify;">The system successfully passed testing scenarios, achieving high-performance marks. This report outlines the design and development of the system, with a particular focus on my contributions to the CNN-based classification and decision-making algorithms for High Beam Assistance (HBA), as well as the DeepStream-based vehicle and pedestrian detection for Forward Collision Warning (FCW). Additionally, it discusses the challenges encountered during the project and the innovative solutions that were implemented to address them.</p>

## 2. System Overview

### 2.1 High Beam Assist (HBA)

<p style="text-align: justify;">The HBA system improves night-driving safety by automatically managing the vehicle's high beams.</p>

- <p style="text-align: justify;"><strong>Goal</strong>: To classify lights into three categories:
  1. Vehicle front lights
  2. Vehicle rear lights
  3. Road lights and random light reflections</p>

- <p style="text-align: justify;"><strong>Implementation</strong>: A custom Convolutional Neural Network (CNN) model was developed for light classification and optimized for real-time inference on NVIDIA Jetson Nano hardware.</p>

### 2.2 Forward Collision Warning (FCW)

<p style="text-align: justify;">The FCW system alerts drivers to potential collisions by detecting vehicles in real time.</p>

- <p style="text-align: justify;"><strong>Goal</strong>: To achieve reliable vehicle detection with a frame rate exceeding 15 FPS on Jetson Nano.</p>
- <p style="text-align: justify;"><strong>Implementation</strong>: NVIDIA's DeepStream library was used to deploy a pre-trained TrafficCamNet model, which performed well without requiring additional re-training.</p>

<p style="text-align: justify;">Both systems were designed to balance accuracy, speed, and hardware efficiency, making them suitable for practical, real-time applications.</p>

## 3. Methodology

### 3.1 High Beam Assist (HBA)

#### Dataset Creation and Annotation

<p style="text-align: justify;">A custom dataset was created due to the lack of pre-existing datasets for this application. Using the CVAT annotation tool, objects like streetlights, traffic signs, and vehicle lights were labeled. This dataset was tailored to local driving conditions.</p>

#### CNN Architecture and Training

<p style="text-align: justify;">The CNN model consisted of multiple convolutional layers, optimized for classification accuracy and real-time inference.</p>
  
- <p style="text-align: justify;"><strong>Preprocessing</strong>: Resizing and normalizing images for model input.</p>
- <p style="text-align: justify;"><strong>Optimization</strong>: Techniques like model pruning and quantization were applied to reduce the model's size and inference time.</p>

<p style="text-align: justify;">The final model met the performance requirements of Jetson Nano, achieving high accuracy in light classification.</p>

### 3.2 Forward Collision Warning (FCW)

#### Vehicle Detection with DeepStream

<p style="text-align: justify;">NVIDIA's DeepStream SDK was used to deploy the TrafficCamNet model on Jetson Nano. The model achieved over 15 FPS, meeting the real-time requirements for FCW. No transfer learning or re-training was needed, as the pre-trained model effectively detected Iranian vehicles as well as the other models.</p>

#### System Integration

<p style="text-align: justify;">The FCW system was integrated with Jetson Nano, ensuring seamless processing of video streams with minimal computational overhead.</p>

## 4. Results and Evaluation

### 4.1 High Beam Assist (HBA)

- <p style="text-align: justify;"><strong>Accuracy</strong>: The CNN-based light classification model achieved an accuracy of over 93% in distinguishing between light categories.</p>
- <p style="text-align: justify;"><strong>Performance</strong>: The optimized model ran smoothly on Jetson Nano, meeting real-time inference requirements.</p>

### 4.2 Forward Collision Warning (FCW)

- <p style="text-align: justify;"><strong>Detection Speed</strong>: The TrafficCamNet model processed video streams at over 15 FPS on Jetson Nano.</p>
- <p style="text-align: justify;"><strong>Robustness</strong>: The model demonstrated consistent performance, effectively detecting vehicles in various scenarios, including local traffic conditions.</p>

## 5. Challenges and Solutions

### 5.1 Hardware Constraints

<p style="text-align: justify;"><strong>Challenge</strong>: The limited computational power of Jetson Nano.</p>
<p style="text-align: justify;"><strong>Solution</strong>: Optimized the CNN model size and inference time for HBA using techniques like pruning and quantization. Utilized the lightweight and efficient TrafficCamNet model for FCW.</p>

### 5.2 Dataset Availability

<p style="text-align: justify;"><strong>Challenge</strong>: Lack of suitable datasets for HBA.</p>
<p style="text-align: justify;"><strong>Solution</strong>: Created a custom dataset by placing the camera in the car and recording data while driving over 3 thousand kilometers at night and using multiple road types. Then, using CVAT, the frames are labeled with relevant features to meet project requirements.</p>

### 5.3 Localization Challenges

<p style="text-align: justify;"><strong>Challenge</strong>: Ensuring compatibility of pre-trained models with local traffic conditions.</p>
<p style="text-align: justify;"><strong>Solution</strong>: Verified the accuracy of TrafficCamNet through extensive testing, confirming its reliability without the need for re-training.</p>

## 6. Conclusion

<p style="text-align: justify;">The Level-1 ADAS project successfully integrated High Beam Assist and Forward Collision Warning functionalities, providing a robust safety solution for SAIPA vehicles.</p>

### Key Outcomes:

1. <p style="text-align: justify;"><strong>HBA</strong>: Developed and deployed a CNN-based light classification system optimized for real-time inference on Jetson Nano.</p>
2. <p style="text-align: justify;"><strong>FCW</strong>: Successfully implemented vehicle detection with NVIDIA DeepStream, achieving high accuracy and real-time performance.</p>

<p style="text-align: justify;">This project showcased the potential of combining AI, edge computing, and custom datasets to address real-world challenges in the automotive industry.</p>

## 7. Future Work

1. <p style="text-align: justify;"><strong>Enhanced Detection</strong>: Explore more advanced detection models (e.g., YOLOv11, MTCNN) to improve robustness in challenging conditions.</p>
2. <p style="text-align: justify;"><strong>Expanded Features</strong>: Extend the system to include additional ADAS functionalities like pedestrian detection or adaptive cruise control.</p>
3. <p style="text-align: justify;"><strong>Deployment</strong>: Integrate the ADAS solution into production vehicles, testing it under real-world conditions.</p>

## 8. References

1. NVIDIA DeepStream SDK Documentation  <a href = "https://developer.nvidia.com/deepstream-sdk"> link</a>
2. CVAT Annotation Tool Documentation Retrieved from <a href = "https://opencv.github.io/cvat/"> link</a>
3. TrafficCamNet Model Details <a href="https://docs.nvidia.com/tao/tao-toolkit-archive/tao-40/text/model_zoo/cv_models/trafficcamnet.html"> link </a>

<img src="/images/hba-1.jpg" alt="HBA" style="width: 95%; height: auto; display: block; margin: 0 auto;">

<img src="/images/hba-7.PNG" alt="HBA" style="width: 95%; height: auto; display: block; margin: 0 auto;">





