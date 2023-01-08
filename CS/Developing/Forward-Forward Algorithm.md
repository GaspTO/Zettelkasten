---
aliases: [FF algorithm]
---
## Content
The forward-forward algorithm is an algorithm used to optimize neural networks. It was invented as an alternative to the backpropagation algorithm.

Its main advantage is its ability to optimize layers towards a local objective, instead of a global one. In practice, this means that a layer can be optimized without completely a full forward pass and a backward one. 

This algorithm uses a contrastive objective to optimize layers, and its reasoning is very close to contrastive learning methods in self-supervised learning.  The idea is, if we look at the neuronal values as vector, we maximize one property of that vector if the data belongs to the data distribution, and minimize it if it isn't. 



#todo this goes on a different note
In the paper, one of the properties used is the sum of the square values of neurons, which is related to the length of the this vector. For the data distribution, this length is maximized, while for other inputs it is shrinked towards zero - ideally the entirely layer of neurons would not fire if the input did not belong to the data distribution. More specifically, they aim to properly classify the input as positive if it belongs to the data distribution using a sigmoid function,
$$\begin{equation}
p(\text{positive}) = \sigma(\sum_{j}y_j^2 - \theta)
\end{equation}$$
where $y_j$ is the neuronal activation of the neuron $j$ and $\theta$ is some threshold.

We have, however, to be careful to erase the property that distinguishes positive from negative examples when we pass the features to the next layer. If the current layer predicts a very lengthy vector, then the next layer will know that it is a positive example. In other words, the next layers will have a tendency to only learn about the length of the vector, which is not the goal. The objective is for each layer to recognize the features learned as a consequence of this pre-task. To do that, after each layer, there is a normalization process, making it indistinguishable, for the next layer, whether the previous thinks that those features are positive or negative.

#todo 

## Tags
#external 

## Source
[[Hinton (2022)]]





