---
title: "Sampi Sorter Machine"
collection: projects
category: projects
permalink: /project/Sampi-Sorter-Machine
excerpt: 'The Sampi Sorter is a state-of-the-art sorting machine that leverages artificial intelligence to precisely categorize grains and agricultural products according to their visual properties.'
date: 2024-02-17
image: /images/sorchine.png
des : 2023 - present , Pouya Fanavaran Kosar 
---

# Development of AI Solutions for Agricultural Sorting  

## 1. Introduction  
The Sampi Sorter is a cutting-edge sorting machine designed to meet the agricultural industry's diverse needs. It utilizes advanced image processing and artificial intelligence (AI) to classify agricultural products like grains, nuts, and dried fruits. The system identifies features such as size, shape, and color to separate products into "desired" and "undesired" categories.  

This project highlights my contributions as the lead AI developer, focusing on optimizing the Sampi Sorter's detection and classification capabilities using computer vision and machine learning models.<a href="https://www.sorter.ir/en/" target="_blank">Project Website</a>

<img src="/images/sorchine.png" alt="karabin" style="width: 90%; height: auto; display: block; margin: 0 auto;">

## 2. System Overview  
The Sampi Sorter operates in multiple stages:  
- Products are first transported via a conveyor, where contaminants like dust are removed.  
- Cameras and sensors then capture high-resolution images of the products.  
- AI algorithms analyze these images in real-time, classifying items based on quality metrics.  
- Sorted products are separated using air jets, ensuring minimal damage.  

The system supports features like non-destructive sorting, remote monitoring, and real-time performance reporting, enhancing efficiency and product quality.  

## 3. AI Development  
### 3.1 Detection with YOLOv8  
A critical aspect of this project was developing an accurate detection model. YOLOv8, a state-of-the-art real-time object detection algorithm, was employed for its balance of speed and precision.  

Key steps in development included:  
- **Data Collection and Preprocessing**: Images of products were captured under varied conditions to create a robust dataset, augmented to improve model generalization.  
- **Model Training**: The YOLOv8 architecture was optimized to detect objects within bounding boxes efficiently.  
- **Optimization**: Hardware constraints were addressed by fine-tuning the model to reduce box loss, achieving high accuracy with minimal computational overhead.  

The final model achieved a detection accuracy of 99%, demonstrating its effectiveness in sorting agricultural products like beans.  

<img src="/images/Sorter_Yolo.bmp" alt="Sorter_Yolo" style="width: 90%; height: auto; display: block; margin: 0 auto;">

### 3.2 Classification with CNNs  
Following detection, convolutional neural networks (CNNs) were used to classify products based on defects. Separate models were developed for each product type, such as lentils, cowpeas, and coffee beans.  

Key steps included:  
- **Architecture Design**: CNNs were configured to extract relevant features from product images, such as broken kernels or discoloration.  
- **Training and Evaluation**: Models were trained on labeled datasets and tested for generalization using unseen data.  
- **Optimization**: Hyperparameter tuning refined the models to minimize errors and improve classification accuracy.  

These classifiers achieved high precision, ensuring the accurate sorting of products based on quality standards.  

#### The Coffee Berry Borer, or Hypthenemus Hampei, is one of the most significant pest problems for coffee farmers.
<img src="/images/CBB-positive-1.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/CBB-positive-2.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">



#### Shell is a common defect where coffee beans have a large cavity similar to a shell.
<img src="/images/shell_positive_1.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/shell_positive_2.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">



## 4. Results and Impact  
The integration of AI into the Sampi Sorter significantly enhanced its performance:  
- **Detection**: The YOLOv8 model achieved 99% accuracy in identifying products across various conditions.  
- **Classification**: CNN models reliably categorized defects, ensuring consistent quality control.  

These advancements made the Sampi Sorter a highly effective tool for real-time agricultural sorting, balancing accuracy and efficiency while maintaining product integrity.  

## 5. Conclusion  
This project demonstrates the transformative potential of AI in agriculture. By leveraging YOLOv8 for detection and CNNs for classification, the Sampi Sorter delivers exceptional accuracy and speed. The integration of these models streamlines the sorting process, enhances product quality, and increases productivity.  

Future improvements could focus on incorporating advanced detection methods and expanding classification capabilities to support a wider variety of agricultural products, further strengthening the role of AI in modern agriculture.  


<!-- ## Overview
<p style="text-align: justify;">The Sampi Sorter is a state-of-the-art sorting machine that leverages artificial intelligence to precisely categorize grains and agricultural products according to their visual properties. <a href="https://www.sorter.ir/en/" target="_blank">Project Website</a></p>


<img src="/images/sorchine.png" alt="karabin" style="width: 90%; height: auto; display: block; margin: 0 auto;">

## My Contributions

<p style="text-align: justify;">In this industrial project, I served as the AI developer. My responsibilities included training high-accuracy models for accurate bean detection and classification.<br/> I successfully fine-tuned the YOLOv8 model with 99% accuracy in bean detection. Subsequently, for each type of bean, I implemented a CNN model for high-accuracy classification. I was part of this project for multiple products such as lentils, Cowpea, and coffee beans.</p>


### Detection Model Output

<p style="text-align: justify;">One of the challenges I faced was detecting coffee beans in the image below. Due to the hardware limitations, the model's input size couldn't be increased much, and for the tracking algorithm, the box loss needed to decrease as much as possible. In the end, the model achieved 99% accuracy in detection.</p>

<img src="/images/Sorter_Yolo.bmp" alt="Sorter_Yolo" style="width: 90%; height: auto; display: block; margin: 0 auto;">

### Classification Model Output


<p style="text-align: justify;">Here are some outputs from the classification models. The images show the latest product, coffee beans, that were added to the system. I trained different models for each type of defect.</p>
<br/>

### Detecting Coffee Berry Borer Damaged

<p style="text-align: justify;">The Coffee Berry Borer, or Hypthenemus Hampei, is one of the most significant pest problems for coffee farmers.</p>
<img src="/images/CBB-positive-1.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/CBB-positive-2.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">



### Detecting Shell
<p style="text-align: justify;">Shell is a common defect where coffee beans have a large cavity similar to a shell.</p>
<img src="/images/shell_positive_1.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/shell_positive_2.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;"> -->











