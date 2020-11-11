---
title: Zero Velocity Detection
summary: Adaptive zero velocity detection for ZUPT-aided pedestrian navigation system.
tags:
- Pedestrian Positioning
date: "2019-09-01T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
- icon: envelope
  icon_pack: fas
  name: Contact
  link: "zhu_ran@outlook.com"
url_code: ""
url_pdf: "media/Symmetrical-Net.pdf"
url_slides: ""
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#   slides = ""
---

Based on the fundamentals of human bipedal motion, Zero Velocity Update (ZUPT) is a pervasive approach in Pedestrian dead reckoning (PDR) to tackle the accumulated error of IMU. The key to ZUPT is precise zero velocity detection that distinguishes the stationary phase from each stride. Besides, due to the complex differences in pedestrian motion patterns, the hope is that the zero velocity detector becomes robust for various individuals. We present a novel approach leveraging deep learning (DL) to detect zero velocity adaptively. Trained by massive foot-mounted IMU data from different individuals, the symmetrical Recurrent Convolutional Neural Network (RCNNs) can effectively learn the gait law because the model takes the information from forward to backward of the undetermined time instant into consideration.

