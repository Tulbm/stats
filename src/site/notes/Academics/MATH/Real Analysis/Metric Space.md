---
dg-publish: true
---
To denote a metric space, we typically use the notation $(X,d)$, the set and the [[Distance Function]] on the set


A metric space is complete if every [[Cauchy Sequence]] of elements in $X$ converges to an element of $X$.
- $\mathbb{Q}$ is not complete as there are sequences in it that converge to elements only in $\mathbb{R}$, i.e. $\pi$

# Examples
Examples $X=\mathbb{R}:$ [[Distance Function#Examples]] 

## Distance between functions
Let $S$ be the set of all functions that are continuous of $[a,b]$ and define
$$
d_{p}(f,g) = \left( \int _{a}^{b} |f-g|^{p}  \, dx   \right)^{1/p}
$$

Then $(S,d_{p})$ is a metric space. It is a well-known family of functions spaces called the $L^{p}$ spaces.

For example with $d_{2}:$
$$
d_{2}(f,g)= \left( \int _{a}^{b} (f-g)^{2} \, dx  \right)^{1/2}
$$
Considering the space of all continuous functions on $[0,1]$.
$$
\begin{align}
d_{2}(x,x^{2}) & = \sqrt{  \int _{0}^{1}(x-x^{2})^{2} \, dx  } \\
 & = \sqrt{  \int _{0}^{1} (x^{2}-2x^{3}+x^{4}) \, dx  } \\
 & = \left( \left. \frac{x^{3}}{3} - \frac{x^{4}}{2} + \frac{x^{5}}{5} \right|_{0}^{1} \right)^{1/2} \\
 & = \left( \frac{1}{3} - \frac{1}{2}+ \frac{1}{5}- 0 \right) ^{1/2} \\
 & = \left(  \frac{10-15+6}{30} \right)^{ 1/2} = \frac{1}{\sqrt{ 30 }}
\end{align}
$$

[[Hausdorff metric]]



## sup norm
Another way to measure distances between functions on some domain $X$

$$
d_{\infty} (f,g)= \underset{x\in  X}{sup} |f(x)=g(x)|
$$


