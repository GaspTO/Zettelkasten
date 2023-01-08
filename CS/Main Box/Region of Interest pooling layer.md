---
aliases: [region of interest pooling layers, roi pooling layer, roi pooling layers, roi layer, roi layers]
---
## Content
The RoI pooling layer is responsible for extracting a fixed vector from a convolutional feature map using a region of interest. 

This layer is a specific case of the [[spatial pyramid pooling layer]], using only one pyramid level.

RoIs can have whatever dimension they want and are defined by 4 values $(r,c,h,w)$, where $r$ and $c$ define the left corner where it starts and $h$ and $w$ define its size.

The way it works is by defining the resulting dimensions before hand, say $H \times W$.   A grid will be created over the  convolutional feature map on top of the coordinates defined by the region of interest  , where there will be $H \times W$ sub-window, inside each there will be a [[Max pooling]] operation. The size of each sub-window is therefore $h/H \times w/W$.


## Tags
#external 

## Source
[[Girshick (2015)]]


