---
aliases: [yolo v2]
---
## Content
The YOLOv2 is a system for [[Object detection]], which results as a direct improvement from [[YOLOv1]].  

**The main model differences are:**
* [[YOLOv2 Anchor box|anchor boxes in YOLOv2]]. 
* It uses [[finer-grained features by concatenating a previous feature map]].  As said in the anchor section, the anchors act in a $13 \times 13$ feature map (as opposed to a $7 \times 7$ in [[YOLOv1]]). To make the feature map more fine-grained, a $26 \times 26 \times 512$ feature map from a previous layer is transformed into a $13 \times 13 \times 2048$ feature map and concatenated with the original one. 
* The [[Darknet-19]] is used as a backbone.
* Compared to [[YOLOv1]], YOLOv2 introduces [[Batch Normalization]].
* The network can handle better inputs of different sizes due to the way the classifier was trained.



## Tags
#external 

## Source
[[Redmon et al. (2016-b)]]