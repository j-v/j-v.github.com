---
layout: media
title: Real-Time Velocity Field Estimation with Kinect
categories: portfolio
image:
  teaser: kinect-velocity-field-400x400.jpg
---

As part of McGill course COMP558 - Fundamentals of Computer Vision, my teammate Beomjoon Kim and I used a Kinect sensor 
and the "optical flow" algorithm from OpenCV to obtain a velocity field of the sensor's surroundings. The intended application
is for a autonomous robot to be able to detect the flow of pedestrian traffic around it, in order to aid it in navigation.

<iframe width="420" height="315" src="https://www.youtube.com/embed/vdfnYbsoZQs" frameborder="0" allowfullscreen></iframe>

The implementation is coded in C++, and the computations are performed in real-time.