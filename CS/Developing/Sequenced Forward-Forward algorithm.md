---
aliases: []
---
## Content
In the [[Forward-Forward Algorithm]], internal layers are updated towards a local objective, independently of one another.  It is based on the data distribution and their manipulation and not their annotations, trying to distinguish positive and negative samples. However, this doesn't take advantage of any structure between samples, even though, in many cases there is one, for example, in videos, where samples have connections to one another, forming sequences. A human being's processing of the world can be seen as an infinite sequence of images, and it makes sense that the features changes smoothly as the sequence progresses. This would explain how we understand the concept of textures changing in different lightning conditions; we see a cat in the sun with a certain texture and, after a certain number of images in the sequence we observe, as he goes into the shadow, the texture changes. If we approximate the features of these sequences, we are, as a consequence, approximating the features of the cat's texture in the sun with the one of his in the shadow, as it makes sense.

The idea is approximate features like this, using image sequences, but, instead of approximating the last layer, we approximate each layer in the network. T


A detail that should be noted is that we should do a soft-approximation,
$$\begin{equation}
\mathcal{L}(x_n,x_{n+1}) = ||f(x_n) - f(x_{n+1})||^2 < \delta
\end{equation}$$
so that each feature map can have some $\delta$ tolerance to learn the meaning variation between frames.  It should also be noted that, in practice, the earlier the layer, the bigger the tolerance will have to be.

**What is the advantage of maximizing each layer's similarity?**
The same way as the forward-forward algorithm does- we don't have to do backpropagation through the network, but just in each layer, independently, which makes the whole optimization much more efficient. Once we have all the forward passes of the relevant sequences we are going to approximate each layer individually to one another. The gradients do not pass to the previous layer.


## Tags
#internal #idea #todo

## Source
