Overview
---
The pipeline is for the *Finding Lane Lines on the Road* project of the Udacity self-driving car nanoddegree. It is used to detect lane lines of any color in images and videos in bright day time conditions. 



Pipeline
---
The pipeline makes a copy of the original image. And then the image is converted from RGB to grayscale (one color channel), after which a Gaussian Noise Kernel is applied. And then Canny edge dection is applied to the image. After that, Hough Transform is used to detect the lines. After the detection of the lines, the lines are overlaid onto the original image. 
  
  
Shortcomings
---
In videos, the lines give the impressions that they are flashing, though each lines are detected on each frame - it gives the appearance that lines are dropped on certain frames. This is probably due to that the non-continuous lane line lacks the uniformity (e.g. compared to the continuous lien).

Another shortcoming is that for the second video, the draw_liens function (used to average/extrapolate the line segments) make the continous line a lot longer than the non-continuous line.


Possible improvements
---
For the first shortcoming mentioned above, it may be possible to introduce time delays of line display on each frame to give the visual appearance that the line overlaying is constant.

For the second shortcoming, it may be possible to introduce lengh limits of the lines so that left lane line drawn will not be much differnt in length compared to the right lane drawn, or vice versa.  
