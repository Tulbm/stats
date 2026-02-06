---
dg-publish: true
---
Let $(X,d)$ be a [[Metric Space]] and $S$ be a subset of $X$. A point $x\in X$ is called a **limit/accumulation point** of $S$ if any of the following conditions are satisfied, all of which are logically equivalent:
1. There exists a sequence of points in $S\setminus \{ x \}$ converging to $x$
2. There exists a sequence of distinct points of $S$ converging to $x$
3. For all $r>0,B_{r}(x)$ contains infinitely many points of $S$
4. For all $r>0, B_{r}(x)$ contains at least a point of $S\setminus \{ x \}$ 

Limit points are the "opposite" of isolated points.
An element of a set can be a limit point or not, an element outside of the set can be a limit point of it or not.

Set of all limit points of:
- $[3,5) \cup (6,7) \cup \{ 10 \}$ is $[3,5] \cup [6,7]$
- $(-1,0)\cup (0,1)$ is $[-1,1]$
- $\{ x : x\in \mathbb{R} \}$ is $\mathbb{R}$
- $\{ x: x\in \mathbb{Q} \}$ is $\mathbb{R}$