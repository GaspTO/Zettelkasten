---
aliases: [uncertainty-based approach, uncertainty-based query rule]
---
# Content
It's a [[Query Strategy|query strategy]] based on the degree of uncertainty that the model has regarding the classification of a sample.

It has the disadvantage that it might be too biased (for example, if you model is very bad at classifying dogs, then you might end up with a batch of samples to label that are all dogs). In other words, the samples are not representative of the unlabeled distribution.

# Tags
#external 

# Source
[[Kellenberger et al. (2019)]]