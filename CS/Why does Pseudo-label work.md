---
aliases: []
---
# Content
How can the technique of [[pseudo-label|pseudo-labels]] work if the information used is already *inside* the network?

It has to do with the [[Low-density assumption]]. [[Lee (2013)]] doesn't explain this very well, so I'll write here what I think.

If you think of the MLP vectors as cluster centers of each class, and the feature of the input as some point in space, it is clear that the label of such point will be that of its closest cluster. If you only have two clusters, then the decision boundary goes in the middle of those clusters. The closer to one of these the feature map is, the higher the softmax value. If the softmax value is lower, it means that the point is further from the cluster, in the middle of the two. Well, the [[Low-density assumption]] says the decision boundary should not pass through many points in the space, or, in other words, we should teach the network to put these feature points closer to each cluster.

This is a brilliant way to use an heuristic for [[self-training]].

# Tags
#external 

# Source
[[Lee (2013)]]