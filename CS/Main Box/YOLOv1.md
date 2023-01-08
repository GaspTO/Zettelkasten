---
aliases: [yolov1, first yolo]
---
## Content
The YOLO network was built for [[Object detection]], with the idea of being a one stage detector in order to be faster than other methods. 

The YOLO network first divides an input image using a $S \times S$ grid. For each grid cell, several *bounding boxes* are used to detect objects. Each bounding box consists of 5 values: $x$, $y$, $w$, $h$, and *confidence.* The $x$ and  $y$ represent the center of the box relative to the bounds of the grid cell. The $w$ and $h$ represent the width and height (relative to the whole image). The *confidence* measures the likelihood an object is being detected by the bounding box.

At the same time, for each grid cell, the network outputs a *class probability vector*, predicting which class it is detecting. If the center of an object falls into a grid cell, that grid cell is responsible for detecting that object.

These two parts can now be put together and the *confidence* of a bounding box can be multiplied by the *class probability* of its grid cell, giving the probability that box is detecting a given class. We can then eliminate all boxes that fall with a lower probability than some threshold. For each grid cell with an object, it is expected that only one box has a high confidence for that object.
 
A summary of the model can be seen in the following image:
![[Pasted image 20221124184147.png|400]]


## Tags
#external 

## Source
[[Redmon et al. (2016-a)]]


