---
title: "Level-1 ADAS"
collection: projects
category: projects
permalink: /project/Level-1-ADAS
excerpt: 'Level-1 Advanced Driver Assistance System'
date: 2023-10-01
des : 2023 , Pouya Fanavaran Kosar - SAIPA CO.

---

## Introduction
<p style="text-align: justify;">
This project was conducted in collaboration with PFK, a leading knowledge-based enterprise, and SAIPA, the largest automobile manufacturer in Iran. The goal was to develop the country’s first Level-1 Advanced Driver Assistance System (ADAS). As a research-based initiative, the project emphasized enhancing road and vehicle safety through the integration of several key features, including Forward Collision Warning (FCW), Lane Departure Warning (LDW), and High Beam Assistance (HBA). This marked SAIPA's first entry into ADAS technology and represented a significant milestone for Iran's automotive industry. </p>


## System Overview
The Level-1 ADAS project included the following components:
### High Beam Assist (HBA)
The HBA system improves night-driving safety by automatically managing the vehicle's high beams.
-	Goal: To classify lights into three categories:
1.	Vehicle front lights
2.	Vehicle rear lights
3.	Road lights and random light reflections
-	Implementation: A custom Convolutional Neural Network (CNN) model was developed for light classification and optimized for real-time inference on NVIDIA Jetson Nano hardware.
### Forward Collision Warning (FCW)
The FCW system alerts drivers to potential collisions by detecting vehicles in real time.
-	Goal: To achieve reliable vehicle detection with a frame rate exceeding 15 FPS on Jetson Nano.
-	Implementation: NVIDIA's DeepStream library was used to deploy a pre-trained TrafficCamNet model, which performed well without requiring additional re-training.
Both systems were designed to balance accuracy, speed, and hardware efficiency, making them suitable for practical, real-time applications


## My Contributions

### High Beam Assist (HBA)
1.	Dataset Creation and Annotation:
A custom dataset was created due to the lack of pre-existing datasets for this application. Using the CVAT annotation tool, objects like streetlights, traffic signs, and vehicle lights were labeled. This dataset was tailored to local driving conditions.
2.	CNN Architecture and Training:
	The CNN model consisted of multiple convolutional layers, optimized for classification accuracy and real-time inference.
	The training process included:
	Preprocessing: Resizing and normalizing images for model input.
	Optimization: Techniques like model pruning and quantization were applied to reduce the model's size and inference time.
	The final model met the performance requirements of Jetson Nano, achieving high accuracy in light classification.

### Forward Collision Warning (FCW)
1.	Vehicle Detection with DeepStream:
	NVIDIA's DeepStream SDK was used to deploy the TrafficCamNet model on Jetson Nano.
	The model achieved over 15 FPS, meeting the real-time requirements for FCW.
	No transfer learning or re-training was needed, as the pre-trained model effectively detected Iranian vehicles as well as the other models.
2.	System Integration:
	The FCW system was integrated with Jetson Nano, ensuring seamless processing of video streams with minimal computational overhead.

<img src="/images/hba-1.jpg" alt="HBA" style="width: 95%; height: auto; display: block; margin: 0 auto;">



<img src="/images/hba-7.PNG" alt="HBA" style="width: 95%; height: auto; display: block; margin: 0 auto;">





