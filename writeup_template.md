# **Finding Lane Lines on the Road** 


**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 
First, I converted the images to grayscale, then I apply Gaussian smoothing in to the grayscale image. Thirdly, I define parameters for Canny Edges, the mask. Then, I apply a four sided polygon to the mask and apply Hough transform onto the masked edges image. Finally, I draw two lines (one left, one right) on the image and combine them together.

In order to draw a single line on the left and right lanes, I created a new function slope_lines() function by firstly calculate the slope and intercept of both lines, and then convert the slope and intercept into pixel points.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be pipelines would not follow the right direction when the detecting line segment are incomplete.

Another shortcoming could be the pipelines are highly affected by the noise on the road or any noise detected by the camera.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to find the correct and complete lane lines nor the lane dots.

Another potential improvement could be to clear all the possible noise that the camera can detect.
