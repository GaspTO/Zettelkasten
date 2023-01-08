---
aliases: [BiFPNs, bi-directional feature pyramid network, bi-directional feature pyramid networks, bi-directional FPN, bi-directional FPNs]
---
## Content
The BiFPN is a [[Feature Network]] that has a two-path fusion, one top-down and another bottom-up. A scheme about the way it works is show in the following figure:
![[Pasted image 20221217235827.png|300]]
**Briefly**, for a feature map a new one is created by merging with the top one. Then, this one is merged with the previous one and the original feature map.  This block can be repeated multiple times.


**In Detail**, 
* for some layer which isn't the first or last:
	1. The first part will be to do a [[Normalized Feature Fusion|normalized feature fusion]] with the resize feature map coming from the next layer:
	   $$\begin{equation}
	   P_6^{td} = \text{Conv}(\frac{w_1 \cdot P_6^{in} + w_2 \cdot \text{Resize}(P_7^{in})}{w_1 + w_2 + \epsilon})
	\end{equation}$$
	2. After this, the resulting feature map will do another [[Normalized Feature Fusion|normalized feature fusion]], but, this time, it will use the previous feature, the resized one from the previous layer and the original from the same layer:
$$\begin{equation}
P_6^{out} = \text{Conv}(\frac{w_1^{'} \cdot P_6^{in} + w_2^{'} \cdot P_6^{td} + w_3^{'} \cdot \text{Resize}(P_5^{out})}{w_1^{'}+w_2^{'}+w_3^{'}+\epsilon})
\end{equation}$$
* For the top layer only the equation 2. is used but without the $P^{td}$ feature map part.
* For the bottom layer, only the equation 1 is used.

## Tags
#external 

## Source
[[Tan et al. (2020)]]