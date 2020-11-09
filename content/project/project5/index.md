---
title: Loop Closure Detection 
summary:  A loop closure detection method using adaptive weighted similarity matrix.
tags:
- Pedestrian Positioning
date: "2019-09-14T00:00:00Z"

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
url_pdf: "media/VI-MapMaching.pdf"
url_slides: ""
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#   slides = ""
---

Map-based indoor localization that reconciles the observations with the constraints provided by the maps in order to estimate the most trajectory, has drawn much attention in both civilian and military fields during the last decade. Unlike outdoor localization, it cannot adopt the Global Navigation Satellite System (GNSS) owing to poor penetration. From the perspective of the pre-deployment hardware, indoor localization methods can be divided into two types&#58 deployment-dependent and deployment-independent positioning. A disadvantage to all deployment-dependent positioning methods is the tediousness and delicacy of the deployment process. In a typical deployment processes, a trainer should perform a careful survey of the environment. This includes going to a certain locations, collecting the value of some type of signals and repeating this for probably a large number of points whose locations are known by accurate measurements. This implies several hours or even days of data collection for radio-map of buildings. Most deployment-dependent algorithms need to update databases or maintain equipments. This requires a lot of manpower and material investment. additionally, deployment-dependent positioning will fail in specific scenarios where the facility cannot be deployed in advance. Therefore, this work focuses on map-based deployment-independent indoor positioning.

As the key to providing accuracy indoor location, the map can be viewed as a geometric information providing spatial constraints. A floor plan of a building calibrates the movement of a user. For example, people can only enter the room through the door, not through the wall. However, most existing map matching methods rely on the external information of prior site survey or initial positions provided by users, which makes it challenging to meet on-demand localization requirements. Researchers have investigated the possibility of reducing reliance for initial positions. 

Inspired by the state-of-the-art researches, we explore a novel strategy for performing deployment-independent indoor positioning in this work. Here, we adopt easily accessible information such as floor plan and simple real-time images captured by smartphones to realize the user positioning by utilizing object recognition, video feature matching, and topological graphic matching all based on deep learning. In particular, topological graphic matching is based on the three-dimensional structure recovered from the floor plan and the spatial information directly extracted from the environmental picture. In summary, the main contributions of this paper are as follows&#58

- On-demand positioning system without initial constraint&#58 We design an indoor positioning system only utilizing map, Inertial Navigation System (INS) and videos to provide ON-DEMAND positioning service. Neither prior site survey nor initial positions from external information is needed.
- Novel matching method guiding pedestrian positioning&#58 A novel method based on architectural perspective theory is designed to recover three-dimensional structure from floor plan. Besides, a Siamese Network has been employed to match the recovered three-dimensional structure with spatial information extracted from smartphone cameras.
- Extensive experiments validation&#58 The proposed system demonstrates its performance in terms of tracking accuracy and robustness with a huge number of real-world experiment data in three different experiment scenarios.

