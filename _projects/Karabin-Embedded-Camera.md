---
title: "Karabin Embedded Camera"
collection: projects
category: projects
permalink: /project/Karabin-Embedded-Camera
excerpt: 'Karabin is an embedded ANPR camera that excels in accurately reading license plates and estimating vehicle speeds. It's a self-contained system that only requires power supply, handling all image processing and internal control functions.'
date: 2023-12-30
des : 2023 , Pouya Fanavaran Kosar

---

<p style="text-align: justify;">The Karabin Embedded LPR Camera is a comprehensive all-in-one system, featuring color and infrared cameras, image processing, control and power electronic units, and a specialized lighting module for ANPR. The process of LPR is done exclusively and independently of any external processing unit, requiring only a power supply. Its output includes license plates and images of passing vehicles 
<a href="https://www.cam2vision.com/products/karabin/" target="_blank">Project Website</a></p>

<p style="text-align: justify;"> I contributed to the improvement of this system by improving the accuracy of persian plate recognition, vehicle type and vehicle model clasdification,</p>


<img src="/images/Karabin.png" alt="karabin" style="width: 100%; height: auto; display: block; margin: 0 auto;">

## My Contributions

### Persian Plate Character Recognition
<p style="text-align: justify;">I developed a CNN model achieving 98% accuracy in recognizing 10 numbers and over 25 Persian letters. Previously, the system relied on pure image processing algorithms. My contribution significantly enhanced plate reading accuracy through deep learning.</p>


<img src="/images/karabin.jpg" alt="karabin-3" style="width: 30%; height: auto; display: block; margin: 0 auto;">

### Vehicle Type Classification
<p style="text-align: justify;">I implemented a classification system for vehicles into six categories: sedan, bus, minibus, truck, pickup, and van. This system works for both front and rear views, using a lightweight CNN model deployable on commercial embedded processors at over 20 FPS. The classification accuracy exceeds 98%.</p>



### Vehicle Model Recognition
<p style="text-align: justify;">I spearheaded the development of a model recognition system for vehicles passing the Karabin camera. We collected data from over 95% of vehicle models in the country's market, covering nearly 700 models. I trained two main models for front and rear views, achieving 97% accuracy with a medium-weight CNN model. This project is a significant achievement in our country, with the model being retrained monthly to include new vehicle models.</p>

<p style="text-align: justify;">Working on this project was a great honor for me, as it contributes to making roads safer, preventing car crashes, and preserving lives by controlling vehicle speed.</p>
