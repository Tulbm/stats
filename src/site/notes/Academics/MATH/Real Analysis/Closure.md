---
dg-publish: true
---
Let $S$ be a subset of a metric space $X$. The closure of $S$, denoted $\bar{S}$, is the intersection of all [[Closed Sets|closed subsets]] of $X$ that contain $S$.

The following are true about the closure of a given subset $S\subseteq X:$
1. $\bar{S}$ exists
2. $\bar{S}$ is a subset of each closed subset that contains $S$
3. $\bar{S}$ is itself a closed set
4. $S$ is closed if and only if $S=\bar{S}$

Let $x\in X$. The following are equivalent:
1. There exists a sequence in $S$ that converges to $x$
2. Every open ball about $x$ contains a point of $S$
3. For every open set $U$ containing $x,U\cap S \neq  \emptyset$
4. $x \in \bar{S}$

Let $S$ be a subset of a metric space $X$ and let $S_{L}$ be the set of all limit points of $S$. Then
$$
\bar{S}= S \cup S_{L}
$$


# Proofs


## 3. $\bar{S}$ is itself a closed set

$\bar{S}$ is defined as the intersection of closed sets, and since any intersection of closed sets is closed, $\bar{S}$ is itself a closed set.

## 4. $S$ is closed $\iff$ $S=\bar{S}$

### $S$ is closed $\Rightarrow S=\bar{S}$

Assume $S$ is closed, that means it contains all of its limit points, if any

We can show this is true if we can show that both:
1. $\bar{S} \subseteq S$ and
2. $S \subseteq \bar{S}$


1: $\bar{S}$ is the intersection of every closed set containing $S$. If $x\in \bar{S}$, then $x$ is an element of every closed set containing $S$. By hypothesis, $S$ is closed, so $S$ is a closed set containing $S,$ meaning $x\in S$.

Thus we see that $\bar{S} \subseteq S$

2: Now consider $x\in S$, $\bar{S}$ is the intersection of all closed sets containing $S$. If $x\in S$, then $x$ is an element of any set that contains $S$. So $x$ is an element of each of the closed sets that contain $S$, and so $x$ is in the intersection of all of these, meaning $x\in \bar{S}$

i.e. $S \subseteq \bar{S}$

With (1) and (2), $S=\bar{S}$

###  $S=\bar{S}\Rightarrow S$ is closed

$\bar{S}$ is defined as the intersection of closed sets, and since any intersection of closed sets is closed, $\bar{S}$ is itself a closed set. So if (by hypothesis) $S=\bar{S}$, then $S$ must be closed too.







