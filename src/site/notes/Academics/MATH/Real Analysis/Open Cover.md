---
dg-publish: true
---
Let $X$ be a [[Metric Space]], and let $S\subseteq X$. Letting $\Lambda$ be some indexing set, suppose that $\{ U_{\lambda} \}_{\lambda \in \Lambda}$ is a collection of open subsets of $X$, and that we have
$$
S\subseteq \bigcup _{\lambda\in  \Lambda} U_{\lambda}
$$
Then $\{ U_{\lambda} \}_{\lambda\in \Lambda}$ is said to be an **open cover** for $S$
- as a result of being a union of open sets, the open cover will always be an open set
- It is trivial to find open covers, there are not a lot of restrictions, but it is hard to find finite [[Subcover]]s sometimes

# Examples

## 1
Consider the real interval $S=(0,1)$ and consider the set $U_{n}=\left( \frac{1}{n},1 \right)$ for $n\in \mathbb{N}$. Then $\{ U_{n} \}$ provides an open cover for $S=(0,1)$


## 2
Consider $S=\{ 0 \}\in \mathbb{R}$ and consider the sets $U_{n}=\left( - \frac{1}{n}, \frac{1}{n} \right)$ for $n\in \mathbb{N}$. Then $\{ U_{n} \}$ provides an open cover for $S$. So does $U_{1},U_{2}\dots$ 
- $\{ 0 \}$ does not as it is not an open set


## 3
Let $S\subset X$ where $X$ is a metric space. $\forall x\in S$, consider the open sets $B_{r}(x)$ for $r>0$. Then the set of all such $B_{r}(x)$ provides an open cover for $S$.

## 4
Let $S=\mathbb{R}$ and consider the open intervals $U_{n}=\left(  \frac{1}{2}n, \frac{1}{2}n + 1 \right)$ for $n\in \mathbb{Z}$. Then $\{ U_{n} \}$ provides an open cover for $S$.

## 5
Let $S=[0,1]\subset \mathbb{R}$ and consider the open intervals $U_{\lambda}=\left( - \frac{1}{4}+ \lambda, \frac{3}{4}+ \lambda \right)$ for $\lambda \in [0, \frac{1}{2}], \lambda \in \mathbb{R}$. Then $\{ U_{n} \}$ provides an open cover for $S$


