---
aliases: [cross-correlation operations, cross-correlation, cross-correlations]
---
## Content
It is defined, for two dimension, as
$$\begin{equation}
(K * I)(i,j) = \sum_m \sum_n I(i,j)K(i+m,j+n)
\end{equation}$$
or, through the commutative property:
$$\begin{equation}
(K * I)(i,j) = \sum_m \sum_n I(i+m,j+n)K(m,n)
\end{equation}$$
It can be defined for more dimensions or just the 1-D case.

An example, for the dimensional case, can be seen in the following image:
![[Pasted image 20221124233518.png|500]]


## Tags
#external

## Source
[[Goodfellow et al. (2016)]]

Images from:
https://towardsdatascience.com/convolution-vs-correlation-af868b6b4fb5


