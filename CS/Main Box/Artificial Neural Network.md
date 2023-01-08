---
aliases: [artificial neural networks, ann, anns, neural network, neural networks, nn, nns, network, networks]
---
## Content
A neural network is used to approximate some function $f^*$. For example, for a classifier function $f^*(\mathbf{x}) = \mathbf{y}$, a neural network can define an approximated mapping $f(\mathbf{x}; \mathbf{\theta})$ by adjusting its parameters $\theta$.

A neural network can be seen as the composition of multiple sub-functions, $f^{(k)}$,
$$\begin{equation}
f(\mathbf{x}) =\ ...f^{(3)} (f^{(2)}(f^{(1)}(\mathbf{x})))
\end{equation}$$
These sub-functions are called *layers*.   Different layers may perform different transformations on their inputs.  Signals travel from the first layer, called *input layer* - which is just $\mathbf{x}$, to the last layer (*output layer*), possibly after traversing the same layer multiple times.  The layers in the between are called *hidden layers*. Each hidden layer is composed by several [[Hidden unit|hidden units]]  The overall length of this chain is the *depth* of the neural network.  Stacking multiple layers in neural networks gave birth to the name ***deep learning***. 

These networks are called neural because they are loosely inspired by
neuroscience. These functions are vector-valued, and their dimensionality determines the *width* of the model. Each element of the vector may be interpreted as playing a role analogous to a neuron. Rather than thinking of the layer as representing a single vector-to-vector function, we can also think of the layer as consisting of many [[Hidden unit|hidden units]] that act in parallel, each representing a vector-to-scalar function. 

Each [hidden unit] resembles a neuron in the sense that it receives input from many other units and computes its own *firing* value. The idea of using many layers of vector-valued representation is drawn from neuroscience.

## Tags
#external 

## Source
[[Goodfellow et al. (2016)]]


