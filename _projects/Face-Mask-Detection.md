---
title: "Face Mask Detection"
collection: projects
category: projects
permalink: /project/Face-Mask-Detection
excerpt: 'A system designed to detect faces and classify individuals based on their mask-wearing status.'
date: 2023-05-01
des : 2023 , Bachelor's Degree Project
---


<div style="text-align: justify;">

## 1. Introduction

The COVID-19 pandemic has highlighted the importance of face masks as a measure to reduce transmission. This project, which was my Bachelor's thesis graded **20/20**, develops a **Face Mask Detection System** that automatically detects faces and classifies whether a person is wearing a mask. The system is designed for real-time applications such as surveillance cameras, public health monitoring, or automated access control in areas where mask-wearing is mandatory.

This report discusses the design, methodology, implementation, challenges faced, and project outcomes.
<a href="https://github.com/zahra-abbasi-vault/Face-Mask-Detection">Github</a>
## 2. System Overview

The Face Mask Detection System consists of two primary components: **face detection** and **mask classification**.

- **Face Detection**: I used the OpenCV Haar Cascade Classifier to detect faces in input images or video frames. This method is lightweight, fast, and effective for real-time applications.
- **Mask Classification**: Once faces are detected, a lightweight Convolutional Neural Network (CNN) model classifies whether the face is wearing a mask or not. The model was optimized for fast inference, making it suitable for real-time scenarios.

The system was designed to balance speed and accuracy, ensuring practical deployment in real-time applications without significant computational overhead.

## 3. Methodology

### 3.1. Face Detection using OpenCV Haar Cascade Classifier

For face detection, I utilized the **OpenCV Haar Cascade Classifier**, a widely used method in computer vision. This method is suitable for real-time applications due to its fast processing and reliable accuracy.

- **Advantages**: The Haar Cascade Classifier is fast, computationally efficient, and simple to implement.
- **Challenges**: While generally effective, the classifier can struggle with occlusions, varying lighting conditions, or faces at unusual angles. Despite these challenges, the model performed well for the scope of this project.

### 3.2. CNN-based Mask Classification

Once faces were detected, they were passed to a CNN model for classification. The CNN was designed to be lightweight, with **228,418 parameters**, optimizing performance for real-time applications. The model was trained using **TensorFlow** and **Keras**, leveraging the following steps:

1. **Data Preprocessing**: I resized and normalized the face images to prepare them for input into the CNN.
2. **Model Architecture**: The CNN architecture consisted of several convolutional layers, followed by pooling layers and a fully connected layer for the final classification output.
3. **Training**: The training process used **categorical cross-entropy loss** and the **Adam optimizer**. The Adam optimizer, known for adjusting the learning rate dynamically, was chosen for its ability to provide faster convergence and better coverage of the search space.

The model achieved **99% accuracy** on the test set, demonstrating its effectiveness in classifying mask-wearing status.

### 3.3. Data Collection and Preparation

The dataset was initially collected from publicly available sources. However, some images contained multiple faces, which made it difficult to train the model with single-face images. To address this, I used the face detection model to crop individual faces from multi-person images, creating a clean and structured dataset for training.

To improve model generalization, I applied **data augmentation** techniques such as rotation, flipping, and brightness adjustments. This enhanced the diversity of the training data and helped the model perform well across varied real-world scenarios.

## 4. Results and Evaluation

The performance of the Face Mask Detection system was evaluated based on the following criteria:

1. **Accuracy**: The CNN model achieved 99% accuracy on the test set, indicating a high level of precision in detecting mask-wearing individuals.
2. **Speed**: The system was optimized for real-time performance, allowing it to process video streams over **30 FPS** on a **Nvidia 1050Ti** graphic card, making it suitable for live surveillance applications.
3. **Robustness**: Despite challenges like varying lighting and face orientations, the model demonstrated consistent performance across different datasets, proving its robustness in diverse conditions.

## 5. Challenges and Solutions

Several challenges arose during the development of the system:

1. **Dataset Quality**: Some datasets contained multiple faces in a single image, which made it difficult to train the model. To resolve this, I used the face detection model to crop individual faces, creating a structured dataset.
2. **Model Optimization**: Balancing the lightweight nature of the CNN model with high accuracy was challenging. I experimented with different architectures and parameter tuning to achieve optimal performance without sacrificing real-time inference.
3. **Face Detection under Varying Conditions**: The face detection model faced challenges in detecting faces under poor lighting or at unusual angles. To mitigate this, I incorporated diverse data sources with varying lighting and angles into the training set.

## 6. Conclusion

The **Face Mask Detection System** developed in this project achieved a high level of accuracy and demonstrated its potential for real-time applications. By using the OpenCV Haar Cascade Classifier for face detection and a lightweight CNN for mask classification, the system is efficient and effective for deployment in environments where mask-wearing needs to be monitored, such as airports, shopping malls, or offices.

The project not only met the initial goals but also provided valuable insights into the challenges of building real-time computer vision applications. Moving forward, improvements could focus on enhancing the robustness of face detection in challenging conditions and expanding the system to detect additional objects or behaviors.

## 7. Future Work

Several areas could be explored for future improvements:

- **Improved Face Detection**: Use more advanced face detection algorithms such as **YOLO** for better accuracy under difficult conditions (e.g., low light, side profiles).
- **Multi-Class Classification**: Expand the system to classify different types of face coverings or detect people without any face coverings, such as those wearing face shields or other protective gear.
- **Deployment**: Implement the system into a complete application that can run on live video streams or integrate with a camera surveillance system.

## 8. References

1. **OpenCV documentation.** (n.d.). Haar Cascade Classifier. Retrieved from [https://docs.opencv.org/4.x/d2/d99/tutorial_js_face_detection.html](https://docs.opencv.org/4.x/d2/d99/tutorial_js_face_detection.html)
2. **TensorFlow documentation.** (n.d.). CNN tutorial. Retrieved from [https://www.tensorflow.org/guide/intro_to_modules](https://www.tensorflow.org/guide/intro_to_modules)
3. **Keras documentation.** (n.d.). Building a CNN. Retrieved from [https://keras.io/guides/sequential_model/](https://keras.io/guides/sequential_model/)
</div>