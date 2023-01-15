## Content
The r-cnn was one of the first [[Object detection]] techniques to use [[Convolutional Neural Network|CNNs]]. The method is divided into three parts. 
1. A [[region proposal method]] is used to determine a subsection of the image to analyse. At test time, 2000 region proposals are used. The specific region proposal method used is irrelevant, but [[Girshick et al, (2014)]] uses [[selective search]].
2. A 4096-dimensional feature vector is extracted from that region using a pre-trained [[alexnet]] as the backbone.
3. A bunch of [[support vector machine|SVMs]], one per class in the dataset, is used on the extracted features to score them. After this step, we get a list of regions for each class.

![[Pasted image 20221122225133.png|450]]

Most of the 2000 regions will be classified as background, but a lot of the remaining regions will be near each other and will recognize the same object, counting it more than one time. After scoring them with the [[support vector machine|SVMs]], a [[greedy non-maximum suppression]] per class ran, which rejects a region if it has an [[intersection-over-union|IoU]] overlap with a high enough threshold that is learned.0

r-cnn also uses a [[bounding-box regression]].

## Tags
#external 
#potential-links - features?

## Source
[[Girshick et al, (2014)]]

