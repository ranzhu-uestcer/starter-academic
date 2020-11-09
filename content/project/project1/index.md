---
title: Human Activity Recognition
summary: An efficient deep Ensemble method to recognize confusing activities.
tags:
- Deep Learning
date: "2019-06-10T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
- icon: envelope
  icon_pack: fas
  name: contact
  link: "zhu_ran@outlook.com"
url_code: ""
url_pdf: "https://ieeexplore.ieee.org/document/8734079"
url_slides: ""
url_video: 'media/HAR_video.mp4'

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

Human activity recognition (HAR) aiming to identify the actions carried out by a person given a set of observations of subject, has attracted much attention from both academia and industry with widely application requirements appearing in the indoor pedestrian tracking, healthcare, and smart cities. Currently, HAR methods can be mainly summarized as two categories: vision-based and sensor-based. Vision-based mainly relies on various high-frame-rate video devices. External factors such as lighting condition, clothing color, and image background have a great impact on recognition accuracy. The sensor-based approach, by contrast, is more robust in complex environments, which makes the system convenient and portable. Also, it can identify confusing human activities with the mathematical model by directly measuring the motion from human activities without infringement of personal privacy.

With the advent of miniaturized sensors and powerful computing resources in smartphones, the concept of efficient and ubiquitous HAR on smartphones is ready to fulfill soon. Among recent studies focusing on smartphone-based HAR, most researchers chose waist as the position to carry smartphones. However, the requirement for rigid attachment and specified placement is incompatible with the way in which people use mobile devices. For example, over a period of a few minutes, a smartphone could be carried in the backpack and then shifted to a pocket, before being taken out and being used to send a text message. This may be one of the main reasons why it is so hard to conduct HAR using smartphone sensors.

Existing studies of sensor-based activity recognition often rely on supervised machine learning approaches such as Hidden Markov Model (HMM) , K-Nearest-Neighbors (KNN) , eXtreme Gradient Boosting (XGBoost), Random Forest (RF) and Support Vector Machine (SVM) using motion data collected from various types and quantities of motion sensors placed in different parts of body. However, these approaches are limited to three aspects: Firstly, due to the diversity and complexity of human activities, handcrafted feature extraction requires experience and expertise of the field. For the same reason, some extracted features show excellent performance in recognizing some activities, but rather bad at others. Secondly, even for the same activity, the waveforms of motion sensors are quite different in different smartphone placements. This makes it difficult to recognize various different activities with high precision. Thirdly, because of the differences in behavioral habits, gender, and age, the movement patterns of different people vary greatly, which enhances the difficulty of dividing the boundaries of different activities. The recognition accuracy tends to be limited due to confusing activities which generate similar motion signals.

Recent years have witnessed fast development and unparalleled performance in many areas (i.e. image recognition, natural language processing) of deep learning. There is a growing trend of discovering meaningful representations of raw data by Convolutional Neural Network (CNN). It has shown great performance in different domains for avoiding handcrafted features. Therefore, we present the ensemble framework based on CNN to recognize human activities. Without tiring data preprocessing and feature extraction and selection, we put raw data that is partitioned by the sliding window into our network. By fully mining the information carried by the signal, it can achieve more accurate recognition on the combination of arbitrary activities and devices placement.

This project presents a framework and performance analysis of smartphone-sensor based HAR. Sensor data from accelerometer, gyroscope and magnetometer were collected when participants performed some typical and daily human activities: going upstairs, going downstairs, running, walking, standing, bicycling and swinging. We then used the ensemble of CNN to recognize human activities, especially those easily confused. The experiments have demonstrated the improvement on recognition accuracy with the proposed approach. In summary, the key contributions are

- A novel approach based on the ensemble of CNN has been proposed to solve the confusion between highly similar activities such as going upstairs and walking, which outperforms the single CNN model and achieves 96.11% accuracy.
- Based on the collected data, we compare our model with the commonly used classifiers. The fact proves that the approach proposed in this paper outperforms other existing models in feasibility and efficiency.
- A huge amount of motion data including 235 977 data samples from various types of motion sensors and sports scenes with different participants and postures are collected to validate the effectiveness of the proposed method.

