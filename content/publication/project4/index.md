---
title: "DeepAVO: Efficient Pose Refining with Feature Distilling for Deep Visual Odometry"
authors:
- Ran Zhu, Mingkun Yang, Wang Liu, Rujun Song, Zhuoling Xiao, Bo Yan
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2019-10-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2019-10-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "*IEEE Internet of Things Journal (under review)*"
publication_short: ""

abstract: Inertial navigation system (INS) is a practical method for indoor pedestrian navigation without pre-installation of infrastructure. Based on the fundamentals of human bipedal motion, zero velocity update (ZUPT) is a pervasive approach to tackle the accumulated error of inertial measurement units (IMU). While zero velocity detection plays a vital role in the algorithm, existing fixed threshold methods to pick these pseudo-measurements of error state Kalman Filter (ESKF) have the doubtful capability to fit various individuals in different motions. To address this issue, we propose the Symmetrical-Net leveraging deep Recurrent Convolutional Neural Networks (RCNNs) to detect the zero velocity interval adaptively. Additionally, two RCNNs are constructed in the symmetrical framework considering bidirectional IMU readings, which further improves the performance of the model. A comprehensive evaluation containing 87 different trajectories from 27 individuals has been conducted. The results show that the detection accuracy is up to 99.5% and 96.5% on the train and validation sets, respectively. It is verified that the precise and robust Symmetrical-Net can be a viable approach for the ZUPT-aided INS system.

# Summary. An optional shortened abstract.
summary: Inertial navigation system (INS) is a practical method for indoor pedestrian navigation without pre-installation of infrastructure. Based on the ...

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: 'media/DeepAVO.pdf'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
# url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---


