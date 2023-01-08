«---
aliases: []
---
## Content
A question that I had when I first read [[Faster R-CNN]] was how the [[Anchor box]] boxes relate to the predicted boxes? Can't the predicted box be something completely different from the anchor?

The answer has to do with the [[Faster R-CNN Loss function|faster r-cnn loss function]].  Basically, the only predicted boxes that matter are the ones who correspond to those anchor boxes that intercept ground-truth boxes. For those anchor boxes, the predicted ones are fitted to match the correspondent ground-truth ones. The ground-truth ones might not correspond exactly to the anchor, but they have to be similar enough. In other words, the predicted box, by imitating the ground-truth box, will end up approximating itself from its anchor - although it doesn't have to be exactly equal to the anchor.

## Tags
#internal

## Source
