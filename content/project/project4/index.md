---
title: Loop Closure Detection 
summary: A loop closure detection method using adaptive weighted similarity matrix.
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

Loop Closure Detection (LCD), considered a key optimization part in the visual SLAM system, aims to recognize the places where a mobile robot previously visited. Correct loop closure detection benefits visual SLAM systems a lot because it can significantly reduce the position errors that accumulate over time. It enables the system to build a consistent map of the environment. We introduce the adaptive weighted similarity matrix by combining the feature extraction module and similarity measurement module to focus on changing appearance over time. Experiments on three typical open datasets are conducted to verify the feasibility of the proposed model.

