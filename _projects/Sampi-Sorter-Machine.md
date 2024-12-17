---
title: "Sampi Sorter Machine"
collection: projects
category: projects
permalink: /project/Sampi-Sorter-Machine
excerpt: 'The Sampi Sorter is a state-of-the-art sorting machine that leverages artificial intelligence to precisely categorize grains and agricultural products according to their visual properties.'
date: 2024-02-17
des: 2023 - present, Pouya Fanavaran Kosar
---

## 1. Introduction

<p style="text-align: justify;">The Sampi Sorter is a cutting-edge sorting machine designed to meet the diverse needs of the agricultural industry. It uses advanced image processing and artificial intelligence (AI) to classify agricultural products like grains, nuts, and dried fruits. By analyzing features such as size, shape, and color, the system separates products into "desired" and "undesired" categories.</p>

<p style="text-align: justify;">This report highlights my contributions as the lead AI developer, focusing on optimizing the Sampi Sorter's detection and classification capabilities using computer vision and machine learning models. <a href="https://www.sorter.ir/en/" target="_blank">Project Website</a></p>

<img src="images/sorter-2.jpg" alt="sorter" style="width: 90%; height: auto; display: block; margin: 0 auto;">

## 2. System Overview

<p style="text-align: justify;">The Sampi Sorter operates in multiple stages:</p>
- <p style="text-align: justify;"><strong>Product Transport</strong>: Products are first moved via a conveyor belt, where contaminants like dust are removed.</p>
- <p style="text-align: justify;"><strong>Image Capture</strong>: High-resolution images of the products are captured by cameras and sensors.</p>
- <p style="text-align: justify;"><strong>AI Classification</strong>: AI algorithms analyze the images in real-time, classifying the products based on quality metrics.</p>
- <p style="text-align: justify;"><strong>Separation</strong>: Sorted products are separated using air jets to minimize damage.</p>

<p style="text-align: justify;">This system features non-destructive sorting, remote monitoring, and real-time performance reporting, ensuring enhanced efficiency and product quality.</p>

## 3. Methodology

### 3.1. Detection with YOLOv8

<p style="text-align: justify;">A critical part of this project was developing an accurate detection model. YOLOv8, a state-of-the-art real-time object detection algorithm, was employed for its balance of speed and precision.</p>

- <p style="text-align: justify;"><strong>Data Collection and Preprocessing</strong>: Images of agricultural products were captured under various conditions, creating a robust dataset. Augmentation techniques were used to improve model generalization.</p>
- <p style="text-align: justify;"><strong>Model Training</strong>: The YOLOv8 architecture was optimized to detect objects with high efficiency and low computational overhead.</p>
- <p style="text-align: justify;"><strong>Optimization</strong>: Fine-tuning was performed to reduce box loss and improve model accuracy.</p>

<p style="text-align: justify;">The final model achieved a detection accuracy of <strong>99%</strong>, demonstrating its effectiveness in sorting agricultural products such as beans.</p>

![YOLOv8 Detection](../images/Sorter_Yolo.bmp)

### 3.2. Classification with CNNs

<p style="text-align: justify;">After detection, convolutional neural networks (CNNs) were used to classify the products based on defects. Separate models were developed for each product type, such as lentils, cowpeas, and coffee beans.</p>

- <p style="text-align: justify;"><strong>Architecture Design</strong>: The CNNs were designed to extract relevant features, such as broken kernels or discoloration, from product images.</p>
- <p style="text-align: justify;"><strong>Training and Evaluation</strong>: The models were trained on labeled datasets and tested for generalization using unseen data.</p>
- <p style="text-align: justify;"><strong>Optimization</strong>: Hyperparameter tuning helped improve classification accuracy and reduce errors.</p>

<p style="text-align: justify;">These classifiers achieved high precision, ensuring accurate sorting based on product quality standards.</p>

## 4. Results and Evaluation

<p style="text-align: justify;">The integration of AI into the Sampi Sorter resulted in significant improvements in performance:</p>
- <p style="text-align: justify;"><strong>Detection</strong>: The YOLOv8 model achieved <strong>99%</strong> accuracy in detecting agricultural products, even under varied conditions.</p>
- <p style="text-align: justify;"><strong>Classification</strong>: The CNN classifiers accurately categorized defects, ensuring that only high-quality products were selected.</p>
<p style="text-align: justify;">These advancements have made the Sampi Sorter a highly efficient tool for real-time agricultural sorting, providing both accuracy and minimal product damage.</p>

<img src="/images/CBB-positive-1.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/CBB-positive-2.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">

#### The Coffee Berry Borer, or Hypthenemus Hampei, is one of the most significant pest problems for coffee farmers.
<br/>
<img src="/images/shell_positive_1.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/shell_positive_2.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">

#### Shell is a common defect where coffee beans have a large cavity similar to a shell.
<br/>

## 5. Challenges and Solutions

<p style="text-align: justify;">During the development process, several challenges were encountered:</p>
1. <p style="text-align: justify;"><strong>Data Variability</strong>: Variations in lighting and product positioning affected the model’s accuracy. To overcome this, extensive data augmentation was applied.</p>
2. <p style="text-align: justify;"><strong>Hardware Constraints</strong>: The model needed optimization to run efficiently on available hardware without sacrificing performance. This was achieved by fine-tuning the YOLOv8 model and optimizing CNN architectures.</p>
3. <p style="text-align: justify;"><strong>Defect Detection Accuracy</strong>: Detecting smaller defects, such as minor discoloration, proved challenging. The solution involved gathering a more diverse dataset and using more advanced data augmentation techniques.</p>

## 6. Conclusion

<p style="text-align: justify;">The Sampi Sorter machine, powered by AI, is a highly effective tool for agricultural sorting, offering significant improvements in speed and accuracy. By utilizing YOLOv8 for detection and CNNs for classification, the system ensures efficient sorting of agricultural products with minimal damage.</p>

<p style="text-align: justify;">This project demonstrates the transformative potential of AI in agriculture. Future work could involve expanding classification capabilities, improving defect detection, and increasing the range of agricultural products supported by the system.</p>



