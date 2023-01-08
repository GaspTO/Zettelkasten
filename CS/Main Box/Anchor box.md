---
aliases: [anchor boxes, anchor, anchors]
---
## Content
During [[Object detection]], during a convolution, at each sliding-window location, it is possible to evaluate multiple possible regions of interest. For a particular location, multiple shapes of regions are considered, all centered in that location. Usually, at each point of the sliding window, a network, shared across all points, outputs the confidence about the existence of an object and the coordinates for the predicted bounding box. The anchor box is only relevant during training, where it decides which ground-truths belong to it. Different shapes and sizes will get different target grounding truths. 

As seen in the following image on the right, the sliding window is at a particular point of the feature map and the network will consider multiple anchor boxes. If you look at the right image, you see that there are multiple objects recognized by  different sized boxes.
![[Pasted image 20221123224240.png]]

## Tags
#external 

## Source
[[Ren et al. (2016)]]


