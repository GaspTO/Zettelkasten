---
aliases: []
---
# Content
It's a type of [[Active Learning]] where the way unlabeled samples are chosen to be labeled by the oracle is by ranking them and choosing the best ones in each iteration.  In an iteration, the *most informative* (by some metric) unlabeled samples are chosen to be labeled to be added to the old date, then the model is updated (or retrained from scratch) using the new data. In the next iteration, the new model is used to choose the unlabeled samples, and so on until some stop condition is met, which might be the labeling budget or some performance criteria by the model.

![[Pasted image 20230115182327.png|400]]

# Tags
#external 

# Source
[[Kellenberger et al. (2019)]]