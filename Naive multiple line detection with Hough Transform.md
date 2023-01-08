---
aliases: []
---
# Content

## Motivation
**If we have a set of points can we find if they are related according to some shape?** For example, take a circle (the shape) and sample some points out of it. Can we recover that circle? That's the problem the **Hough Transform** addresses.

## Algorithm
**Given:** Set of points $(x,y) \in \mathbb{R}^2$ 
**Do:**
1.  Create [[Accumulator array of the vector space]] $A(m,c)$ initialized at 0 in each position
2. For each point, $(x_i,y_i)$:
	1. Find the parameter line, $c = -mx_i + y_i$, using the method described in [[Hough Transform for Lines]].
	2. Increment all the positions in the vector space array, $A(m,c) \leftarrow A(m,c) + 1$  that lie in the parameter line $c = -mx_i + y_i$.
3. Find the local maxima in the array. It has to be the local maxima because there might be different lines.

# Tags
#external

# Source
https://www.youtube.com/watch?v=XRBc_xkZREg&ab_channel=FirstPrinciplesofComputerVision