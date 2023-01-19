## Content
Fast r-cnn is an [[Object detection]] method, which is an improvement over [[R-CNN]].
This method no longer separates the convolutional part from the bounding box regressor and the classification. 

As an input, fast r-cnn receives both an image and several [[region of interest| RoIs]], that were previously selected by, for example, selective search.

First, a [[Convolutional Neural Network]] is used to process an image into a feature map (The feature map will have width and height, resembling a processed image). 

Second, for each RoI, a [[Region of Interest pooling layer]] will extract a feature vector of fixed length. 

Third, this feature vector is pre-processed by two fully connected layers before branching to two different output paths.

The first, applies a softmax to the previous vector, returning the correct class (including background). The second is a set of 4 real valued numbers for each class. Each set of 4 values encodes refined bounding-box positions for one of the K classes.


![[Pasted image 20221123014301.png|450]]

## Tags
#external 

## Source
[[Girshick (2015)]]


