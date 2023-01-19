---
aliases: []
---
# Content
It's a network that predicts [[Point Cloud]] from 2D images.
The network words by multi-stages, where a sparse point cloud is predicted from a 2D image, which is then refined to become a denser point cloud, as explained in the following scheme:
![[Pasted image 20230118123511.png|300]]

The pipeline is composed by an encoder-decoder network that creates the first point cloud, followed by the recursive use of a [[Dense Reconstruction Network]], that keeps upsampling the point cloud, making it denser. An overview can be seen in the following scheme:
![[Pasted image 20230118124334.png|600]]



# Tags
#external 

# Source
[[Mandikal et al. (2019)]]
