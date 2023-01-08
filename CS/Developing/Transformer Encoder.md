---
aliases: [encoder of transformer]
---
## Content
The default transformer encoder has $N=6$ layer. 
Each layer is composed by: 
* [[Multi-Head Self-Attention]]
* [[Feedforward Neural Network|feedforward network]]
* A [[Residual connection]] around the [[Multi-Head Self-Attention]] and another around [[Feedforward Neural Network|feedforward network]].
* After adding features through the [[Residual connection]], the resulting embedding is passed through a layer normalization.

All these sub-layers in the model, as well as the embedding layers, produce outputs of dimension $d_{\text{model}} = 512$.

An overview of the encoder:
![[Pasted image 20221230010540.png]]

## Tags
#external 

## Source
[[Vaswani et. al (2017)]]