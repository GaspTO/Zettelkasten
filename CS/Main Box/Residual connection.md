---
aliases: [residual connections, shortcut connection, shortcut connections]
---
## Content
The idea of residual connections is to merge a feature of some layer to another that comes from a previous one ([[Feature Map Fusion]]). In this way, feature maps computed by a particular layer, not only advance to the next layer, but to others much further, as shown by the following scheme:

![[Pasted image 20221121013846.png|300]]


The hypothesis is that it is easier to optimize the [[Residual function]], $F(x)$, than the original desired one from scratch (without using the input, $x$, as a starting point).

## Tags
#external

## Source
[[He et al. (2016)]]



