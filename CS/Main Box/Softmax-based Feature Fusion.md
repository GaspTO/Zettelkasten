---
aliases: [softmaxed feature fusion, Softmax-based Feature Fusion]
---
## Content
It's a [[Weighted Feature Fusion|weighted feature map fusion technique]], given by:
$$\begin{equation}
\sum_i \frac{e^{w_i}}{\sum_j e^{w_j}} \cdot I_i
\end{equation}$$
where, $I_i$ is a feature map and $w_i$ is its associated weight. The feature maps need to have the same dimensionality.

## Tags
#internal 

# Source

