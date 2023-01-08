---
aliases: []
---
## Content







**Given:** A bunch of points in the (x,y)
![[Pasted image 20230106230606.png|200]]

**Goal:** Detect line $y = mx + c$
![[Pasted image 20230106230814.png|200]]

Consider point $(x_i,y_i)$, we have:
$$\begin{equation}
y_i = mx_i + c \Leftrightarrow c = -mx_i + y_i
\end{equation}$$
We can see the latter equation as describing the variables $m$ and $c$. In other words, it describes all the lines (all the parameters) that pass through the point $x_i$ and $y_i$. The interesting thing is that this equation is also a line:
![[Pasted image 20230106231237.png|300]]

If we find all these parameter equations for all the points, we get:
![[Pasted image 20230106231353.png|300]]

Where we can see that there is parameter combination $(m,c)$ that is the same to every point. While if there is a point outside of the original line, we get:
![[Pasted image 20230106231519.png|300]]


## Tags

## Source
