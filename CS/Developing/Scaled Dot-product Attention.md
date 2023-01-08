---
aliases: [transformer attention]
---
## Content
It is given by
$$\begin{equation}
\text{Attention}(Q,K,V) = \text{softmax}(\frac{QK^T}{\sqrt{d_k}}) \cdot V
\end{equation}$$
* $Q \in \mathbb{R}^{N \times d_k}$ is the matrix of queries
* $K \in \mathbb{R}^{N \times d_k}$ is the matrix of keys
* $V \in \mathbb{V}^{N \times d_v}$ is the matrix of values
* $N$ is the number of input tokens (for e.g. number of words), which does not have a fixed size
* $d_k$ is the dimension of each key
* $d_v$ is the dimension of each value
* $d_\text{model}$ is the chosen size for each embedding.


For large $d_k$ values, the dot product tends to grow large in magnitude, pushing the softmax function into regions where it has small gradients. (The dot product should still be centered around 0, but the variance grows a lot).

**It is shown in the following scheme:**
![[Pasted image 20230105221301.png|150]]


## Tags
#external 

## Source
[[Vaswani et. al (2017)]]
