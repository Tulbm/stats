---
dg-publish: true
---
Let $X$ be a [[Metric Space]] and $S$ be any subset of $X$. A point $x\in S$ is called an **interior point** of $S$ if there is an [[Open ball]] about $x$ that is totally contained within $S$. We denote $Int(S)$ as the set of all interior points of $S$. 

The following are true:
1. $Int(S)$ is an open subset of $X$
2. Every open subset of $X$ that is contained in $S$ is also contained in $Int(S)$
3. The union of all open subsets of $X$ that are contained in $S$ is equal to $Int(S)$
4. $S$ is open if and only if $S=Int(S)$

# Proofs

## 3

Let $U$ be the union of all open subset of $X$ contained in $S$. We must show $U=Int(S)$

We can do this if we can show that $U\subseteq Int(S)$ and $Int(S) \subseteq U$

$(U\subseteq Int(S))$
Suppose $x\in U$. Then $x$ belongs to at least one open subset $S^{*}\subseteq S$

Since $S^{*}$ is open, $\exists r>0$ such that $B_{r}(x) \subseteq S^{*}\subseteq S$. But this makes $x$ an interior point of $S$. So $x\in Int(S)$, $\therefore U \subseteq Int(S)$

$(Int(S) \subseteq U)$
Suppose $x\in Int(S)$. $x$ is an interior point, so $\exists r>0$ such that $B_{r}(x) \subseteq S$

$B_{r}(x)$ is an open ball and thus an open set that is contained in $S$. Thus $x\in B_{r}(x) \subseteq U$
$\therefore Int(S) \subseteq U$

From both of these, $U=Int(S)$
