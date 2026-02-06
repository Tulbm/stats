---
dg-publish: true
---
A subset of $X$ is said to be closed if it contains all of its own [[Limit point]]s.
- $[0,1]$ is closed, since it contains all of its endpoints
- $\{ -4 \}$ is closed, as it doesn't have any limit points to begin with

Given a [[Metric Space]] $(X,d)$ both $X$ and the empty set are examples of closed sets. This means that $X$ and $\emptyset$ are both open and closed.

# Theorems

## $S$ is closed $\iff$ $S^{C}$ is open
Let $X$ be a metric space and $S \subseteq X$. Then $S$ is closed $\iff$ $S^{C}$ is open

1. If $S$ is closed $\Rightarrow$ $S^{C}$ is open

If $S$ is closed, then we know $S$ must contain all of its own limit points.

Thus, no elements/points of $S^{C}$ can be limit points 

Now consider $x\in S^{C},$ which we know is not a limit point of $S$. From that we know it does not satisfy the definition of limit points for $S$:
- For all $r>0, B_{r}(x)$ contains at least a point of $S\setminus \{ x \}$ 

So it is false that $\forall r>0, B_{r}(x)$ contains at least a point of $S\setminus \{ x \}$. There exists $r>0$ so that $B_{r}(x)$ contains no points of $S$

So $B_{r}(x)\subseteq S^{C}$ , and since we can find such a ball for every $x\in S^{C}$ we see that $S^{C}$ must be open

2. If $S^{C}$ is open $\Rightarrow S$ is closed

Consider any point $L$ such that $\{ a_{n} \}$ converges to $L$ while $\{ a_{n} \}\subseteq S$

If $\{ a_{n} \}\to L$, then for any $\epsilon>0\exists N\in \mathbb{N}, n>N\to d(a_{n},L)<\epsilon$

If we can show that $L\in S$, then $S$ must be closed. Assume $L\notin S$ to prove by contradiction:

If $L\notin S$ then $L\in S^{C}$. Since by hypothesis $S^{C}$ is open, we can find $r>0$ so that $B_{r}(L)\subseteq S^{C}$

This violates the initial assumption, which says that sequence terms $\{ a_{n} \}\in S$ will be found in any size ball about $L$ ($d(a_{n},L)$). Contradiction!

$\therefore L\in S$ and so $S$ is closed

## Any intersection of closed sets is closed, every finite union of closed sits is closed

It is not true in general that infinite unions of closed sets are closed. Consider
$$
\bigcup _{k=2}^{\infty}\left[  \frac{1}{k},1 \right] = \left[  \frac{1}{2},1 \right] \cup \left[ \frac{1}{3}, 1 \right] \cup \dots
$$
which is given by $(0,1]$, which is not closed in $\mathbb{R}$

