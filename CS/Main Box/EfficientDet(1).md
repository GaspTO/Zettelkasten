---
aliases: [EfficientDets]
---
## Content
EfficientDets is a one-stage [[Object detection]] architecture that was designed to be easily and efficiently scalable. An efficientDet is composed by a pre-trained [[EfficientNet]] backbone, a [[BiFPN]] applied to feature maps 3-7, and a class/box prediction network.  See the following scheme of the architecture:

![[Pasted image 20221217221652.png]]


For **scaling**, a [[EfficientDet Compound Rule|(EfficientDet) compound rule]] is proposed, based on the coefficient $\phi$, scaling the dimensions of the backbone, [[BiFPN]], class/box network, and resolution.

## Tags
#external 
#todo

## Source
[[Tan et al. (2020)]]
