---
aliases: []
---
## Content
This refers to the idea of doing multiple pruning sequences to a network in order to get the final pruned network. In [[Frankle et al. (2018)]], 

0) the network's weights are initialized
1) the network is trained
2) $x\%$ of the weights are pruned
3) the unpruned weights are restored **to the same starting weights as in 0)**
4) go back to 1) and repeat for $n$ iterations


## Tags
#external 

## Source
[[Frankle et al. (2018)]]