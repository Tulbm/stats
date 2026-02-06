---
dg-publish: true
---
Let $X$ be [[Metric Space]] and consider a subset $S \subseteq X$. The boundary of $S$, denoted $\partial S$, is defined as the intersection of the [[Closure]] $\bar{S}$ and $\bar{S^{C}}$. The following are true:
- $\partial S$ is a closed set
- An element $x\in X$ is in $\partial S$ $\iff$ $\forall r>0, B_{r}(x)$ contains elements of both $S$ and $S^{C}$
- $S$ is closed $\iff$ $S$ contains $\partial S$
- $S$ is open $\iff$ $S\cap \partial S = \emptyset$

A sequence in an open set $S$ that converges to an element on the boundary of the set ($\partial S$) does not necessarily converges in $S$, but we can say that it is a [[Cauchy Sequence]] 


# Proofs

## $S$ is closed $\iff$ $S$ contains $\partial S$
Proving both ways:

### $S$ is closed $\Rightarrow$ $S$ contains $\partial S$

Suppose $S$ is closed. We must prove $\partial S \subseteq S$.

As $\partial S=\bar{S} \cap \bar{S^{C}}$, which is a subset of $\bar{S}$ (by the definition of intersection)

Since $S$ is closed, $\bar{S} = S$ and so $\partial S$ is a subset of $S$ as well, i.e. $\partial S \subseteq S$


### $S$ contains $\partial S$ $\Rightarrow$ $S$ is closed

Suppose $S$ contains $\partial S$. We must show that $S$ is closed.

Proof by contradiction:
Suppose $S$ is not closed. That means $\exists$ $x$, a limit point of $S$, that is not in $S$, $x\in S^{C}$ and thus $x\in \bar{S^{C}}$ (the closure of the complement)

Further $x \in \bar{S}$, as $\bar{S}$ is the union of $S$ with its limit points ([[Closure]])

Hence $x\in \bar{S}$ as well as $\bar{S^{C}}$, so $x\in \bar{S} \cap \bar{S^{C}}$. This means that $x\in \partial S$. By the hypothesis $\partial S \subseteq S$, so $x\in S$ also (contradiction).

$\therefore$ $S$ is closed