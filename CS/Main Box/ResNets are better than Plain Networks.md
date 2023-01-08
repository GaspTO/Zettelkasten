## Content
[[He et al. (2016)]] studied the convergence of 18 and 34 layered plain and [[ResNet|resnets]] in the [[ImageNet]]. 

When looking at the convergence of plain networks, the 34-layered one was worse than the 18 one:
![[Pasted image 20221121214402.png|400]]

Obviously, this is counter-intuitive since the resnet-18 learns within the subspace of functions that the other network can learn.

When evaluating the residual networks, the opposite happens, the 34 is now better.
![[Pasted image 20221121214539.png|400]]

More importantly, the [[degradation problem]] seems to have been solved here.

Interestingly enough, the final result of both plain and residual 18 is the same. The authors claim that the resnet-18 converges faster, but I can't tell from the pictures.






## Tags
#external 
#assertion 

## Source
[[He et al. (2016)]]

