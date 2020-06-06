---
layout: post
title: Object Detection: Is SOTA really the best?
date: 2017-09-12 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: mac.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Productivity, Workflow] # add tag
---

Since the past few days, I have been trying to get a hang of object detection and which architecture should one use if an individual wants to get his hands dirty.

My first instinct was to look for State Of The Art (SOTA) techniques, understand their architecture and implement them on public datasets by myself. (Easier said than done eh?)

When I started looking for tutorials, I realized that Faster RCNN was the most in-use architecture. I figured that must be because it is SOTA. To my utter surprise that was not the case. In reality, Faster RCNN was hard to find in the pecking order. That got me wondering why it is still used so widely if it is not SOTA (or anywhere near it) anymore.

![I and My friends]({{site.baseurl}}/assets/img/objdet_comparison.jpeg)

On doing some research and discussing the issue with peers I realised that there are many factors contributing to it.

1) The pre-trained model of Faster RCNN is available in both PyTorch and TensorFlow model zoo which makes it the easiest to implement of all architectures.

2) Faster RCNN can be made good enough for general tasks by making a few tweaks like changing backbone, introducing FPN or TDM in its architecture.

3) Faster RCNN is actually fast. So much that it can be used for real-time object detection. (A feature not many architectures possess).

4 ) Professionals spend most of their time on dataset creation rather than implementing modern vision models. Getting the dataset of high quality is the most important thing. Once you have that, you want to rely on models that can be reproduced, be extended in many different ways and be deployed in production. FRCNN is all of that. Given a deadline would you rather: spend time on a new model with 1-2 % gains (which are sometimes hard to reproduce) on CoCo vs spending time on gathering more data?

So, all in all, Faster RCNN is a pretty robust and decent choice for object detection, more so if you are just starting out.
