# **Finding Lane Lines on the Road** 

---

## Introduction

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

## Reflection

### 1. Describtion of pipeline.

My pipeline consisted of 6 steps.
1. Converted the images to the gray images
2. Applied a Gaussian Noise kernel to remove the noises
3. Applied the Canny transform to detect the edges
4. Retained the trapezoid area in front of the car
5. Applied the Hough transform to remove short and useless edges
6. Fit the lane line and generate the start and end point of the fitted line

In order to draw a single line on the left and right lanes, I modified the draw_lines() function
1. Calcaulate the slope of every line
2. Process the left and right lines separately
3. Use numpy.polyfit() to fit the left and right lines
4. Draw the lines separately

### 2. Potential shortcomings with the pipeline

One potential shortcoming would be what would happen when the vehicle makes a turn.

Another shortcoming could be that it can not deal with the situation when the car run in the bad weather or in the night


### 3. Possible improvements to the pipeline

A possible improvement would be to to use curve instead of straight line to describe the lane

Another potential improvement could be to use machine learning to adjust the parameters of Hough transform etc.
