---
title: Visual Odometry
summary: Efficient pose estimation with featuredistilling for deep visual odometry.
tags:
- Mobile Robotics
date: "2019-10-01T00:00:00Z"

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
url_pdf: "media/DeepAVO.pdf"
url_slides: ""
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#   slides = ""
---

From Unmanned Ground Vehicles (UGVs) to Micro Aerial Vehicles (MAVs), it is essential to know where autonomous robots are and to perceive the surrounding area. Global Positioning System (GPS) provides information about the position of the sensor in the world coordinate. However, a precise self-localization purely relying on the GPS is not sufficient for challenging environments like indoor scenarios and urban canyons. In this situation, a more precise measure or an alternative localization system is required in the real application for autonomous driving.

The camera is a small, light-weighted sensor that provides rich information about the environment around the sensing platform. It can recover the ego-motion from image sequences by exploiting the consistency between consecutive frames. Therefore, The concept of Visual Simultaneous Localization And Mapping (V-SLAM) and Visual Odometry (VO) are proposed to solve the well-known problem of positioning, which estimates vehicles' position relative to its start point. As an essential task in robotics and computer vision communities, VO has been widely applied to various applications, ranging from autonomous driving and space exploration to virtual and augmented reality. From the perspective of the camera used, the VO methods consist of two types: stereo VO and monocular VO. This work aims at investigating the monocular VO, for a single camera is cheaper, lighter, and more general than a stereo rig. Especially when the ratio of stereo baseline to depth is minimal, the stereo VO degenerates to the monocular one.

Over the past thirty years, enormous work has been done to develop an accurate and robust VO system. The traditional VO algorithms can be divided into the feature-based method and the direct method. Feature-based methods typically consist of camera calibration, feature detection, feature matching, outlier rejection (e.g., RANSAC), motion estimation, scale estimation, and optimization (e.g., Bundle Adjustment). Unfortunately, how to detect appropriate features for recovering specific motions remains a challenging problem. Handcrafted feature descriptors such as SIFT, ORB  designed for general visual tasks, lack the response to motions. Instead, extra information that is guided by geometric prior such as planar structures and vanishing points, is used for camera pose estimation in specific environments, providing promising performance but limited generalization ability. Unlike feature-based methods, direct methods track the motion of the pixel and obtain pose prediction by minimizing the photometric error, so it is extremely vulnerable to light changes. Moreover, the absolute scale estimation in the traditional monocular VO must use some extra information (e,g., the height of the camera) or prior knowledge.

The emerging Deep Learning (DL), a data-driven approach, has yielded impressive achievement in the computer vision. Rather than handcrafted features, DL that has the ability to extract deep features from the plain input, encodes the high-level priors to regress camera poses. Compared with traditional VO, learning-based VO has the advantage of low computation cost and no need for internal camera parameters. A few methods on DL have been proposed for camera motion recovery, such as DeepVO, ESP-VO, SfmLearner, and GeoNet. While achieving promising performances, they do not take into account the different responses of visual cues and the effect of pixels movement in different directions in the input image to the camera motion, thus may output trajectories with large error. For learning-based VO, it should focus more on geometric constraints than the "appearance'' information when harnessing Convolutional Neural Networks (CNNs) to extract features. Optical flow, as the representation of the geometric structure, has been proved useful for estimating Frame to Frame (F2F) ego-motion. Therefore, we take the optical flow as input to the proposed model.

Guided by the previous considerations, we explore a novel strategy for performing visual ego-motion estimation in this work. Here, we extend the network into four branches focusing on pixels movement in different directions in the optical flow and then regress the global feature concatenated from the four outputs to obtain F2F motion estimation. In particular, features extracted by each branch have been distilled by using the attention mechanism to refine estimation. In this project, many quantitative and qualitative experiments in terms of precision, robustness, and computation speed are conducted. The results demonstrate that the proposed model outperforms many current monocular methods and provides a competitive performance against the classic stereo VO. In summary, our key contributions are as follows&#58



- Novel visual perception guiding ego-motion estimation&#58 By considering the four quadrants in optical flow and fusing the distilling module into each branch encoder, the learning-based DeepAVO model pays more attention to the visual cues that are effective for ego-motion estimation.
- Lightweight VO framework with enhanced tracking performance&#58 The proposed DeepAVO model framework yields more robust and accurate results compared with competing monocular VOs. The F2F VO calculation can be done within 12 ms, making it practical and valuable in real-world applications.
- Extensive fresh scenes validation&#58 The DeepAVO produces promising pose estimation and maintains high-precision tracking results on the 11-20 sequence of the KITTI dataset and the Malaga dataset. Outstanding improvements in the accuracy and robustness of VO are further demonstrated.

