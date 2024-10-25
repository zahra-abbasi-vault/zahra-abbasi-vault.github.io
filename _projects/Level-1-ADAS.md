---
title: "Level-1-ADAS"
collection: projects
category: projects
permalink: /project/Level-1-ADAS
: 'Level-1-ADAS'
date: 2023-10-01
des : 2023 , Pouya Fanavaran Kosar - SAIPA CO.

---

<p style="text-align: justify;">This Level-1 ADAS project utilizes a monocular camera with an NVIDIA Jetson Nano board. After more than 6 months of focused research, we have effectively created and optimized AI and Computer Vision algorithms, meeting the specified performance goals for the Departure Warning (LDW) and High Beam Assist (HBA) systems. </p>

<p style="text-align: justify;">I contributed to the design of the CNN architecture and decision-making algorithms of HBA in this projet.</p>


![hba-1](/images/hba-1.jpg)


## Challenges

<p style="text-align: justify;">Due to the hardware limitations of the Jetson Nano, I had to optimize the model size and the inference time to meet the real-time requirements. Furthermore, situable datasets were not available for training the HBA model , so I had to create my own dataset. For this perpous I used CVAT annotation tool to detect objects (such as street lights , signs , vehicles front and rear lights , etc). Thanks to our annotating team, the dataset was ready in a short time.</p>

### Annotation
![HBA-7](/images/hba-7.PNG)

 




