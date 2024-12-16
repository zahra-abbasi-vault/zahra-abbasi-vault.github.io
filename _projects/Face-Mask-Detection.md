---
title: "Face Mask Detection"
collection: projects
category: projects
permalink: /project/Face-Mask-Detection
excerpt: 'A system designed to detect faces and classify individuals based on their mask-wearing status.'
date: 2023-05-01
des : 2023 , Bachelor's Degree Project
---

## 1. Introduction

<p style="text-align: justify;">The COVID-19 pandemic has highlighted the importance of face masks as a measure to reduce transmission. This project, which was my Bachelor's thesis graded <strong>20/20</strong>, develops a <strong>Face Mask Detection System</strong> that automatically detects faces and classifies whether a person is wearing a mask. The system is designed for real-time applications such as surveillance cameras, public health monitoring, or automated access control in areas where mask-wearing is mandatory.</p>

<p style="text-align: justify;">This report discusses the design, methodology, implementation, challenges faced, and project outcomes. <a href="https://github.com/zahra-abbasi-vault/Face-Mask-Detection">Github</a></p>

## 2. System Overview

<p style="text-align: justify;">The Face Mask Detection System consists of two primary components: <strong>face detection</strong> and <strong>mask classification</strong>.</p>

- <p style="text-align: justify;"><strong>Face Detection</strong>: I used the OpenCV Haar Cascade Classifier to detect faces in input images or video frames. This method is lightweight, fast, and effective for real-time applications.</p>
- <p style="text-align: justify;"><strong>Mask Classification</strong>: Once faces are detected, a lightweight Convolutional Neural Network (CNN) model classifies whether the face is wearing a mask or not. The model was optimized for fast inference, making it suitable for real-time scenarios.</p>

<p style="text-align: justify;">The system was designed to balance speed and accuracy, ensuring practical deployment in real-time applications without significant computational overhead.</p>

## 3. Methodology

### 3.1. Face Detection using OpenCV Haar Cascade Classifier

<p style="text-align: justify;">For face detection, I utilized the <strong>OpenCV Haar Cascade Classifier</strong>, a widely used method in computer vision. This method is suitable for real-time applications due to its fast processing and reliable accuracy.</p>

- <p style="text-align: justify;"><strong>Advantages</strong>: The Haar Cascade Classifier is fast, computationally efficient, and simple to implement.</p>
- <p style="text-align: justify;"><strong>Challenges</strong>: While generally effective, the classifier can struggle with occlusions, varying lighting conditions, or faces at unusual angles. Despite these challenges, the model performed well for the scope of this project.</p>

### 3.2. CNN-based Mask Classification

<p style="text-align: justify;">Once faces were detected, they were passed to a CNN model for classification. The CNN was designed to be lightweight, with <strong>228,418 parameters</strong>, optimizing performance for real-time applications. The model was trained using <strong>TensorFlow</strong> and <strong>Keras</strong>, leveraging the following steps:</p>

1. <p style="text-align: justify;"><strong>Data Preprocessing</strong>: I resized and normalized the face images to prepare them for input into the CNN.</p>
2. <p style="text-align: justify;"><strong>Model Architecture</strong>: The CNN architecture consisted of several convolutional layers, followed by pooling layers and a fully connected layer for the final classification output.</p>
3. <p style="text-align: justify;"><strong>Training</strong>: The training process used <strong>categorical cross-entropy loss</strong> and the <strong>Adam optimizer</strong>. The Adam optimizer, known for adjusting the learning rate dynamically, was chosen for its ability to provide faster convergence and better coverage of the search space.</p>

<p style="text-align: justify;">The model achieved <strong>99% accuracy</strong> on the test set, demonstrating its effectiveness in classifying mask-wearing status.</p>

### 3.3. Data Collection and Preparation

<p style="text-align: justify;">The dataset was initially collected from publicly available sources. However, some images contained multiple faces, which made it difficult to train the model with single-face images. To address this, I used the face detection model to crop individual faces from multi-person images, creating a clean and structured dataset for training.</p>

<p style="text-align: justify;">To improve model generalization, I applied <strong>data augmentation</strong> techniques such as rotation, flipping, and brightness adjustments. This enhanced the diversity of the training data and helped the model perform well across varied real-world scenarios.</p>

## 4. Results and Evaluation

<p style="text-align: justify;">The performance of the Face Mask Detection system was evaluated based on the following criteria:</p>

1. <p style="text-align: justify;"><strong>Accuracy</strong>: The CNN model achieved 99% accuracy on the test set, indicating a high level of precision in detecting mask-wearing individuals.</p>
2. <p style="text-align: justify;"><strong>Speed</strong>: The system was optimized for real-time performance, allowing it to process video streams over <strong>30 FPS</strong> on a <strong>Nvidia 1050Ti</strong> graphic card, making it suitable for live surveillance applications.</p>
3. <p style="text-align: justify;"><strong>Robustness</strong>: Despite challenges like varying lighting and face orientations, the model demonstrated consistent performance across different datasets, proving its robustness in diverse conditions.</p>

## 5. Challenges and Solutions

<p style="text-align: justify;">Several challenges arose during the development of the system:</p>

1. <p style="text-align: justify;"><strong>Dataset Quality</strong>: Some datasets contained multiple faces in a single image, which made it difficult to train the model. To resolve this, I used the face detection model to crop individual faces, creating a structured dataset.</p>
2. <p style="text-align: justify;"><strong>Model Optimization</strong>: Balancing the lightweight nature of the CNN model with high accuracy was challenging. I experimented with different architectures and parameter tuning to achieve optimal performance without sacrificing real-time inference.</p>
3. <p style="text-align: justify;"><strong>Face Detection under Varying Conditions</strong>: The face detection model faced challenges in detecting faces under poor lighting or at unusual angles. To mitigate this, I incorporated diverse data sources with varying lighting and angles into the training set.</p>

## 6. Conclusion

<p style="text-align: justify;">The <strong>Face Mask Detection System</strong> developed in this project achieved a high level of accuracy and demonstrated its potential for real-time applications. By using the OpenCV Haar Cascade Classifier for face detection and a lightweight CNN for mask classification, the system is efficient and effective for deployment in environments where mask-wearing needs to be monitored, such as airports, shopping malls, or offices.</p>

<p style="text-align: justify;">The project not only met the initial goals but also provided valuable insights into the challenges of building real-time computer vision applications. Moving forward, improvements could focus on enhancing the robustness of face detection in challenging conditions and expanding the system to detect additional objects or behaviors.</p>

## 7. Future Work

<p style="text-align: justify;">Several areas could be explored for future improvements:</p>

- <p style="text-align: justify;"><strong>Improved Face Detection</strong>: Use more advanced face detection algorithms such as <strong>YOLO</strong> for better accuracy under difficult conditions (e.g., low light, side profiles).</p>
- <p style="text-align: justify;"><strong>Multi-Class Classification</strong>: Expand the system to classify different types of face coverings or detect people without any face coverings, such as those wearing face shields or other protective gear.</p>
- <p style="text-align: justify;"><strong>Deployment</strong>: Implement the system into a complete application that can run on live video streams or integrate with a camera surveillance system.</p>

## 8. References

1. <strong>OpenCV documentation.</strong> (n.d.). Haar Cascade Classifier. Retrieved from <a href="https://docs.opencv.org/4.x/d2/d99/tutorial_js_face_detection.html">link</a>
2. <strong>TensorFlow documentation.</strong> (n.d.). CNN tutorial. Retrieved from <a href="https://www.tensorflow.org/guide/intro_to_modules">link</a>
3. <strong>Keras documentation.</strong> (n.d.). Building a CNN. Retrieved from <a href="https://keras.io/guides/sequential_model/">link</a>
