---
aliases: [yolov2 classification training]
---
## Content
The network is trained for classification on [[ImageNet]] 1000 classification dataset for 160 [[epochs]], using [[stochastic gradient descent]] with a starting [[learning rate]] of 0.1,  [[polynomial rate decay]] with a power of 4, [[weight decay]] of 0.0005, and [[momentum]] of 0.9, using the [[Darknet training]] framework.

Standard [[data augmentation]] is used ([[random crop]], [[rotation]], [[hue]], [[saturation]], [[exposure shift]]).

After the initial training on $224 \times 224$ images, the network is fine-tuned using $448 \times 448$ images. The same parameters as before are used, but only 10 [[epochs]] are ran, starting at a [[learning rate]] of $10^{-3}$.

This network achieves $76.5\%$ and $93.3\%$ as top-1 and top-5 accuracy, respectively.

## Tags
#external 

## Source
[[Redmon et al. (2016-b)]]
