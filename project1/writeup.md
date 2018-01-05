**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.  
step one: I converted the images to grayscale.  
![image](https://github.com/elonshi/udacity/raw/master/project1/images/grayscale.png)  
step two: used a 5 order Gaussian Filter to reduce image noise.  
![image](https://github.com/elonshi/udacity/raw/master/project1/images/gaussian_filter.png)  
step three: used the canny edge detection algorithm to detect the edge of the image.  
![image](https://github.com/elonshi/udacity/raw/master/project1/images/canny_edges.png)  
step four: selected the area of interest in the image.  
![image](https://github.com/elonshi/udacity/raw/master/project1/images/region_mask.png)  
step five: used the hough transform algorithm detect the Lane lines on the road.  
![image](https://github.com/elonshi/udacity/raw/master/project1/images/hough_transform.png)  
In order to draw a single line on the left and right lanes, I modified the draw_lines() function by three steps:  
step one: distinguish the points belonging to the left lane line and the points belonging to the right lane line 
          according to the positive and negative slope of the slope.  
step two: iterative calculate the mean value of the slope until the difference between each slope value 
          and the mean slope value is less than delta.  
step three: calculate the vertices of the left lane line and the right lane line respectively.  

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when the area where the lane line is located is not fixed. 

Another shortcoming could be the lane line is a straight line.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to adding appropriate algorithms.

Another potential improvement could be to improve the applicability of pipeline.
