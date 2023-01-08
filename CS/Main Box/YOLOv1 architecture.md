---
aliases: []
---
## Content
[[YOLOv1]]'s architecture is inspired by GoogleNet. It has 24 [[Convolutional Layer|convolutional layers]], followed by 2 [[Fully Connected layer|fully connected layers]]. 
Instead of the [[inception module]], this one uses $1 \times 1$ reduction layers followed by $3\times3$ convolutional layers. The last feature map has a dimension of $7 \times 7 \times 30$. The $7 \times 7$ is the grid cell feature map - there are $49$ grid cells. For each grid cell there are $30$ values predicted: $20$ possible classes; $2$ bounding boxes, each one needs $5$ predicted values - 1 for confidence and 4 for coordinates ($h$, $w$, $x$, $y$).

The **width** and **height** for each bounding box is normalized by the size of the image, making them fall between $0$ and $1$.

For all layers, including the final one, a [[Leaky ReLU]] is used.

A design can be seen in this image:
![[Pasted image 20221124192327.png|550]]

## Tags
#external 

## Source
[[Redmon et al. (2016-a)]]