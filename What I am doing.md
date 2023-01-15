## Active Learning
* A Survey of Deep Active Learning
* **(CEAL)**: [Cost-Effective Active Learning for Deep Image Classification](https://arxiv.org/abs/1701.03551)
* **(LLAL):**[Learning Loss for Active Learning](https://arxiv.org/abs/1905.03677)
* 


## Domain adaptation + Active Learning
* Half a Percent of Labels is Enough: Efficient Animal Detection in UAV Imagery using Deep CNNs and Active Learning


## Active Learning (with 3D LiDAR points):
* Deep Active Learning for Efficient Training of a LiDAR 3D Object Detector


## TO READ
* Hiranmayi Ranganathan, Hemanth Venkateswara, Shayok Chakraborty, and Sethuraman Panchanathan. 2017. Deep active learning for image classification. (2017), 3934–3938.
* William H. Beluch, Tim Genewein, Andreas Nürnberger, and Jan M. Köhler. 2018. The Power of Ensembles for Active Learning in Image Classification. In 2018 IEEE Conference on Computer Vision and Pattern Recognition, CVPR 2018, Salt Lake City, UT, USA, June 18-22, 2018. IEEE Computer Society, 9368–9377.



##  POINTS FROM SURVEY
* First models would first train the deep models and then *fine-tune* using AL
* CEAL was the first to integrate both deep learning and AL
* CEAL overview:
  ![[Pasted image 20230115223517.png]]
* You can look at the uncertainty about cnns to be composed by two stages. Feature extraction and task learning stage:
![[Pasted image 20230115230651.png|500]]

* LLAL is an uncertainty method and it bases itself in the idea that there is a difference between task loss and feature loss. Overview:
  ![[Pasted image 20230115225250.png|500]]
  * The loss prediction module is learned to predict the target loss of the unlabeled dataset, while the top-𝐾 strategy is used to select the query samples
  