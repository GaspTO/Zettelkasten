---
aliases: []
---
## Content
[[Frankle et al. (2018)]] compares both [[One-Shot Pruning]] and [[Iterative Pruning]] strategies at the quality of the [[The Lottery Ticket Hypothesis|winning tickets]] found.

The experiments are done on MNIST, using [[Fully Connected Neural Network|fully connected networks]]. They apply either the iterative or one-shot strategy until getting the desired percentage of pruned weights, then train the winning ticket until an early-stop condition (which is the iteration of minimum validation loss) as a proxy for measuring how fast it takes a network to train. The following graphs have more information than needed. We're only interested in winning tickets, so we'll be analyzing the blue and green curves.

**The iterative (blue) is considerably faster at achieving the early stop condition than the one-shot method (green):**
![[Pasted image 20221212224019.png]]

**For 50k iterations, the iterative (blue) achieves much better results for the same amount of parameters as the one-shot method (green):**
![[Pasted image 20221212231541.png|250]]

## Tags
#external 
#assertion

## Source
[[Frankle et al. (2018)
