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

Indoor pedestrian tracking cannot count on Global Positioning System (GPS) owing to its poor penetration. Therefore, researchers have proposed various radio frequency localization systems (i.e., Wi-Fi, Bluetooth, ibeacon, etc.) for the indoor environment, but all require installation of infrastructure beforehand. The burden of deploying beacons or landmarks falls on such systems, which is unrealistic in some conditions, especially in the rescue scene.

Pedestrian dead reckoning (PDR) with inertial measurement units (IMU), as the self-contained navigation system without the requirement for ambient conditions, is a justifiable solution for general indoor localization. Nevertheless, the inertial navigation system (INS) calculates the relative displacement of an object that will result in accumulated errors due to the sensors' drift. Stable trajectories could only maintain for a very short term using commercial IMU. To address this issue, foot-mounted IMU with zero velocity update (ZUPT) was proposed to eliminate the divergence of trajectory over time. The argument about attaching IMU to feet is that bipedal gait can split into two phases&#58; the stance phase and the swing phase. Under the assumption that the velocity is zero when the foot is stationary, it provides error-state Kalman Filter (ESKF), the drift corrector, pseudo-measurements to modify the position error.

The key to ZUPT with ESKF is precise zero velocity detection that distinguishes the stationary phase from each stride. Due to the complex differences in pedestrian motion patterns, the hope is that the zero velocity detector becomes robust for various individuals. While using other sensors besides IMU can realize precise detection, these systems tend to be intricate because of synchronizing each module. Utilizing the raw IMU readings only, we present a novel approach leveraging deep learning (DL) to detect zero velocity adaptively. Trained by massive foot-mounted IMU data from different individuals, the symmetrical Recurrent Convolutional Neural Network (RCNNs) can effectively learn the law of gait because the model takes the information from forward to backward of the undetermined time instant into consideration. The Convolutional Neural Network (CNN) and the Long Short-Term Memory (LSTM) in Symmetrical-Net extracts features and contextual information from input sequences, respectively. The proposed adaptive approach, unlike the conventional fixed threshold detector, requires no tuning on the optimal threshold, which will significantly elevate the applicability of ZUPT-aided INS. In summary, the main contributions of this project are as follows&#58;

- Robust and adaptive zero velocity detection&#58; Leveraging the neural network, more robust and adaptive zero velocity detection is realized compared with the fixed threshold. The symmetrical framework also guarantees precise detection regardless of motion types and individual differences.
- Accurate and robust pedestrian tracking&#58; Performance of zero velocity detector makes a profound impact on the trajectory reconstruction of the ZUPT-aided INS system. The navigation system utilizing our proposed zero velocity detection shows significant improvement in terms of tracking accuracy and robustness.
- Extensive real-world validation&#58; Huge numbers of experiments reveal that INS assisted by Symmetrical-Net keep the high tracking accuracy in multiple indoor and outdoor environments under three paces (i.e., walking, fast walking, and running). Outstanding improvements, especially in robustness, on zero velocity detection via the proposed model are corroborated.

