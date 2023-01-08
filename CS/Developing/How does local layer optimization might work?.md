---
aliases: []
---
## Content
I just wrote about the [[Forward-Forward Algorithm]] which learns representations locally. 

I am trying to grasp the intuition behind it. How can the output of layer $n-1$ be changed to help the output layer of layer $n$ if there is no backpropagation from the $n^{th}$ to the $(n-1)^{th}$?

It seems that, according to the paper, that the posterior layers are always forced to rely on whatever information was left over from the previous one. 

So, by induction:
1) Can the first layer learn the necessary features for classification?
2) Can layer $n$ learn the necessary features for classification if the layer $n-1$ has done so?


**The answer to both:**
First, answering the second.
2) If we prove point 1) we also prove point 2) since we can think of the input image as features that contain all the image information. If we can learn from the image directly, there is no reason why we can't learn from another vector/features which do have all the relevant information as well. So, all that remains to show is whether or not we can learn relevant features in the point 1)

1) What's stopping the layer to learn the same normalized vector for every data sample, only distinguishing the sample category based on the length of the vector? In this case, all the features, once normalized and passed to the next layer, would be the same and, therefore, useless. 
    However, this isn't a unique problem to the [[Forward-Forward Algorithm]]. The question also arrives at the contrastive learning in [[self-supervised learning]]. If you take a sample, $x_a$ and augment it, creating $x_b$, and approximate $f(x_b)$ to $f(x_a)$,  where do the *good features* come from since $f(x_a)$ was randomly initialized. Why does mimicking randomly initialized features work? The only answer for this is that randomly some features are initialized correctly and those are the ones that end up being useful and persist throughout the self-supervised learning, the others being lost. This is the same explanation as the [[The Lottery Ticket Hypothesis|lottery ticket hypothesis]].  
	    **The question is:** How do both [[Forward-Forward Algorithm]], but also [[self-supervised learning]]  know and erase bad features? Well, what is a bad feature? It's one that is invariant to a irrelevant context. In fact, the best way to think of all features, including those randomly initialized, is to think of the contexts in which they appear. Those contexts are the ones they are invariant to. If one neuron is always the same independently of the image, then the context includes all the image space. If a neuron is invariant when there is a lot of green pixels, then the context is all the images with a lot of green pixels. The answer, therefore, to what makes a bad feature is features that are invariant when they shouldn't be. Their in-variance isn't helping. Well, this is not so simple, in reality even if a feature is variant according to different contexts, there is a difference between the feature being randomly attributed to different instances of the context, and the relationship between different features reflects the difference between contexts, in such way that a non-linear function might be able to identify each one. The context we want to identify is the label space, each instance of that context is a label. So, going back, how does **contrastive learning** eradicate bad features? Well, sometimes $f(x_a)$ is the target, other times $f(x_b)$ is the target, other times $f(x_c)$... so, it is only possible to learn to differentiate the context of the features that were randomly initialized by one of these. If we are approximating $f(x_a)$ towards $f(x_b)$, it makes sense that if these two share two contexts captured in common, $f(x_a)$ will keep that, while the other contexts have a proclivity to disappear. And vice-versa for $f(x_b)$ and $f(x_c)$. However this reasoning implies that $f(x)$ will tend to keep the features that capture the same contexts and will throw everything else out. Uhmm... interesting, I guess in a way this makes sense. If $x_a$ is a cat and $x_b$ is the rotated version of that cat, contrastive learning will destroy the context of orientation which is something not in common. So... hold on, contrastive self-supervised learning is the set of contexts (only those that are shared in common). **How to test this:** Pick a random network, let the first layer with the random unchanged initialized weights and pre-train. If all the features are captured there by random, then you should be able to train a network without training the first layer. But, now that I think of it, this is very unlikely to be possible, so my theory is wrong.... 
       So, maybe, that what happens in the forward-forward algorithm - random features are initialized and those simply aren't destroyed

## Tags
#internal 

## Source
