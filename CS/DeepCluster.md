---
aliases: [Deep Clustering]
---
# Content
It is a [[self-supervised learning]] technique based on the pre-task of predicting feature clusters.  The motivation comes from the observation that [[Randomly initialized CNNs achieve 12% on ImageNet]]. The idea of deepcluster is to exploit this weak signal and amplify it. 

The algorithm takes several feature maps and clusters them together. The particular [[clustering algorithm]] isn't important, but the paper uses [[k-means]]. After coming up with the different cluster points, the network is trained to predict which cluster the input belongs to. This is done by using a [[Multi-layer Perceptron|mlp]] on top of the feature layer where the size of the output is the number of clusters. The particular cluster central point values is not important, we just need to map all the features, that belong to the same cluster, to the same output bin in the mlp.


# Tags
#external 

# Source
[[Caron et al. (2018)]]