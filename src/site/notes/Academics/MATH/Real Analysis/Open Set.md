---
dg-publish: true
---
A set is said to be **open** if it can be expressed as the union of a collection of [[Open ball]]s
- every point $a$ in the set has some open ball $B_{r}(a)$ that lies entirely in the set

Any intervals that do not include their endpoints is open
- $S_{1}=(5,25)$ 
- $S_{2}=(0,1) \cup (2,3)$)
The entirety of $\mathbb{R}$ is open
- $\dots \cup (-1,0) \cup (- \frac{1}{2}, \frac{1}{2}) \cup (0,1)\cup \dots$ 
- $\bigcup _{k \in \mathbb{Z}} (\frac{k}{2}-0.5, \frac{k}{2}+ 0.5)$
The empty set $\emptyset$ is trivially open (union of a collection of zero balls)

Every union of open sets is open

Every finite intersection of open sets is open
- not every intersection of open sets is open, as certain infinite intersections may not be
$$
\bigcap _{k=1}^{\infty} \left( - \frac{1}{k}, \frac{1}{k} \right) =\{ 0 \} \text{ (not open)}, \quad k \in  \mathbb{N}
$$


Every single element in a discrete space is open
- every element is an isolated point

# Theorems
Let $(X,d)$ be a metric space and let $S$ be a subset of $X$. Then $S$ is an open set $\iff \forall a\in S\ \exists r>0$ such that $B_{r}(a)\subseteq S$ 
- it is possible to draw $B_{r}(a)$ such that the ball is completely in $S$

## Proof
Both ways:
1. $S$ open $\to$ $\forall a \in S\ \exists r>0 \ | \ B_{r}(a) \subseteq S$
Then $S=$ union of a collection of open balls.
$$
= \bigcup _{i \in  I} B_{r_{i}}(x_{i}) \text{ with each } B_{r_{i}}(x_{i}) \text{ being an open ball, and index set } I
$$
Now, consider any $a\in S$. Then $a$ belongs to this union of sets, and thus belongs to at least one of the sets/open balls in the union.

Say this ball is $B_{r_{k}}(x_{k})$ for some $k\in I$.

Suppose we choose any $r\leq r_{k}- d(a,x_{k})$. Then for any $x\in  B_{r}(a):$
 $$
\begin{align}
d(x_{k},x)  & \leq d(x_{k},a)+d(a,x) \\
 &  <  d(x_{k},a) + r \quad \text{ as }x \text{ is in }B_{r}(a) \\
 & \leq d(a,x_{k}) + r_{k} - d(a,x_{k}) \\
 &  \leq r_{k} \\
\therefore d(x_{k},x)  & < r_{k} \Rightarrow x \in B_{r_{k}}(x_{k})
\end{align}
$$
we get a new ball $B_{r}(a)$, such that all of its elements $x$ are also contained in $B_{r_{k}}(x_{k})$, that is, $B_{r}(a)\subseteq B_{r_{k}}(x_{k})$. 

Thus $B_{r}(a)\subseteq B_{r_{k}}(x_{k}) \subseteq S \Longrightarrow B_{r}(a) \subseteq S$

$\therefore\forall a\in S, \exists r>0 \ | \ B_{r}(a) \subseteq S$ 



2. $\forall a \in S\ \exists r>0 \ | \ B_{r}(a) \subseteq S\to$ S open
We now want to prove the other way:

Suppose for every $a\in S$ $\exists r>0$ such that $Br(a)\subseteq S$

We want to prove that $S$ is open, i.e. that
$$\begin{align}
S & =\text{a union of open balls} \\
S & =\bigcup _{i \in  I}B_{r_{i}}(x_{i})
\end{align}
$$
Consider the union of all balls that exist by hypothesis about any $a\in S$
- $S$ cannot contain any additional points that are outside this union, since this violates that every point is the centre of an open ball contained in $S$

Thus, $S$ is no bigger than this union, i.e. 
$$
S\subseteq \bigcup _{i\in I} B_{r_{i}}(a_{i}) \quad (1)
$$
Further, since each ball is contained in $S$, the union of all such balls must be as well. So, 
$$
\bigcup _{i\in I} B_{r_{i}}(a_{i}) \subseteq S \quad (2)
$$
From $(1)$ and $(2)$, we see
$$
S=\bigcup _{i\in I} B_{r_{i}}(a_{i})
$$

 

# Examples
1. 
Consider the metric space $(\mathbb{R},d)$ with standard absolute value measuring [[Distance Function]] $d(x,y)=|x-y|$
Then:
- $B_{2}(-3)=(-5,-1)$
- $B_{10}(10)= (0,20)$
- $B_{r}(a)=(a-r,a+r)$

2. 
Consider the metric space $(\mathbb{R}^{2},d)$ where $d$ represents the standard Euclidean Metric
- $B_{1}(1,-1)=$ disk of radius $1$ about $(1,-1)$, not including the boundary
- $B_{r}(\mathbf{a})=$ disk of radius $r$ about $\mathbf{a}$, not including the boundary

3. 
Consider the metric space ($\mathbb{R}^{2},d$) where $d_{\text{Manhattan}}(\mathbf{x},\mathbf{y})=|x_{1}-y_{1}|+|x_{2}-y_{2}|$ 

The Manhattan metric sums the vertical distance plus the horizontal distance from points
- $B_{1}(0,2)=$ all points inside the diamond formed by the points $(0,3),(0,1), (-1,2),(1,2)$

4. 
Consider the metric space $(\mathbb{N},d)$ with $d(x,y)=|x=y|$
- $B_{5}(2)= \{ 1,2,3,4,5,6 \}$
- $B_{ 1/2}(1)=\{ 1 \}$
