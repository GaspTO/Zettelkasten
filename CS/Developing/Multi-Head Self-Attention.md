---
aliases: [Multi-head Attention]
---
## Content
Multi-head self-attention is the application of multiple [[Scaled Dot-product Attention]]. 

Formally, it is given by:
$$\begin{equation}
\text{MultiHead}(Q,K,V) = \text{Concat}(\text{head}_1,...,\text{head}_h)W^Q
\end{equation}$$
where
* $\text{head}_i = \text{Attention}(QW_i^Q, KW_i^K, VW_i^V)$
* The $\text{Attention}$ formula can be seen in [[Scaled Dot-product Attention]].
* $W_i^Q \in \mathbb{R}^{d_\text{model} \times d_k}$ are the projection matrices for the queries
* $W_i^K \in \mathbb{R}^{d_\text{model} \times d_k}$ are the projection matrices for the keys
* $W_i^V \in \mathbb{R}^{d_\text{model} \times d_v}$ are the projection matrices for the values
* $d_k$ is the dimension of each key
* $d_v$ is the dimension of each value
* $W^O \in \mathbb{R}^{hd_v \times d_\text{model}}$ is the projection matrix for the concatenated values.
* $h$ is the number of heads (or parallel [[Scaled Dot-product Attention]] operations).
* $d_\text{model}$ is the chosen size for each embedding.

Visually, it is given by:
![[Pasted image 20221230010634.png|250]]
In the original work:
	$d_k = d_v = d_\text{model}/h$
	


## Tags
#external 

## Source
[[Vaswani et. al (2017)]]