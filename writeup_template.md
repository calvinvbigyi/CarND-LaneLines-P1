# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps.
1. First convert the orignal image to grayscale
2. Perform Gaussian Blur to smooth the image and make the edges more detectable
3. Perform Canny Edge detection with tuned parameters
4. Select the region of interests
5. find out the hough lines and draw them
6. in the end, combined the grayscale image with edge detected and the original image

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 
distinguishing leftlane line and rightlane line using their slopes
and then do the extrapolating with the maximum top line end and maximum top line point with right and left respectively

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

The draw_lines method is half broken due to a unexpected error when doing extrapolating lines.
Thus, very unfortunately, P1.mp4 is not achieved, But The line segment detection is wokring fine. I will try my best to get to that point


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to fix the draw_line method
