---
dg-publish: true
---
- [[Metric Space]] that measures distances between sets

Consider $\mathbb{R}^{n}$ for some finite $n$, and a point $x$ in an existing metric space $(\mathbb{R}^{n},d)$. 

The problems is that regardless of how $d$ is defined, it measures distances between points in $\mathbb{R}^{n}$, not *sets* of points.

$$\underset{\sim}{d}(x,S)=\underset{y\in  S}{\text{inf}} \ d(x,y) $$
We can define 
$$
h(R,S)= \underset{x\in  R}{\text{sup}}\ \underset{\sim}{d}(x,S) = \underset{x\in  R}{\text{sup}}\{  \underset{y \in  S}{ \text{inf}}\ d(x,y) \}
$$
It still the case that given two subsets $R$ and $S$, we have that $h(R,S)\neq h(S,R)$ (in general)

Last step to ensure that all properties of a metric are satisfied:
$$
d_{H}(R,S)=\text{max} \{ h(R,S),h(S,R) \}
$$
This is the definition of the Haussdorff metric

# Examples

Consider $(\mathbb{R},d)$ where $d(x,y)= |x-y|$. Suppose that $R=[-3,0]$ and $S=[-1,100)$. Then $d_{H}(R,S):$

$$
\begin{align}
h(R,S) & = \underset{ x\in  R }{  \text{sup} } \{  \underset{ y \in  S }{ \text{inf} }\ d(x,y) \} = |-3-(-1)| = 2 \\
h(S,R)  & = \underset{ x\in  S }{  \text{sup} } \{  \underset{ y \in  R }{ \text{inf} }\ d(x,y) \} = |0 - 100| = 100
\end{align}
$$
Then
$$
d_{H}(R,S)=d_{H}(S,R)= \text{max} (2,100) = 100
$$