## Content
The [[Region Proposal Network]] was originally introduced for the [[Faster R-CNN]]. For this particular method, the input is a feature map, with $H \times W$ dimensions, that resulted from the pre-processing of an image.

A network slides through the feature maps using a $n \times n$ window (in this paper $n=3$)  with $d$ filters ($256$-d for ZF and $512$-d for VGG). Therefore, for each position the window passes, we get a $d$-dimensional vector. Two $1 \times 1$ convolutions are then used, separately, on this vector, one for the bounding box regression part and another for the object classification part.

The convolution for the regression has $4k$ filters, where $k$ is the number of [[Anchor box|anchors]] (all, of course, with the different formats), which defines $4k$ total bounding boxes. The one for classification has $2k$, where, for each $k$, the two positions are for the existence of object and for its opposite. In the paper, there was a softmax for each these pairs, for simplification.

In summary, for each sliding-window location, there are $k$ anchor boxes, whose locations are going to be adjusted by the regression part. Whether or not these boxes are going to be *proposed* depends on the classifier part.

By default $k == 9$.

For a feature map, there are $H \cdot W  \cdot k$ anchors.

## Tags
#external 

## Source
[[Ren et al. (2016)]]


