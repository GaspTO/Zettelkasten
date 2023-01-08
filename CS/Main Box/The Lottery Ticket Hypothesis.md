---
aliases: [lottery ticket hypothesis, winning ticket, winning tickets]
---
## Content
According to the **Lottery Ticket Hypothesis**, a [[Artificial Neural Network|neural network]] can be seen as the composition of smaller neural networks. This hypothesis states that the success of a network in a given problem is due to the lucky initialization of the weights of one of these subnetworks Winning Ticket.  These subnetworks (with the proper initialized weights) could be trained in isolation and achieve similar results as the original one by themselves alone (when trained by, at most, the same number of epochs).

**This would explain** the fact that [[Networks can be pruned extensively without harming accuracy]], up to 90%. However, the architectures discovered during [[Network pruning]] do not perform nearly as well when training from scratch (different weight initialization). 


## Tags
#external 

## Source
[[Frankle et al. (2018)]]