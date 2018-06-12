# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[lane1]: ./test_images_output/lane_solidWhiteCurve.jpg  "disrcret lane lines"
[lane2]: ./test_images_output/lane2_solidWhiteCurve.jpg "continuous lane lines"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps. The details are given as the following.
Step1: I converted the images to grayscale  
Step2: I make the gaussian smoothing  
Step3: I detect the edge by canny algorithm  
Step4: I set the region of interest which include the lanes  
Step5: I get the straight lines by hough transformation  
Step6: I merge the lane lines and the original image  

The hough transformation could only give me the disrcret line segments. For instance, one of them is shown here.  

![lane line segments][lane1]

In order to draw the continuous line on the left and right lanes, I modified the draw_lines() function by fitting the points in the hough line and calculation the lane line model and vertices. So, I could draw the continuous and more accurate lane line which is shown here.  

![lane line segments][lane2]

Moreover, I adjust some key parameters of hough transformation, such as threshold, minlen, maxgap etc, to get more lane lines and avoid some errors arised from the empty verteces of left or right lane. Finally, I apply the pipeline to the video and get the results that seems not bad.  

### 2. Identify potential shortcomings with your current pipeline


One shortcoming is that the lane lines drew by the pipeline seems not very stable sometimes.

Another potentialshortcoming could be that it can't process the shadows in the challenge video.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to adjust the canny and hough parameters to get better effects.

Another potential improvement could be to apply color mask to filter the pixels other than lanes.
