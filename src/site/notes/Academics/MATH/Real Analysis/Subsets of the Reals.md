---
dg-publish: true
---
$\mathbb{Z}$(Integers): Defined as $\mathbb{N}\cup \{ 0 \}\cup{\text{ set of all additive inverse elements of }\mathbb{N}}$ 

$\mathbb{Q}$(Rational numbers): Defined as the set of all allowable quotients of elements of $\mathbb{Z}$ 

$\mathbb{R} \setminus \mathbb{Q}$ is denoted $\bar{\mathbb{Q}}$: The set of all irrational numbers

$\mathbb{N}$: 
Letting $a\in\mathbb{R}$ and $k\in \mathbb{N}$ we define:
$$
ka=a+a+\dots+a \quad k\text{ times}
$$


## Theorems

1. If $a$ is a positive real number, then for all $m,n\in\mathbb{N}$ we have that $ma\neq na$ if $m\neq n$

Assume instead that $ma=na$, then $ma-na=0$

We have by assumption that $m\neq n$. Without loss of generality, let's assume that $m>n$. Then:
$$
\begin{align}
ma-na & = a\text{ added m times} - (\text{ a added n times}) \\
 & =a +a+\dots+a-(a+a+\dots+a) \\
 & =a+a+\dots +a \quad \text{(m-n times, the leftovers)}
\end{align}
$$
Each of the $a$'s is a positive number. So their sum must also be positive.

But we assumed that $ma-na=0$. Therefore blablba

2. $\mathbb{R}$ contains an infinite sequence of distinct terms, and is therefore an infinite set
From 1, we know that $a$ is distinct from $a+a$, which is distinct from $a+a+a$ and so on...
So this is a sequence of distinct terms, and thus $\mathbb{R}$ is an infinite set
- $2=1+1$
- $3=1+1+1$

# Proofs 

## $ab\in R^{-}$
Given $a\in R^{+}$ and $b\in \mathbb{R}^{-}$, show that the product $ab\in \mathbb{R}^{-}$:

Assume $ab\in \mathbb{R}^{+}$
.... (practice)



## $p^{2}=2n \to p=2j$
Let $p\in\mathbb{N}$, and let $p^{2}$ represent $p\times p$. Show that if $p^{2}$ is an even number, then $p$ must also be even.

[[Logic|Contraposition]]: Assume $p$ is odd (not even), we must show that $p^{2}$ is an odd number (not even)

$p$ odd means that $p$ can be expressed as $p=2k-1, \quad k\in \mathbb{N}$

We consider 
$$
\begin{align}
p^{2}=pp  & =(2k-1)(2k-1) \\
 & =4k^{2}-2k-2k+1 \\
 & = 4k^{2}-4k+1 \\
 & =4k^{2}-4k+2-1 \\
 & =2(2k^{2}-2k+1)-1 \\
 & = 2j -1, \quad j=2k^{2}-2k+1 \in \mathbb{N}
\end{align}
$$
$2j-1$ is in the form of an odd number, $\therefore$ $p^{2}$ must be odd

So, $p$ odd $\to p^{2}$ odd and hence $p^{2}$ even $\to p$ even

## $\sqrt{ 2 }\in \bar{\mathbb{Q}}$

Assume there is an element of $\mathbb{R}$ such that $x^{2}=2$, which we call $\sqrt{ 2 }$
Suppose $\sqrt{ 2 }$ exists and is rational.

It may be written as
$$
\sqrt{ 2 }= \frac{p}{q}
$$
where $p$ and $q$ are integers where $q\neq 0$ and $p$ and $q$ are relative primes

Then:
$$\begin{align}
2  & = \frac{p^{2}}{q^{2}} \\
 2 q^{2}  & = p^{2} 
\end{align}
$$
We see that $p^{2}$ must be even as it is 2 times an integer. From the last proof, $p$ is also even. Thus, $p=2n$, where $n\in \mathbb{Z}$. We get:
$$
\begin{align}
2q^{2} & =(2n)^{2} \\
 & = 4n^{2} \\
q^{2} & =2n^{2}
\end{align}
$$
and we find that $q^{2}$ must also be even $\to$ q is even

But if $p$ and $q$ are both even, $2$ divides both and they couldn't have been relative primes to begin with. (Contradiction)

Therefore, $\sqrt{ 2 }$ cannot be written as $p/q$ and must be irrational
