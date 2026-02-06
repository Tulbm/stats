---
dg-publish: true
---
Let $(X,d)$ be a [[Metric Space]]. The **diameter** of a subset $S$ of $X$ is given by
$$
\text{sup}\{ d(a,b):a,b\in  S \}
$$
sometimes denoted $\text{diam}(S)$
- largest possible distance between two elements of that set

If the distance $d(a,b)$ has no upper bound, then the diameter of $S$ is said to be infinite (and S is unbounded)

For $S=\emptyset$ we define the diameter to be equal to zero


# Theorems

## $S$ has finite diameter if and only if, for any $a\in X$, there exists a finite number $r>0$ such that $S \subseteq B_{r}(a)$
Let $(X,d)$ be a metric space, and let $S$ be a nonempty subset of $X$. 
A subset $X$ of $S$ is said to be bounded if it satisfies either of the conditions of this theorem
### Proof

$(\Rightarrow)$
Suppose that $S$ has finite diameter. We must show that $\forall a \in X,\ \exists$ finite number $r>0$ such that $S\subseteq B_{r}(a)$

Consider any $a\in X$. Notice that for any $x_{1},x_{2} \in S$
$$
\begin{align}
d(a,x_{2}) & \leq d(a,x_{1})+d(x_{1},x_{2}) \\
 & \leq d(a,x_{1}) + \text{diam}(S)
\end{align}
$$
So if we choose $r>d(a,x_{1})+ \text{diam}(S)$ $\forall x_{1}\in X$, then every $x \in S$ will be contained in $B_{r}(a)$

$(\Leftarrow)$
Suppose given any $a\in X$, $\exists$ a finite number $r>0$ so that $S\subseteq B_{r}(a)$

Consider the distance between any two points $x_{1},x_{2}\in S$. 
$$
\begin{align}
d(x_{1},x_{2})  & \leq d(x_{1},a) + d(a,x_{2}) \\
 & \leq r+ r \quad \text{ because }S,x_{1},x_{2} \in  B_{r}(a)\\
 &  = 2r, \quad \text{ which is finite as long as }r \text{ is}
\end{align}
$$
Which means that $d(x_{1},x_{2})$ is bounded above by $2r$, and so by the least upper bound property, 
$$
\text{sup}\{ d(x_{1},x_{2}): x_{1},x_{2}\in  S \} \text{ must exist}
$$
and is finite

And that is the definition of the diameter of S