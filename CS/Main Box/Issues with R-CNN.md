---
aliases: [problems with r-cnn, r-cnn's problems]
---
## Content
The [[R-CNN]] has several drawbacks that motivated faster versions of it:
1. Training is a multi-stage pipeline. First CNNs are trained, then SVMs,  then bounding-box regressors.
2. For SVMs and bounding-box regressors, features are extracted for every object proposal for each image. These features are then written to disk as they become training data and they require hundreds of gigabytes.
3. r-cnns took, when proposed, 47 seconds, for a test image, using a VGG-16 as the backbone.

R-CNN is slow because it performs a forward pass for each object proposal, without sharing computation. 2000 regions are passed one at a time.

## Tags
#external 
#potential-links 

## Source
[[Girshick (2015)]]


