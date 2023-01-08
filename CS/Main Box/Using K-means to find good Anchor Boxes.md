---
aliases: []
---
## Content
[[Anchor box|Anchor boxes]] can be seen as priors. The different anchor box sizes can be handpicked but they can also be chosen using a [[clustering algorithm]] like [[k-means]].  

The centroids are the anchor boxes. It follows that the number of anchor boxes used is $k$. The distance metric is based on the IoU between the centroid and the ground truth bounding boxes used (usually a subset of the training set):
$$\begin{equation}
d(\text{box},\text{centroid}) = 1 - \text{IoU}(\text{box},\text{centroid})
\end{equation}$$
The reasoning is that we are trying to find the size of anchor boxes that best explain the sizes of all the bounding boxes.

## Tags
#external 

## Source
[[Redmon et al. (2016-b)]]
