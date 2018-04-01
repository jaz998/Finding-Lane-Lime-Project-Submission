Overview
---
The pipeline is for the *Finding Lane Lines on the Road* project of the Udacity self-driving car nanoddegree. It is used to detect lane lines of any color in images and videos in bright day time conditions. 



Pipeline
---
The pipeline makes a copy of the original image. And then the image is converted from RGB to grayscale (one color channel), after which a Gaussian Noise Kernel is applied. And then Canny edge dection is applied to the image. After that, Hough Transform is used to detect the lines. 

The points lines detected by Hough Tranform are then separated into those belong to left lane line and those belong to right lane line. Then a Least squares polynomial fit are applied to the points in order to draw the left lane line and right lane line. 
  
  
Shortcomings
---
In videos, the non-continuous line sometimes gives the impressions that it is flashing (or shaky), though the line is detected on each frame - this is probably due to there is sudden major change of the line.  

Another shortcoming is that the pipeline does not work on the challenge video. 


Possible improvements
---
For the first shortcoming mentioned above, current frame can be averaged out with previous frame(s) to smooth the non-continuous line. 

For the second shortcoming, the region of interest may be optimised to fit the Challenge video. In addition, color can be introduced as a condition for line detection so the only lines in certain color are detected as lane line. 