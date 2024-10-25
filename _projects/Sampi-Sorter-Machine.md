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

![Sampi Sorter Machine](/images/sorchine.png)

<p style="text-align: justify;">The Sampi Sorter is a state-of-the-art sorting machine that leverages artificial intelligence to precisely categorize grains and agricultural products according to their visual properties.</p>

<p style="text-align: justify;">In this industrial project, I served as an AI developer. 
My responsibilities included training high accuracy models for accurate bean detection and classification.
I successfully fine-tuned the YOLOv8 model with 99% accuracy in bean detection. 
Subsequently, for each product , I implemented a CNN model for high accuracy classification.</p>
<p> I was part of this project fot multiple products such as lentils, Cowpea, coffee beans.</p>
<p style="text-align: justify;">Coffee beans are the lastes bean types that were added to the system.</p>


## Detection Model Output

The detection of coffee beans in the image below was one of the challenges that I faced. Due to the hardware limitations, the model's input size couldn't be increased much and for the tracking algorithm, there was a need to decrease the box loss as much as possible. In the end the model achieved 99% accuracy in detection.


![Sampi Sorter Machine](/images/Sorter_Yolo.bmp)


## Classification Model Output

Below are some of the outputs of the classification models.
the images are from the lastest product , coffee beans , that were added to the system.
I trained different models for each type of the defects.

### Detecting Shell
 shell is common defect where coffee beans have a large cavity similar to a shell.

![Coffee Shell detection](/images/shell_positive_1.bmp)


![Coffee Shell detection](/images/shell_positive_2.bmp)


### Detecting Coffee Berry Borer Damaged

Coffee Berry Borer damaged coffee beans. The Coffee Berry Borer, or Hypthenemus Hampei, is one of the most significant pest problems for coffee farmers. 

![Coffee Berry Borer detection](/images/CBB-positive-1.bmp)

![Coffee Berry Borer detection](/images/CBB-positive-2.bmp)






