---
aliases: [efficientdet compound scaling rule]
---
## Content
This [[compound scaling rule]] allows a network for a [[Object detection|object detection]], that uses [[BiFPN]], to be expanded with only one parameter, $\phi$:

* **Backbone dimensions**:
	The same width and depth defined by the [[efficientnet compound rule]], where $\phi = 0$ is B0 and $\phi = 6$ is B6, mainly so that it is possible to use pre-trained checkpoints.

* **[[BiFPN]]**:
	- width (# of channels): $W_{bifpn} = 64 \cdot (1.35^\phi)$
	* depth (# layers): $D_{bifpn} = 3 + \phi$
	
	Notice how depth increases much slower (linearly) than depth (exponentially)

* **Box/Class network**:
	* width (# of channels): $W_{pred} = W_{bifpn}$
	* depth (# layers): $D_{box} = D_{pred} = 3 + [\phi / 3 ]$

* **Image resolution** (It has to be divisible $2^7$=128):
	* $R_{input} = 512 + \phi \cdot 128$


Here's a scheme summarizing the possible networks:
![[Pasted image 20221217231652.png|500]]


Here's the overview of results based on the compound rule. See the paper for details.
![[Pasted image 20221217233400.png|400]]

## Tags
#external 

## Source
[[Tan et al. (2020)]]
