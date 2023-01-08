---
aliases: []
---
## Content
I have been thinking about how does contrastive learning learn proper features.
Proper features means that the features are the same when all the interesting properties are equal and different otherwise. For animal images, $x$, and their rotations $z$, their features are the same if the our network is invariant to rotation. 

By property I mean human concept that distinguishes two types of images. Those which have and those which do not have that property. It might be that a random network knows most properties conceivable, which is bad since there is too much information/properties that are not needed. If the networks' random weights do not know a property (for example, if an animal with ears and an animal without them are mapped to the same features), then contrastive self-supervised won't change that. On the other hand, if we approximate $f(x)$ and $f(z)$ towards one another, we are destroying the knowledge of the network, keeping only the properties that are interesting. 

Keeping only the relevant properties helps to generalize. Let's say, for two cats, with different rotations, $x_a$ and $x_b$, there is no invariance. The network will therefore have to learn two different mappings towards the same class $f(x_a)$ and $f(x_b)$. But, if they have the same features, then the network only needs to learn one mapping. 

Destroying irrelevant properties is therefore the key to generalization. Destroying to many of them will leave us underfitting.


## Tags

## Source
