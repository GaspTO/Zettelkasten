---
aliases: []
---
## Content
Based on the reasoning I developed in [[Sequenced Forward-Forward algorithm]], I am wondering whether you can distill a network into another but, instead of distiling the last layer feature maps, do that for multiple layers. Based on the [[Sequenced Forward-Forward algorithm]], I wonder what happens if we introduce some $\delta$ tolerance.

Noisy student does have a distillation cycle which is very effective at improving the model, I wonder whether replacing it by a layer-layer distillation with some tolerance (otherwise it would just copy the teacher network) would work.

It would be interesting to see if we could speed up the distillation process.








## Tags
#internal #idea #todo

## Source
