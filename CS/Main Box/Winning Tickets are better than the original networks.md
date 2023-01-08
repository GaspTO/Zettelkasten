---
aliases: []
---
## Content
These experiments were made to understand the quality of different [[Winning Ticket|winning tickets]] as compared to their original network. The following experiments were done by training LeNet on MNIST at different pruning percentages:
![[Pasted image 20221212234431.png|600]]
As seen, in the left figure, the original network (blue) gets worse results than one with 21.1% of the original weights. 

However, reducing more than this deteriorates the performance, and it can even become worse than the original (1.9% brown).

The ones that achieve better results also need less iterations to get the same performance as their counter-parts.

## Tags
#external 
#assertion 

## Source
[[Frankle et al. (2018)]]