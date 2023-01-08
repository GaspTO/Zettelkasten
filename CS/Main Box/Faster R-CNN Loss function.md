---
aliases: [faster r-cnn loss]
---
## Content
During training of [[Faster R-CNN]], the [[anchors|Anchors]] are assigned positive labels if either:
1. have the highest IoU overlap with a ground-truth box
2. have IoU overlap with some ground-truth box is higher than 0.7
A single ground-truth box might assign positive labels to multiple anchors.

Anchors are assigned negative labels if their IoU overlap is lower than 0.3 for all ground-truth boxes. 

The anchors that aren't assigned a positive or negative label are not used for training.

The **loss function** to be minimized is
$$\begin{equation}
\mathcal{L}(\{p_i\},\{t_i\}) = \frac{1}{N_{cls}} \sum_i \mathcal{L}_{cls}(p_i,p_i^*) + \lambda \frac{1}{N_{reg}} \sum_i p_i^* \mathcal{L}_{reg}(t_i,t_i^*)
\end{equation}$$
**where**,
* $i$ is the index of an anchor in a mini-batch and $p_i$ is the probability of that anchor having an object. The ground-truth label $p_i^*$ is 1 if the anchor is positive, and is 0 if it is negative.
* $t_i$ is a 4-dimensional vector, representing the parameterized coordinates of the predicted bounding box, and $t_i^*$ is that of the ground-truth box associated with a positive anchor.
* $\mathcal{L}_{cls}$ is log loss over two classes (objects vs not object).
* $\mathcal{L}_{reg}(t_i,t_i^*) = R(t_i - t_i^*)$, where $R$ is the robust loss function ([[Smooth L1 Loss]]). 
* $p_i^* \mathcal{L}_{reg}$ means the loss is only activated for anchor boxes that are labeled positive.
* Two terms are normalized by $N_{cls}$ and $N_{reg}$ and weighted by a balancing parameter $\lambda$. In their implementation, $N_{cls}$ is equal to the mini-batch size (256), $N_{reg}$ is the number of anchor locations (~2400) and $\lambda = 10$.
* For bounding box regression, $t$ parameterizations of the 4 coordinates following:
$$\begin{equation}
t_x = (x-x_a)/w_a \ , \ \ t_x^* = (x^* - x_a)/w_a
\end{equation}$$
$$\begin{equation}
t_y = (y-y_a)/h_a \ , \ \ t_y^* = (y^* - y_a)/h_a
\end{equation}$$
$$\begin{equation}
t_w = \log(w/w_a) \ , \ \ t_w^* = \log(w^*/w_a)
\end{equation}$$
$$\begin{equation}
t_h = \log(h/h_a) \ , \ \ t_h^* = \log(h^*/h_a)
\end{equation}$$
**where,** $x$, $y$, $w$ and $h$ denote the box's center coordinates and its width and height. Variables $x$, $x_a$, and $x^*$ are for the predicted box, anchor box, and ground-truth box respectively (likewise for $y$, $w$, $h$).


**In words,** the predicted boxes that are going to be updated to be more like some ground-truth boxes. The target ground-truth boxes are chosen based on their overlap with the predicted boxes' anchors.  For the classification part, it is trained to classify the existence of an object if the corresponding anchor has a big overlap with some ground-truth box, and trained to not classify if there is no big overlap. Boxes that have some overlap, but not enough to classify positively, are ignored.

## Tags
#external 

## Source
[[Ren et al. (2016)]].