---
aliases: []
---
## Content
In this [[Feature Map Fusion|feature fusion technique]], there is an order associated to the feature maps, since the ones merges belong to feature maps of layers of the same network.

To create a new feature map at depth $n$, the original feature map at that depth goes through a $1 \times 1$ convolution, mostly to reduce or expand to a specific number of channels. Then, the next feature map, at depth $n+1$, will be upsampled to match the previous' dimensions (using the nearest neighbor for simplicity). Finally these two feature maps are added together element-wise ([[Unweighted Feature Addition|feature map addition]]) and form the new feature map at depth $n$.

A scheme can be seen in the following image:
  ![[Pasted image 20221211171235.png|300]]

## Tags
#external 

## Source
[[Lin et al. (2017)]]