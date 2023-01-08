---
aliases: []
---
## Content
The [[Pre-train a network as a classifier before training it as a object detector]] on [[ImageNet]], achieving 88% top-5 accuracy. The Darknet framework is used for training and inference at this point.

Then, the model is converted to detectors. The network is slightly changed from the pre-trained one. **Four** [[Convolutional Layer|convolutional layers]] and **two** [[Fully Connected layer|fully connected layers]] are added with random weights.

Detection requires fine-grained visual information, so the input resolution is increased from $224 \times 224$ to $448 \times 448$.

[[YOLOv1]] then optimizes a [[YOLOv1 Loss function|multi-part loss function]].

## Tags
#external 

## Source
[[Redmon et al. (2016-a)]]
