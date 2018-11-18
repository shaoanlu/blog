---
layout: post
title: Vehicle Detection with Mask-RCNN and SSD
date: 2017-11-02 00:00:00 +0300
description: Using deep learning models to detect vehicles in a video clips.
img: ssd-lane-detection-min.gif # Add image post (optional)
tags: [Deep Learning] # add tag
type: project
---

### [Description]

In this project, we used modern deep learning models, [SSD (Single Shot Multibox Detector)](https://arxiv.org/abs/1512.02325) and [Mask-RCNN](https://arxiv.org/abs/1703.06870), to detect vehicles in a video clip.

**SSD** is a single stage object detection algorithm that has VGG-16 as its backbone architecture. The model predicts several bounding boxes and classes on each anchor point within one forward pass. In our experiments, we used a SSD model pre-trained on VOC2007 dataset.

**Mask-RCNN** is another powerful object detection algorithm. Unlike SSD, it is a two-stage method, requiring a region-proposal operation followed by a per-proposal classification operation. In addition, Mask-RCNN also generates segmentation mask for each detected object. In general, two stage model are more accurate (have higher mAP) but are slower than single stage models like SSD as a trade-off ([source](https://arxiv.org/abs/1611.10012)). In our experiment, we used implementation from [matterport](https://github.com/matterport/Mask_RCNN), which has ResNet101 as backbone architecture and pre-trained weights on COCO dataset.

Furthermore, we also explored:
  1. The importance of the training dataset.
      - The quality of training data is crucial for deep learning models. 
  2. The benefits of increasing input resolution.
      - Increasing input resolution has very positive impact on segmentation results and small object detection. (Also shown in  [Kaggle Carvana competition](https://www.kaggle.com/c/carvana-image-masking-challenge/discussion).)
  3. How to smoothen bounding box over frames.
      - Moving average method is introduced to smoothen bounding box coordinate.
  4. Lane detection using traditional computer vision approach.
      - We applied color space transformation, peak finding, and polynomial fitting to achieve lane detection.
    
### [Results]

**SSD (with lane detection)**

![](https://shaoanlu.files.wordpress.com/2017/05/ssd-lane-detection-min.gif)

**Mask-RCNN**

![](https://shaoanlu.files.wordpress.com/2017/05/mask_rcnn_car_detection-min.gif)

##### Test video is from Udacity self-driving car nano degree program.
