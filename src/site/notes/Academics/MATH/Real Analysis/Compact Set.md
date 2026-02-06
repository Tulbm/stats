---
dg-publish: true
---
Let $X$ be a metric space. A subset of $X$ is compact if **every** [[Open Cover]] for $S$ has a finite [[Subcover]].

In other words, whenever $S$ is a subset of a union of open subsets of $X$, then it must also be the case that it is a subset of open finitely many of those subsets.

Compact sets have many properties that make them distinctive
- Any finite set is compact
- There any many non-compact sets
- Some compact sets are *not* finite, like any real closed intervals ($[0,1]$)

Let $X$ be a metric space and let $S\subseteq X$. Then the following are equivalent:
- $S$ is a [[Compact Set]]
- Every sequence in $S$ has a subsequence that converges to a point in $S$
- Every infinite subset of $S$ has a [[Limit point]] in $S$

A subset $S$ of $\mathbb{R}$ is compact if and only if it is closed and bounded
- $\{ a_{n} \}= \left\{  1, \frac{1}{2}, \frac{1}{3}, \dots  \right\}$ is not compact (not closed)
	- $\left(  \frac{1}{n},2 \right)$ for example is an open cover, with no finite subcover
- $\{ b_{n} \}=\left\{   0,1, \frac{1}{2}, \frac{1}{3},\dots  \right\}$ is compact (closed and bounded)

This tells us that
- Open intervals like $(a,b)$ must be not compact
- Half-open intervals like $[a,b)$ must be not compact
- $\mathbb{R}$ itself and $\mathbb{N}$ must be not compact (not bounded sets)
- Some infinite unions of closed intervals, such as $\{ [n,n+ 1] \}_{n\in \mathbb{N}}$ (which is unbounded) must be not compact

 Any closed, bounded subset of $\mathbb{R}^{n}$ is compact
 - much easier to use this than to worry about all open covers and finite subcovers

If $S$ is a [[Compact Set]], then $f(S)$, the forward [[Image]] of $S$ under $f$, is a compact subset of $Y$

# Proofs

## The closed interval $[a,b]$ is compact
Consider the metric space $(\mathbb{R}, |\cdot |).$ Let $a,b\in \mathbb{R}$ with $a<b$. 

Proof by contradiction: Assume $[a,b]$ is not compact.

If $[a,b]$ were not compact, there is an open cover for $[a,b]$ with no finite subcover.

Consider that $[a,b]$ can be written as the union of two intervals:
$$
\left[ a, \frac{a+b}{2} \right] \cup \left[ \frac{a+b}{2}, b \right]
$$
Further splitting up that interval, we could write $[a,b]$ as the union of $4,8,\dots, 2^{n}$ sub intervals
- each will have diameter of $\frac{b+a}{2}$

For there to be no finite subcover for $[a,b],$ it must be the case that at least one of these $2^{n}$ intervals has no finite subcover $\forall n\in \mathbb{N}$
- at least one part of the interval, that requires an infinite subcover when we make the open cover

Choose one such interval at each $n$, $I_{n}$ to be the at least one that requires an infinite subcover. If $I_{n}$ has no finite subcover we can then find $I_{n+ 1}\subset I_{n}$ for each $n$.

This produces a set $\{ I_{n} \}_{n+ \mathbb{N}}$ that is a sequence of nested intervals. By the [[Nested Interval Theorem]], the intersection of the $I_{n}$ intervals is nonempty. Since the lengths of the $I_{n}$ are 
$$
\frac{b-a}{2^{n}},
$$
the lengths of these intervals $\to 0$ as $n\to \infty$. Therefore the intersection of all $I_{n}$ must be a single element, $x\in \mathbb{R}$.

This $x\in [a,b]$ and as $[a,b]$ is covered, then $x$ must be an element of at least one [[Open Set]] $I^{*}$ in any open cover. 

Since $I^{*}$ is open, then there exists $\epsilon>0$ such that $(x-\epsilon,x+ \epsilon)$ is completely contained in $I^{*}$
- an [[Open ball]] $B_{\epsilon}(x)$

However, given any $\epsilon$ no matter how small, we can find $\mathbb{N}$ such that $\frac{b-a}{2^{n}}<\epsilon$, meaning there are subintervals $I_{N}$ that can be covered by $B_{\epsilon}(x)\subseteq I^{*}$, a single open set. Meaning that $I_{N}$ has a finite subcover, which creates a contradiction.

