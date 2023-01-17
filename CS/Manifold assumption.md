---
aliases: []
---
# Content
In machine learning prolems where the data can be represented in [[Euclidean space]], the observed data points in the high-dimensional input space $\mathbb{R}$ are usually concentrated along lower-dimensional substructures. These substructures are known as [[Manifold]].

The manifold assumption is [[Assumptions of semi-supervised learning|semi-supervised assumption]]  that relies on two sub-assumptions:
1. The input space is composed of multiple lower-dimensional manifolds on which all data points lie.
2. Data points lying on the same manifold share the same label.

Consequently, if we are able to determine which manifolds exist and which data points lie on which manifold, the class assignments of unlabelled data points can be inferred from the labelled data points on the same manifold.

**A reasoning about this:** This does not mean that every data point with a particular label is one same manifold, but those that are on the same manifold share the same label. It's interesting to think that the problem of classification could be broken into two: first, map every point to its manifold; two, map each manifold to a label. 

![[Pasted image 20230116172551.png|300]]

# Tags
#external 

# Source
[[Engeleen et al. (2020)]]