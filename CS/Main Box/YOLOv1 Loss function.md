---
aliases: [yolo loss function, yolo loss, yolov1 loss]
---
## Content
[[YOLOv1]] predicts multiples bounding boxes per grid cell, but we only want one to be responsible for each object. The predicted bounding box that is assigned to an object is the one with the highest current IOU with the ground truth of such object. 

This leads to specialization between the bounding box predictors. Each predictor gets better at predicting certain sizes, aspect ratios, or classes of object, improving overall recall.

The **loss function** to be minimized is:

$$\begin{equation}
\begin{split}

&\lambda_{\text{coord}} \sum_{i=0}^{S^2} \sum_{j=0}^{B} \mathbb{1}_{ij}^{\text{obj}}[(x_i - \hat{x}_i)^2 +(y_i - \hat{y}_i)^2] \\

+ &\lambda_{\text{coord}}\sum_{i=0}^{S^2} 
\sum_{j=0}^{B}\mathbb{1}_{ij}^{\text{obj}}[(\sqrt{w_i}-\sqrt{\hat{w}_i})] \\

+ &\sum_{i=0}^{S^2} \sum_{j=0}^{B} \mathbb{1}_{ij}^{\text{obj}}(C_i - \hat{C}_i)^2 \\

+ &\lambda_{\text{noobj}} \sum_{i=0}^{S^2} \sum_{j=0}^{B} \mathbb{1}_{ij}^{\text{obj}}(C_i - \hat{C}_i)^2 \\

+ &\sum_{i=0}^{S^2} \mathbb{1}_i^{\text{obj}} \sum_{c\in\text{classes}}(p_i(c) - \hat{p}_i(c))


\end{split}
\end{equation}$$
 **where,** $\mathbb{1}_i^{\text{obj}}$ denotes if object appears in cell $i$ and $\mathbb{1}_{ij}^\text{obj}$ denote that the $j^{\text{th}}$ bounding box predictor in cell $i$ is responsible for that prediction. 
 
 There is a $\lambda_{\text{noobj}}$ to balance the much higher number of bounding boxes that do not have objects than those which do. A $\lambda_{\text{coord}}$ to balance between the localization and classification error.

* Note that the loss function penalizes classification error **only if** an object is present in that grid cell (hence the conditional class probability discussed earlier). 
* It also penalizes bounding box coordinate error **only if** that predictor is “responsible” for the ground truth box (i.e. has the highest IoU  of any predictor in that grid cell).

See the following image explaining the terms of the loss(\*):
![[Pasted image 20221204222612.png|600]]
 

 

## Tags
#external 

## Source
[[Redmon et al. (2016-a)]]

(\*)Image taken from: https://towardsdatascience.com/yolov1-you-only-look-once-object-detection-e1f3ffec8a89

