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
<p style="text-align: justify;">The Sampi Sorter is a cutting-edge sorting machine designed to meet the agricultural industry's diverse needs. It utilizes advanced image processing and artificial intelligence (AI) to classify agricultural products like grains, nuts, and dried fruits. The system identifies features such as size, shape, and color to separate products into "desired" and "undesired" categories. </p> 

<p style="text-align: justify;">This report highlights my contributions as the lead AI developer, focusing on optimizing the Sampi Sorter's detection and classification capabilities using computer vision and machine learning models</p>.<a href="https://www.sorter.ir/en/" target="_blank">Project Website</a>

<img src="/images/sorchine.png" alt="karabin" style="width: 90%; height: auto; display: block; margin: 0 auto;">

## 2. System Overview  
<p style="text-align: justify;">The Sampi Sorter operates in multiple stages:</p>  
- <p style="text-align: justify;">Products are first transported via a conveyor, where contaminants like dust are removed.</p>  
- <p style="text-align: justify;">Cameras and sensors then capture high-resolution images of the products.</p>  
- <p style="text-align: justify;">AI algorithms analyze these images in real-time, classifying items based on quality metrics.</p>  
- <p style="text-align: justify;">Sorted products are separated using air jets, ensuring minimal damage.</p>  

<p style="text-align: justify;">The system supports features like non-destructive sorting, remote monitoring, and real-time performance reporting, enhancing efficiency and product quality.</p>

## 3. AI Development  
### 3.1 Detection with YOLOv8  
<p style="text-align: justify;">A critical aspect of this project was developing an accurate detection model. YOLOv8, a state-of-the-art real-time object detection algorithm, was employed for its balance of speed and precision.  </p>

Key steps in development included:  
- **Data Collection and Preprocessing**:<p style="text-align: justify;"> Images of products were captured under varied conditions to create a robust dataset, augmented to improve model generalization.</p>
- **Model Training**: <p style="text-align: justify;">The YOLOv8 architecture was optimized to detect objects within bounding boxes efficiently. </p> 
- **Optimization**: <p style="text-align: justify;">Hardware constraints were addressed by fine-tuning the model to reduce box loss, achieving high accuracy with minimal computational overhead. </p>

<p style="text-align: justify;">The final model achieved a detection accuracy of 99%, demonstrating its effectiveness in sorting agricultural products like beans.</p>

<img src="/images/Sorter_Yolo.bmp" alt="Sorter_Yolo" style="width: 90%; height: auto; display: block; margin: 0 auto;">

### 3.2 Classification with CNNs  
<p style="text-align: justify;">Following detection, convolutional neural networks (CNNs) were used to classify products based on defects. Separate models were developed for each product type, such as lentils, cowpeas, and coffee beans.  </p>

Key steps included:  
- **Architecture Design**: <p style="text-align: justify;"> CNNs were configured to extract relevant features from product images, such as broken kernels or discoloration.</p>
- **Training and Evaluation**: <p style="text-align: justify;"> Models were trained on labeled datasets and tested for generalization using unseen data.</p>
- **Optimization**: <p style="text-align: justify;"> Hyperparameter tuning refined the models to minimize errors and improve classification accuracy.</p>

<p style="text-align: justify;">These classifiers achieved high precision, ensuring the accurate sorting of products based on quality standards.  </p>

<img src="/images/CBB-positive-1.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/CBB-positive-2.bmp" alt="cbb" style="width: 90%; height: auto; display: block; margin: 0 auto;">

#### <p style="text-align: justify;">The Coffee Berry Borer, or Hypthenemus Hampei, is one of the most significant pest problems for coffee farmers.</p>



<img src="/images/shell_positive_1.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<img src="/images/shell_positive_2.bmp" alt="shell" style="width: 90%; height: auto; display: block; margin: 0 auto;">

#### <p style="text-align: justify;"> Shell is a common defect where coffee beans have a large cavity similar to a shell.</p>



## 4. Results and Impact  
<p style="text-align: justify;">The integration of AI into the Sampi Sorter significantly enhanced its performance:  </p>  
- **Detection**:<p style="text-align: justify;"> The YOLOv8 model achieved 99% accuracy in identifying products across various conditions.  </p>  
- **Classification**:<p style="text-align: justify;"> CNN models reliably categorized defects, ensuring consistent quality control.  </p>  

<p style="text-align: justify;">These advancements made the Sampi Sorter a highly effective tool for real-time agricultural sorting, balancing accuracy and efficiency while maintaining product integrity. </p> 

## 5. Conclusion  
<p style="text-align: justify;">This project demonstrates the transformative potential of AI in agriculture. By leveraging YOLOv8 for detection and CNNs for classification, the Sampi Sorter delivers exceptional accuracy and speed. The integration of these models streamlines the sorting process, enhances product quality, and increases productivity.</p>

<p style="text-align: justify;">Future improvements could focus on incorporating advanced detection methods and expanding classification capabilities to support a wider variety of agricultural products, further strengthening the role of AI in modern agriculture.  </p>











