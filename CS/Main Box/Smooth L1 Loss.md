---
aliases: []
---
## Content
$$\begin{equation}
\text{smooth}_{L_1}(x,x^*) = \left\{
\begin{array}{ll}
      0.5(x-x^*)^2 & |x-x^*| < 1\\
      |x-x^*|-0.5 & \text{otherwise}
\end{array}
\right.
\end{equation}$$
It is supposed to be an alternative to the [[l2 loss|L2 loss]], by being less sensitive to outliers than it. When the targets are unbounded, the $L_2$ loss might create exploding gradients.

(I changed how the loss is presented«)

## Tags
#external 

## Source
[[Girshick (2015)]]