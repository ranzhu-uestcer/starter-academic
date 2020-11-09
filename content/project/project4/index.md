---
title: Loop Closure Detection 
summary:  A loop closure detection method using adaptive weighted similarity matrix.
tags:
- Mobile Robotics
date: "2019-09-15T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
- icon: envelope
  icon_pack: fas
  name: Contact
  mailto: zhu_ran@outlook.com
url_code: ""
url_pdf: "media/MetricNet.pdf"
url_slides: ""
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#   slides = ""
---

Visual simultaneous localization and mapping (vSLAM) that simultaneously recovers camera pose and scene structure from video, as one of the key autonomous positioning and navigation technologies in areas where GPS fails or cannot be covered, is gaining importance in robotic applications such as autonomous cars or unmanned aerial vehicles. Loop Closure Detection (LCD), considered one of the essential parts in the visual SLAM system, is designed to recognize previsited areas by an autonomous mobile robot according to the image information collected by the visual sensors during the moving so also known as visual place recognition. Accurate LCD methods offer precise pose estimation by introducing extra constraints to correct the trajectory drift over time, improving the system performance. However, there are still two common challenges&#58 1) the same place has different appearances at different times due to change of illumination and weather; 2) different scenes look similar for reasons such as sharing common objects. Therefore, an excellent LCD method needs to resolve these two problems to detect more correct loops.

In the field of vSLAM, the appearance-based methods treating LCD as an image matching problem compare the similarity between the current image and previous images. If the similarity between them is sufficiently high to exceed a given threshold, we can regard it as a loop closure. As one of the most popular LCD approaches, it can be divided into two crucial steps: feature generation and similarity measurement.

In the vSLAM system, image feature extraction forms the basis of a series of tasks, such as keyframe extraction, tracking, positioning, and map construction, which have a decisive influence on the robot’s autonomous positioning. The traditional appearance-based methods mainly follow the visual bag-of-words (BoWs) model, which uses a clustering procedure on a training sample of local features and quantizes the descriptor space into Visual Words (VWs). However, this approach uses hand-crafted traditional features. Most of these features discard certain geometric and structural information, making it difficult to cope with the challenges such as camera motion and illumination changes. Moreover, BoWs relies on specific environments and has poor robustness to different application scenarios. In recent years, deep learning has made significant breakthroughs in the field of computer vision. Much related research demonstrates that the deep features learned by convolutional neural networks (CNNs) can provide more robust image representations in changeable environmental conditions, especially when illumination change and viewpoint variation. Besides, the network models trained for specific tasks can be transferred to other tasks successfully. Some classic pre-training network models’ availability makes it more convenient to complete various feature extraction tasks. Based on the above reasons, researchers began to apply CNNs to LCD. Although good results have been achieved, these works paid little attention to similarity measurement strategies, which also play a crucial role in image matching tasks. Fixed pre-specified distance metrics such as Euclidean distance or cosine similarity are commonly used. Moreover, feature extraction exists independently of similarity measurement, its effectiveness severely restrains the similarity measurement’s effect. For these reasons, further improvement of detection precision is hindered.

This project proposes a two-branch end-to-end network called MetricNet that performs LCD based on the adaptive weighted similarity matrix, jointly optimized with feature extraction, to address the issues mentioned earlier. In summary, the key contributions are as follows&#58



- Adaptive feature selection and similarity matrix&#58 By using the channel weighting to remove the irrelevant background information and a weighted similarity matrix to adaptively select spatial information, MetricNet has been proved to be more robust and accurate than competitive models in both theory and practice.
- An end-to-end LCD framework&#58 this research also proposes a novel LCD framework that encompasses both feature extraction and similarity measurement to extract more effective representation. The learning-based MetricNet can achieve a recall rate up to 47.08% under 100 precision.
- Extensive multi-dataset validation&#58 MetricNet has proved its excellent performance on three typical open datasets under drastic illumination and seasonal variations. Outstanding improvements in detection accuracy and generalization ability are also further demonstrated.

