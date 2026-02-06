---
dg-publish: true
---
[[Sequences]] in which elements become arbitrarily close to one another

Let $(X,d)$ be a metric space. A sequence $\{ a_{n} \}_{n=1}^{\infty}$ is Cauchy if
$$
\forall \epsilon>0, \exists N\in  \mathbb{N} \ | \ m,n> N \to d(a_{m},a_{n})< \epsilon
$$
Very similar to the definition of [[Sequences and Convergence]] but:
- for a Cauchy sequence, the elements in the sequence must be arbitrarily close to one another, instead of to a point $x$



Completeness of $\mathbb{R}$

$$
\lim_{ n \to 0 } x_{n}=x^{*}
$$

$$
\forall\epsilon>0, \exists N>0 \text{ s.t.} |x_{n}-x_{m}| <\epsilon \forall n,m> N
$$
# Theorems

## If $\{ a_{n} \}$ converges, then it is a Cauchy sequence

If $\{ a_{n} \}$ converges to $L$, then $\forall \epsilon>0,\exists N\in \mathbb{N}\ |\ n>N \to d(a_{n},L)<\epsilon$

Choose any $\epsilon>0$ and let $\epsilon_{2}= \frac{1}{2}\epsilon$. We know that there must exists $N\in \mathbb{N}$ such that:
- $d(a_{n},L)<\epsilon _{2}$ for $n>N$ and
- $d(a_{m},L)<\epsilon_{2}$ for $m>N$

We are interested in $d(a_{m},a_{n})$

For $m,n>N$ we have 
$$
\begin{align}
d(a_{m},a_{n}) & \leq d(a_{m},L) + d(L, a_{n}) \\
 & = d(a_{m},L)+ d(a_{n},L) \\
 & < \epsilon_{2} + \epsilon_{2} &  \\
 & = \epsilon
\end{align}
$$
So it is true that $\exists \epsilon$ such that $d(a_{m},a_{n})<\epsilon$

