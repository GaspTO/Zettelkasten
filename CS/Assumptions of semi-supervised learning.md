---
aliases: [semi-supervised assumption]
---
# Content
A necessary assumption of [[Semi-supervision|Semi-supervised learning]] is that the underlying marginal data distribution $p(x)$ contains information about the posterior distribution $p(y|x)$

In order words, the probability of the distribution $p(y|x)$ and that of $p(x)$ are not independent. So, if we understand the structure of the data, we might understand better the structure of the labels over the data. 

On the other hand if knowing $p(x)$ does not tell us anything about $p(y|x)$, then it is inherently impossible to improve the accuracy of our model using unlabeled data.

Fortunately, in practice, this relationship does seem to exist in most (if not all) learning problems, which explains the success of semi-supervised approaches. However, the way in which $p(x)$ and $p(y|x)$ interact is not always the same and this has given rise to specific assumptions about this relationship.

# Tags
#external 

# Source
[[Engeleen et al. (2020)]]