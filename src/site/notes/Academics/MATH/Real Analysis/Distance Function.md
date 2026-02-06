---
dg-publish: true
---
Given a set $X$, a metric/distance function $f$ on $X$ is a function $X\times X\to \mathbb{R}$ that satisfies all of the following properties.
1. $d(x,y)\geq 0\ \forall x,y\in X$
   with $d(x,y)=0\iff x=y$
2. $d(x,y)=d(y,x)\ \forall x,y \in X$
3. $d(x,y)\leq d(x,z)+d(z,y)\ \forall x,y,z\in X$

# Examples
With real numbers:
## Absolute Value
Absolute values provide us with a natural way of measuring distances between any two real numbers. 

Define:
$$
d(x,y)= |x-y|\quad \forall x,y\in \mathbb{R}
$$
Then $(\mathbb{R},d)$ is a [[Metric Space]], as it satisfies the properties of a distance function:
1. $|x-y|\geq 0\ \forall x,y\in \mathbb{R}$
   we also need that $d(x,y)=0\iff x=y$
   $x=y\to d(x,y)=d(x,x)=|x-x|=0$
   $d(x,y)=0\to |x-y|=0\iff x-y=0\iff x=y$
2. $d(x,y)=|x-y|=|-1|\ |x-y|= |(-1)(x-y)|=|y-x|=d(y,x)\ \forall x,y\in \mathbb{R}$
3. $d(x,y)=|x-y|=|x-z+z-y| \leq |x-z|+|z-y|= d(x,z)+d(z,y)$
   $\Longrightarrow d(x,y)\leq d(x,z)+d(z,y)$
## Trivial/Discrete Metric
$$
d(x,y)= \begin{cases}
0,  & \text{ if } x=y \\
1, & \text{ otherwise} 
\end{cases}
$$
## Euclidean Metric
$$
d(x,y)= \sqrt{ (x_{1}-y_{1})^{2}+(x_{2}-y_{2})^{2} }
$$
The Euclidean metric scales up for $\mathbb{R}^{n}$ in a natural way. For $x,y\in \mathbb{R}^{n}$, define:
$$
d(\mathbf{x},\mathbf{y})= \sqrt{  \sum_{i=1}^{n}(x_{i}-y_{i})^{2} }
$$
1. $d(\mathbf{x},\mathbf{y})\geq 0\ \forall \mathbf{x},\mathbf{y}\in \mathbb{R}^{n}$
   $d(\mathbf{x},\mathbf{y})=\sqrt{  \sum (x_{i}-y_{i})^{2} }$ is non-negative by the definition of $f(x)=\sqrt{ x }$
   $d(\mathbf{x},\mathbf{y})=0 \iff \mathbf{x}=\mathbf{y}$
   $\mathbf{x}=\mathbf{y}\to x_{i}=y_{i}\ \forall i\Longrightarrow d(\mathbf{x},\mathbf{y})= \sqrt{  \sum (x_{i}-x_{i})^{2} }=\sqrt{ \sum (0) }=0$
   $$
\begin{align}
d(x,y)=0 \Longrightarrow \sqrt{ \sum (x_{i}-y_{i})^{2} } & =0  \\
 \sum (x_{i}-y_{i})^{2} & =0 \\
(x_{i}-y_{i})^{2}  & =0 \\
x_{i}-y_{i} & =0 \\
x_{i} & =y_{i} \Rightarrow \mathbf{x} = \mathbf{y}
\end{align}
$$
2. $d(\mathbf{x},\mathbf{y})=d(\mathbf{y},\mathbf{x})\ \forall \mathbf{x},\mathbf{y}\in \mathbb{R}^{n}$
   $$
\begin{align}
d(x,y)  & = \sqrt{  \sum_{i=1}^{n} (x_{i}-y_{i})^{2}  } \\
 & = \sqrt{  \sum ((-1) (y_{i}-x_{i}))^{2} }  \\
 & = \sqrt{ \sum (y_{i}-x_{i} )^{2} } = d(\mathbf{y},\mathbf{x})
\end{align}
$$
3. $d(\mathbf{x},\mathbf{y})\leq d(\mathbf{x},\mathbf{z})+d(\mathbf{z},\mathbf{y})$
   Instead we will prove:
   $$
\begin{align}
(d(\mathbf{x},\mathbf{y}))^{2}  & \leq (d(\mathbf{x},\mathbf{z}))^{2} + 2d(\mathbf{x},\mathbf{z})d(\mathbf{z},\mathbf{y}) + (d(\mathbf{z},\mathbf{y}))^{2} \\
 d(\mathbf{x},\mathbf{y})^{2}  & \leq d(\mathbf{x},\mathbf{z})^{2} +d(\mathbf{z},\mathbf{y})^{2} +2d(\mathbf{x},\mathbf{z}) d(\mathbf{z},\mathbf{y}) \quad (1)
\end{align}
$$
As we already know that $d(x,y)$ is non-negative, $x^{2}<y^{2}\to x<y$

So:
$$
\begin{align}
d(\mathbf{x},\mathbf{y})^{2} &  = \sum_{i=1}^{n} (x_{i}-y_{i})^{2}   = \sum_{i=1}^{n} (x_{i}-z_{i}+z_{i}-y_{i})^{2} \\
 d(\mathbf{x},\mathbf{y})^{2}  & = \sum_{i=1}^{n} [ (x_{i}-z_{i})^{2} +2(x_{i}-z_{i})(z_{i}-y_{i})+ (z_{i}-y_{i})^{2}] \\
 & = \sum (x_{i}-z_{i}) ^{2} + \sum (z_{i}-y_{i})^{2} + 2 \sum (x_{i}-z_{i})(z_{i}-y_{i})\\
d(\mathbf{x},\mathbf{y})^{2}  & = d(\mathbf{x},\mathbf{z})^{2} + d(\mathbf{z},\mathbf{y})^{2} + 2 \sum_{i=1}^{n} (x_{i}-z_{i})(z_{i}-y_{i})
\end{align}
$$
The expression $(1)$ will hold as long as
$$
2 \sum_{i=1}^{n} (x_{i}-z_{i})(z_{i}-y_{i}) \leq 2 d(\mathbf{x,z})d(\mathbf{z,y})
$$
or equivalently:
$$
\begin{align}
\sum_{i=1}^{n} (x_{i}-z_{i}) (z_{i}-y_{i})  & \leq   \sqrt{  \sum_{i=1}^{n} (x_{i}-z_{i})^{2} } \sqrt{ \sum_{i=1}^{n}(z_{i}-y_{i})^{2} } \\
\sum_{i=1}^{n} u_{i}v_{i}  & \leq \sqrt{  \sum_{i=1}^{n} u_{i}^{2}  }\sqrt{  \sum_{i=1}^{n} v_{i}^{2} } \quad (2)
\end{align}$$
Which is true according to the [[Cauchy-Schwartz inequality]]

