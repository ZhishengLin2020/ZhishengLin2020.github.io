---
title: "3D Human Pose Estimation in 2D Video"
excerpt: "This project performs 3D human pose estimation from 2D videos. Given a 2D video of a person, the main idea of 3D pose estimation is to detect 3D locations of the person's joints, which form a “skeleton”.<br/><img src='/images/pose_estimation.gif'>"
collection: portfolio
---

# Overview
Human Pose Estimation is about estimating 2D and 3D localization of human joints in images or videos. In our project, we perform 3D human pose estimation from 2D videos. Given a 2D video of a person, the main idea of 3D pose estimation is to detect 3D locations of the person's joints, which form a “skeleton”. It has applications in human action recognition, motion capture, interesting mobile applications, sport, augmented and virtual reality, robotics, etc. It is an important step towards understanding people in images and videos. We realized this process through 2 steps, one is using Detectron2 to detect the 2D joint keypoints from an arbitrary 2D video, the other one is applying [a pre-trained temporal CNN](https://github.com/facebookresearch/VideoPose3D) for predicting 3D joint keypoints from 2D keypoints. See codes [here](https://github.com/ZhishengLin2020/ee435-deep-learning-foundations-from-scratch/tree/master/Final%20Project).
