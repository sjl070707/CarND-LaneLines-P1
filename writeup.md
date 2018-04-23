# **Finding Lane Lines on the Road** 

## Writeup Template

---

**Finding Lane Lines on the Road**

<!-- The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report -->


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg "line"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 

1) convert img to grayscale  
2) apply gaussian filter for canny to pickup the edges  
3) apply canny to detect edges  and focus only on the region of interest
4) apply hough transform
5) detect left and right lane by comparing the slopes and decting intercept in hough space


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline
1) this approach would have hard time detecting fast curve of the road due to the slope detection I implemented    
2) if the camera is facing the downhill, my region of interest would only cover small portion of the roads  
3) night condition of the road would have different reflection on the road thus might cause different result in detection   


### 3. Suggest possible improvements to your pipeline
1) with gyroscope sensor data, we could apply different threshold for region of interest  
2) with lighjt sensor, we could apply different threshold for the low and high light threshold
