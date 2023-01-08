---
aliases: []
---
## Content
In [[Object detection]], the feature maps in which the detection stage happens should have enough detail to help performance. Say we get a $k \times k$  feature map, one way to provide more fine-grained features would be to get a previous feature map and concatenate it to the original one. If the feature map used is not of the same dimensions, it can be broken down and stacked in the channels dimensions. For example, a $2k \times 2k \times 25$ would be transformed into a $k \times k \times 100$ feature map.

This resembles [[Residual connection|residual connections]], except we are concatenating and not adding.

#todo - [[Feature Fusion Product]]

## Tags
#external 

## Source
[[Redmon et al. (2016-b)]]