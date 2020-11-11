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
  link: mailto:ranzhu@std.uestc.edu.cn
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

To build an intelligent robotic positioning system that can more efficiently deal with the traditional SLAM problems such as camera calibration, monocular scale ambiguity, we explore a novel strategy for performing visual ego-motion estimation based on deep learning. Here, we extend the model into four branches focusing on pixels movement in different directions in the optical flow and then regress the global feature concatenated from the four outputs to obtain F2F motion estimation. In particular, features extracted by each branch have been distilled by using the attention mechanism to refine estimation. Experiments on the KITTI and Malaga benchmark datasets demonstrate that the proposed model outperforms state-of-the-art monocular methods by a large margin and produces competitive results against the classic stereo VO algorithm, which also highlights its promising generalization ability.

