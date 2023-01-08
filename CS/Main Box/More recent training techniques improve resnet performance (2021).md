## Content
Often new architectures are compared against the results of older architectures unfairly, since that new architectures usually also use more updated training methods. For example, when the [[EfficientNet]] architecture results are compared to [[ResNet]] ones.  

However, when employing techniques used in the [[EfficientNet]] to the [[ResNet]] , the results of the latter improve tremendously from those published back in 2016 in [[He et al. (2016)]]. 

The techniques employed are [[cosine learning rate decay]], [[increased training epoch]], [[expected moving average weight update]], [[label smoothing]], [[stochastic depth]], [[randaugment]], [[dropout]] (on the fully connected / FC layer), decreased [[weight decay]], [[squeeze and excitation]], [[resnet-d]].

The additive study of them can be seen in the following table:

![[Pasted image 20221122160643.png|350]]

Where blue are training methods, green are regularization methods and yellow are architecture methods


## Tags
#external  

## Source
[[Bello et al. (2021)]]


