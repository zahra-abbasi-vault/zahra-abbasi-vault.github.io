---
title: "Face Mask Detection"
collection: projects
category: projects
permalink: /project/Face-Mask-Detection
excerpt: 'A system designed to detect faces and classify individuals based on their mask-wearing status.'
date: 2023-05-01
des : 2023 , Bachelor's Degree Project
---


A system designed to detect faces and utilize a Convolutional Neural Network (CNN) for accurate classification based on individuals’ mask-wearing status. This project served as my bachelor’s thesis, earning a commendable 4.0/4.0 grade.

## Overview
I used the OpenCV Haar Cascade Classifier for face detection. Then I fed the detected faces into a CNN model for classification.
My perpous was to create a system that can be used in real-time applications, so I made sure that the face detection and classification model are light and fast.


### Face Detection
For face detection I used the OpenCV Haar Cascade Classifier which is light ,accurate and fast, suitable for real-time applications.


### Classification
For the classification task I trained an light weight CNN model with only  228,418 parameters. For this perpous I coded a training script in python using Tensorflow and Keras. At the end of the training process I got an accuracy of 99.5% on the test set.


### Data
Fot this project I gathered data from different sources available on the internet and converted them into the required format for training. One of my challenged was that one of my datasets included images with multiple people in them which was not suitable for training a model. to fix this problem I used my detection model to detect faces and cropping them, creating a new dataset.


