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


## Overview
<p style="text-align: justify;">The Sampi Sorter is a state-of-the-art sorting machine that leverages artificial intelligence to precisely categorize grains and agricultural products according to their visual properties. <a href="https://www.sorter.ir/en/" target="_blank">Project Website</a></p>


<img src="/images/sorchine.png" alt="karabin" style="width: 90%; height: auto; display: block; margin: 0 auto;">

<p style="text-align: justify;">In this industrial project, I served as an AI developer. My responsibilities included training high-accuracy models for accurate bean detection and classification.<br/> I successfully fine-tuned the YOLOv8 model with 99% accuracy in bean detection. Subsequently, for each type of bean, I implemented a CNN model for high-accuracy classification. I was part of this project for multiple products such as lentils, Cowpea, and coffee beans.</p>


## Detection Model Output

<p style="text-align: justify;">One of the challenges I faced was detecting coffee beans in the image below. Due to the hardware limitations, the model's input size couldn't be increased much, and for the tracking algorithm, the box loss needed to decrease as much as possible. In the end, the model achieved 99% accuracy in detection.</p>


![Sampi Sorter Machine](/images/Sorter_Yolo.bmp)


## Classification Model Output


<p style="text-align: justify;">Below are some of the outputs of the classification models. The images are of the latest product, coffee beans, that were added to the system. I trained different models for each type of the defect.</p>

### Detecting Shell
<p style="text-align: justify;">Shell is a common defect where coffee beans have a large cavity similar to a shell.</p>

![Coffee Shell detection](/images/shell_positive_1.bmp)


![Coffee Shell detection](/images/shell_positive_2.bmp)


### Detecting Coffee Berry Borer Damaged

<p style="text-align: justify;">The Coffee Berry Borer, or Hypthenemus Hampei, is one of the most significant pest problems for coffee farmers.</p>

![Coffee Berry Borer detection](/images/CBB-positive-1.bmp)

![Coffee Berry Borer detection](/images/CBB-positive-2.bmp)






