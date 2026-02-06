---
dg-publish: true
---
(Banach's Fixed Point Theorem/ Contraction Mapping Principle)
Let $(X,d)$ be a [[Completeness|complete]] [[Metric Space]] and let $f:X\to X$ be a [[Contraction Mapping]] on $X.$ Then, there exists a unique [[Fixed point]] $\bar{x}$ satisfying $f(\bar{x})=\bar{x}$. Further, $d(f^{\mathrm{o}n}(x_{0}),\bar{x})\to0$ as $n\to \infty$ for any $x_{0}\in X$
- guarantees existence of a unique, globally attractive fixed point


If you have a function $f$ that is known to be contractive on a complete metric space $X$, and you need to find its fixed point $\bar{x},$ you need only pick a single initial point $x_{0}\in X$ and apply the function $f$ repeatedly to it. The sequence of points obtained is guaranteed to grow arbitrarily close to $\bar{x}$

# Proof
Choose $x_{0}\in X$ and define a sequence via 
$$
x_{i+ 1} = f(x_{i})
$$
- $x_{n}=f^{\mathrm{o}n}(x_{0})$
- $f^{\mathrm{o}0}(x_{0})=x_{0}$

Let $m$ and $n$ be positive integers such that $m<n.$ Then
$$
\begin{align}
d(x_{m},x_{n}) & = d(f^{\mathrm{o}m}(x_{0}),f^{\mathrm{o}n}(x_{0})) \\
 & = d(f(f^{\mathrm{o}(m-1)}(x_{0})),f(f^{\mathrm{o}(n-1)}(x_{0}))) \\
 & \leq c \ d(f^{\mathrm{o}(m-1)}(x_{0}),f^{\mathrm{o}(n-1)}(x_{0})) \quad \text{ with }c\in [0,1) \\
 & \leq c^{2}\ d(f^{\mathrm{o}(m-2)}(x_{0}),f^{\mathrm{o}(n-2)}(x_{0}) ) \\
 & \dots \\
d(x_{m},x_{n}) & \leq c^{m}\ d(x_{0},f^{\mathrm{o}(n-m)}(x_{0})) \quad(1)
\end{align}
$$
On the side, consider the quantity
$$\begin{align}
d(x_{0},f^{\mathrm{0}k}(x_{0}))  & = d(x_{0},x_{k}) \quad \text{ for } k\geq 1 \\
 & \leq d(x_{0},x_{1}) + d(x_{1},x_{2})+ \dots+ d(x_{k-1},x_{k}) \\
 & = d(x_{0},x_{1}) + d(f(x_{0}),f(x_{1}))+ \dots+ d(f^{\mathrm{o}(k-1)}(x_{0}),f^{\mathrm{o}(k-1)(x_{1})}) \\
 & \leq d(x_{0},x_{1})+ c\ d(c_{0},c_{1})+ \dots+ c^{k-1}\ d(x_{0},x_{1}) \\
 & =[1+ c+ c^{2}+ \dots+ c^{k-1}] d(x_{0},x_{1}) \\
 & \leq d(x_{0},x_{1}) \sum_{i=0}^{\infty} c_{i} \quad \text{Geometric series} \\
 & = d(x_{0},x_{1}) \left( \frac{1}{1-c} \right)
\end{align}
$$
Using this in the result from $(1):$
$$
\begin{align}
d(x_{m},x_{n})  & \leq c^{m}\ d(c_{0},f^{\mathrm{o}(n-m)}(x_{0})) \\
 & \leq c^{m}\ d(x_{0},x_{1}) \frac{1}{1-c}
\end{align}
$$
Since $d(x_{0},x_{1}) \frac{1}{1-c}$ is finite given any choice of $x_{0}\neq \bar{x}$ and contraction factor $c$, and since $c\in[0,1)$, causing $c^{m}$ to be arbitrarily small (with large enough $m$), we can see $d(x_{m},x_{n})$ can also be made arbitrarily small.
- given $\epsilon >0\ \exists N\in \mathbb{N}$ such that $m,n>N \to d(x_{m},x_{n})<\epsilon$
Thus $\{ x_{n} \}$ is cauchy.

$X$ is complete by hypothesis, so $\{ x_{n} \}$ converges to a point $\bar{x}\in X$

Now consider:
$$
x_{n+ 1}=f(x_{n})
$$
If we let $n\to \infty$, then $x_{n+1}\to \bar{x}$ and $f(x_{n})\to f(\bar{x})=\bar{x}$
- 

So we see that $f(\bar{x})=\bar{x}$ and $\bar{x}$ must be a fixed point


To prove $\bar{x}$ is unique, assume not:

There exists $\bar{x},\bar{y}\in X$ such that 
$$
f(\bar{x})=\bar{x}\quad \text{and} \quad f(\bar{y})=\bar{y}
$$
But then,
$$
\begin{align}
d(\bar{x},\bar{y})  & = d(f(\bar{x}),f(\bar{y})) \leq c\ d(\bar{x},\bar{y}) \\
d(\bar{x},\bar{y}) &  \leq c\ d(\bar{x},\bar{y})
\end{align}
$$
which implies $c\geq 1$. But $c\in [0,1)$ since $f$ is a contraction. Contradiction!

Thus $\bar{x}$ is unique.