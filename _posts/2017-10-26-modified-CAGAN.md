---
layout: post
title: Generative Adversarial Networks for Garment Swapping
date: 2017-10-26 00:00:00 +0300
description: A modified CAGAN (conditional analogy GAN) to swap clothes.
img: cagan_flow_chart2.jpg # Add image post (optional)
tags: [Software, GAN] # add tag
type: project
---

### [Description]
In this project, we developed **generative adversarial networks (GAN) for garment swapping** which combined [CAGAN](https://arxiv.org/abs/1709.04695) with architectures introduced in [StackGAN++](https://arxiv.org/abs/1710.10916), and [SENet](https://arxiv.org/abs/1709.01507). Our improved model leverages multi-scale archtecture and generates images with higher fidelity. We also explored several approaches to stablize training, such as adding an idendity cyclic loss and concatenating conditioning images to every intermediate layers.
For more details please refer to [this blog post](https://shaoanlu.wordpress.com/2017/10/26/reimplement-conditional-anology-gan-in-keras/).

---
### [Architecture]
![](https://shaoanlu.files.wordpress.com/2017/10/ca-stack-gan1.jpg)

---
### [Cherry-picked results]

Given three input images: 
  - human wearing cloth A (x_i)
  - stand alone cloth A (y_i)
  - stand alone cloth B (y_j)
  
Our model generates a human image wearing cloth B (x_ij). See figures below.

![](https://shaoanlu.files.wordpress.com/2017/10/format.jpg)

![](https://shaoanlu.files.wordpress.com/2017/10/intra-1.jpg?w=788)

![](https://shaoanlu.files.wordpress.com/2017/10/sleeves-2.jpg?w=788&h=236)

![](https://shaoanlu.files.wordpress.com/2017/10/graphics-2.jpg?w=788&h=236)

##### (Due to copyright concerns, input images are replaced by illustrations.)
---
### [More results]

![](https://shaoanlu.files.wordpress.com/2017/10/others.jpg?w=788)

##### (Due to copyright concerns, input images are replaced by illustrations.)
