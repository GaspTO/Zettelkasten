---
aliases: []
---
## Content
The [[yolov2]] architecture is modified after [[YOLOv2 training for classification]]. The last [[Convolutional Layer|convolutional layer]] is swapped by three $3 \times 3$ [[Convolutional Layer|convolutional layers]] with $1024$ filters, each followed by a final $1 \times 1$ [[Convolutional Layer|convolutional layer]] with the same number of outputs as needed for detection. For *VOC*, 5 boxes with 5 coordinates each and 20 classes per box, so 125 filters.

The network is trained for 160 [[epoch|epochs]], with a [[starting learning rate]] of $10^{-3}$, dividing it by 10 at 60 and 90 [[epochs]]. A [[weight decay]] of 0.0005 and a [[momentum]] of 0.9 is used. 

Similar [[data augmentation]] is used here as in [[YOLOv1 Training]]. The same training strategy is used in both VOC and COCO.

## Tags
#external 

## Source
[[Redmon et al. (2016-b)]]