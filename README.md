# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project I will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

To complete the project, two files have been submitted: a file containing project code (P1_cai.ipynb) and a file containing a brief write up (writeup_cai.md) explaining the solution. 

The results are included in the test_images_output and test_videos_output. In the simple scenario, the lane lines could be detected easily and accurately. But, if there are lots of shadows on the road, the algorithm may failed. More factors should be considered to refine the pipeline.

Environment
---
The pipeline could run on the jupyter notebook. Of course, the neccesary packages should be installed, such as numpy, opencv, matplotlib etc.
I use anaconda to configure the python(ver3.6) environment.