---
aliases: [spatial pyramid pooling layers, spp, spps , spp layer, spp layers]
---
## Content
The SPP Layer is a [[pooling layer]] that transforms feature maps of all dimensions into a fixed-sized feature map. Different input sizes can then be used.

It works by establishing first a fixed-length vector, with $n$ size. Then we divide that vector into different parts, where each *part* can have different sizes. Obviously, summing the sizes of each part adds up to $n$.

For a $k$ sized part, we define a $\sqrt{k} \times \sqrt{k}$ *grid*, where each position is called a *bin*. The grid will then be matched against the input in such a way that each bin will be responsible for a different *square* part of the input. For example, if the input has $100 \times 100$ dimensions and the grid has $2 \times 2$ dimensions, then each grid bin will be responsible for  $50 \times 50$ input squares. In each one of these bins, a [[pooling operation]] is executed to reduce each input squares to one single value. In this way, a the bigger the input, the bigger the input squares per bin, but the output of each grid has always the same dimensions. 

For each part of the fixed-length vector, there is a different grid. The bigger the part, the bigger the grid and the finer the features captured. 

A scheme of the spatial pyramid pooling layer is shown below:
![[Pasted image 20221211194043.png|400]]



## Tags
#external 

## Source
[[He et al. (2015)]]