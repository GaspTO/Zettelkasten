---
aliases: [yolov2 anchor boxes]
---
## Content
YOLOv2 uses anchor boxes. Here's the details:
* **[[Anchor box|Anchor boxes]]**: (**Convolutional with Anchor Boxes**) When changing to anchor boxes, YOLOv2 no longer predicts the class for multiple bounding boxes, but predicts the class for each anchor/bounding box. [[YOLOv1]] predicted 98 bounding boxes per image, while YOLOv2 predicts more than a thousand.  The anchor boxes act on a $13\times13$ feature map.
* **[[Anchor Box Location Prediction relative to Grid Cell]]** (**Direct location prediction**). Unlike [[Region Proposal Network|region proposal networks]], the values predicted are not offsets of the anchors, since these are unbounded. Instead, they are given by a logistic regression, between 0 and 1, that, just like [[YOLOv1]], predict location coordinates relative to the location of the grid cell.
* **[[Using K-means to find good Anchor Boxes]]** (**Dimension Clusters**). They find $k=5$ to give the best trade-off between recall and model complexity.

## Tags
#external 

## Source
[[Redmon et al. (2016-b)]]