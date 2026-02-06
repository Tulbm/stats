---
dg-publish: true
---
An infinite set $S$ is countable if there is a one-to-one correspondence between $S$ and $\mathbb{N}$
- "There is a sequence of distinct terms of $S$"

Countable sets include the natural, prime numbers, etc. But also the set of rational numbers:
$$
\begin{align}
\begin{bmatrix}
\dots & -2 & -1 & 0 & 1 & 2 & \dots \\
\dots  &  \frac{-2}{2}  & - \frac{1}{2} &  & \frac{1}{2} &  \frac{2}{2} &  \dots \\
\dots &  - \frac{2}{3} & - \frac{1}{3}  &   & \frac{1}{3} &  \frac{2}{3} &  \dots \\
\dots & \dots & \dots & \dots & .. & \dots & \dots
\end{bmatrix}
\end{align}
$$
And we could create a sequence of these numbers, by doing something like a spiral

# Theorems

## $\mathbb{R}$ is an uncountable set

If $\mathbb{R}$ were countable, we could craft an infinite sequence that includes all elements of the $\mathbb{R}$. We "try" to do this:

Such a sequence 
1. must be composed of distinct elements
2. cannot be [[Sequences#Monotone Increasing/Decreasing Sequence Theorem|monotone]] (increasing or decreasing)
- no matter the first element, there will always be a real number lesser and one greater than it
- between any two sequence terms $x,x+\epsilon$, we would always "miss" the elements in $(x,x+\epsilon)$

Assume WLOG that $x_{1}<x_{2}$. Let $I_{0}$ be the interval $[x_{1},x_{2}]$

There must be future elements in this interval, otherwise not all real numbers will be covered. Let $x_{m_{1}}$ and $x_{n_{1}}$ be the next two elements that that are selected from this interval. 

WLOG assume $x_{m_{1}}<x_{n_{1}}$. They define a new interval $I_{1}=[x_{m_{1}},x_{n_{1}}]$

We repeat the logic to find $x_{m_{2}}<x_{n_{2}}$, both withing $I_{1}$, defining an interval $I_{2}$. 

We can continue indefinitely, generating a set of nested intervals
$$
I_{k}=[x_{m_{k}},x_{n_{k}}]
$$
That satisfy the hypotheses of the [[Bounded Sets#Nested Interval Theorem|Nested Interval Theorem]]. 
So, the intersection 
$$
\bigcap _{k\in  \mathbb{N}} I_{k} \quad \text{ must be non empty}
$$
and cannot ever contain elements of our constructed sequence, as they form endpoints of the intervals $I_{k}=[x_{m_{k}},x_{n_{k}}]$, and any $x_{m_{k}}$ or $x_{n_{k}}$ cannot be contained in the "next" interval
$$
I_{k+1}=[x_{m_{k+1}},x_{n_{k+1}}]
$$
But this sequence was supposed to contain every point of $\mathbb{R}$, creating a contradiction.

This argument doesn't work for rational numbers $\mathbb{Q}$, as there are rational sets with a $sup\in \mathbb{R}$, thus the Nested Interval Theorem doesn't hold.







