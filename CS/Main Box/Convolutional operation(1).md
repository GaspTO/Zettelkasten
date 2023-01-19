---
aliases: [convolution, convolutions, convolutional operations, convolutional op, convolutional ops, conv op, conv ops]
---
## Content
It is defined as
$$\begin{equation}
(x * w)(t) = \int_{-\infty}^{+\infty} x(\tau)w(t-\tau) d\tau
\end{equation}$$
* The $w$ function is usually called kernel
* $f$ is called **input**
* the output is sometimes called **feature map**

A lot of times, we are dealing with discreet problems and functions, in which case the convolution operation is given by

$$\begin{equation}
(x * w)(t) = \sum_{a=-\infty}^{+\infty} x(\tau)w(t-\tau)
\end{equation}$$
We can also define it for the two dimensional case as
$$\begin{equation}
(K * I)(i,j) = \sum_m \sum_n I(m,n)K(i-m,j-n)
\end{equation}$$
convolutional operations enjoy the **commutative property**, which might be useful to write proofs. With that we can write: 
$$\begin{equation}
(K * I)(i,j) = \sum_m \sum_n I(i-m,j-n)K(m,n)
\end{equation}$$
**In practice,** a lot of *convolutional operations* are, in practice, implemented as [[Cross-correlation operation|cross-correlation operations]].

## Tags
#external 

## Source
[[Goodfellow et al. (2016)]]



