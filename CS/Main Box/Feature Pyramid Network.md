---
aliases: [Feature Pyramid Networks, FPN, FPNs]
---
## Content
FPNs are type of [[Feature Network|feature network]], which serve the purpose of [[recognizing objects at different scales]]. It is then possible to use each feature independently to try to find and recognize objects of different scales, as shown in following scheme: 
![[Pasted image 20221211173449.png|350]]

FPNs are based on the natural hierarchical nature of [[Convolutional Neural Network|convolutional neural networks]].  There are two sequential parts of the behavior of an FPN: the *bottom-up* and *top-down* paths. FPNs can, in general, have any convolutional network as the backbone.

1. **Bottom-Up**: CNNs usually decreased the size of the feature map and it proceeds forward. This path simply runs the input through the network and collects different feature maps. Each level of the pyramid is made up by feature maps of different dimensions. The higher the level, the smaller the feature map. In the paper, the feature maps collected were the ones of the layers before resizing.
2. **Top-Down**: After the previous path, we should have feature maps for each pyramid level. The idea is to use each one of these to make predictions,but there is a problem. The first feature map has less information than the second one, and so on. To address this, for each feature map, starting at the top, we merge it with the one above in the pyramid in order to gain its knowledge. The top one merges with the top second, then the top second merges with the top third... so on, until the bottom feature map gets merged and every feature map will have the information from above its level. After the merged maps, we apply to them a $3\times3$ convolution to generate the final map, which is used to reduce the aliasing effect of upsampling. The number of channels is fixed for every feature map because the point is to share convolutional layers for each feature map afterwards (for whatever purpose we use these pyramid feature maps).
	* **How is [[Feature Map Fusion]] done?** [[FPN feature fusion]]   

## Tags
#external 

## Source
[[Lin et al. (2017)]]
