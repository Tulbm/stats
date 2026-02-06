---
dg-publish: true
---
A more formal definition of bounded sets uses [[Diameter and Bounded Sets]]

Let $K$ be a non-empty subset of $\mathbb{R}$. $K$ is a **bounded** set if there exist real number $m$ and $M$ such that $m\leq k$ and $M\geq k$ for all $k\in K$.

We call $m$ a lower bound and $M$ an upper bound on the set $K$

$M^{*}$ is said to be a least upper bound or **supremum** for a set $K \subset \mathbb{R}$ if $M^{*}$ is an upper bound for $K$, while $M^{*}<M$ for any other upper bound $M$.
$$
M^{*}=\text{sup}(K)
$$
$m^{*}$ is said the be a greatest lower bound or **infimum** for a set $K \subset \mathbb{R}$ if $m^{*}$ is a lower bound for $K$, while $m^{*}>m$ for any other lower bound $m$.
$$
m^{*}=\text{inf}(K)
$$
If the supremum $M^{*}$ of a set $K$ is also an element of $K$, then $M^{*}$ must be the greatest element of $K$, $\text{max}(K)$. Similarly for the infimum, with $\text{min}(K)$
- In open sets $K=(x,y)$, the $\text{min}$ and $\text{max}$ don't exist, but the supremum and infimum do ($\text{sup}(K)=y, \ \text{inf}(K)=x$)

The domain of the set can be denoted with subscripts on the functions:
- $\underset{x \leq 0}{\text{max}}\{ e^{x} \}=1$
- $\underset{x\geq 0}{\text{sup}}\{ e^{x} \}= \text{DNE}$

Every nonempty subset of $\mathbb{R}$ that is bounded above has a least upper bound.
Every nonempty subset of $\mathbb{R}$ that is bounded below has a greatest lower bound.

# Theorems

## Let $K$ be a non-empty subset of $\mathbb{R}$ that is bounded above. let $M \in \mathbb{R}$ be an upper bound for $K$. Then, the following statements about $M$ are equivalent:
1. $M=\text{sup}(K)$
2. For any $\epsilon >0$, there exists $x\in K$ such that $|x-M|<\epsilon$
3. For any $\epsilon >0$, there exists $x\in K$ such that $x\in (M-\epsilon, M]$

## Let $K\subset \mathbb{R}$ and let $M$ be a lower bound on $K$. Prove that if $M=inf(K)$ that for any $\epsilon> 0$ there exists $x\in K$ such that $x\in [M,M+ \epsilon)$

If $M$ = inf$(K)$, then that means it is the greatest of all lower bounds on $K$.

Contradiction: Assume that for any $\epsilon>0$, there doesn't exist $x\in K$ such that $x\in [M,M+ \epsilon)$

Take $\epsilon = 1,$ then that means no $x\in K$ exists in the bound $[M,M+ 1)$.  
### proof

Theorem is proved with by doing 
$$
1\to 2\to 3\to 1
$$
$1\to 2$
By contradiction:

Assume (1), $M=\text{sup}(K)$ and $\neg (2)$, that there is at least one $\epsilon>0$ for which 
$$
|x-M|\geq \epsilon \quad\forall x\in  K
$$
This would mean that either $x\geq M+\epsilon$ or $x\leq M-\epsilon$
- first case: $x$ cannot be greater than $M$ since $M$ is an upper bound on $K$
- second case: If $x\leq M-\epsilon$ $\forall x$ then we have found another upper bound for $K$. As $M-\epsilon  <M$ this upper bound would be a lesser upper bound than $M$, which we assumed was the supremum (least upper bound). Contradiction!

Thus $1\to 2$

$2\to 3$

If $|x-M|<\epsilon$, we have that $x\in(M-\epsilon,M+\epsilon)$. But $x$ cannot be larger than $M$ since $M$ was an upper bound on the set $K$. 
Thus, $x\in (M-\epsilon,M]$, and we have $2\to 3$

$3\to1$

Here we will not assume that $M$ is the $sup(K)$ (still an upper bound), but we will assume (3), that:
For any $\epsilon >0$, there exists $x\in K$ such that $x\in (M-\epsilon, M]$

Then, there would exist an upper bound $u$ on $K$ that is less than $M$, such that
$$
u\geq x \quad \forall x \in  K
$$
with $u<M$, as $M\neq sup(K)$

Define $\delta= M-u$, the "gap between the two"

$\delta$ is a number, and if we choose any $\epsilon$ smaller than it, we can apply out assumption (3) and get:
$$
\exists x \in (M-\epsilon,M)
$$
But since $u=M-\delta<M-\epsilon$, $u$ could not be an upper bound on $K$. As it would not bound all elements of it. Contradiction!

Thus, $3\to 1$

## $\forall x\in \mathbb{R}, \exists n\in \mathbb{N}$ such that $n>x$ (Archimedean)

(Archimedean Property)
Suppose not.
Then there exists as real number $M$ larger than all elements of $\mathbb{N}$.

We can see that $M$ is an upper bound on $\mathbb{N}$. Thus, by the least upper bound property, $\mathbb{N}$ must have a least upper bound $M^{*}$
By the previous theorem, 
- For any $\epsilon >0$, there exists $a \in \mathbb{N}$ such that $a\in (M^{*}-\epsilon, M^{*}]$
- (as $\mathbb{N} \subset \mathbb{R}$ I guess this is okay)

Choosing $\epsilon=\frac{1}{2}$, we would be able to find an element $a\in \mathbb{N}$ in the interval $\left( M^{*}- \frac{1}{2},M^{*} \right]$

But, we know from the definition of $\mathbb{N}$, that if $a\in \mathbb{N}$, then $a+1$ is also a natural number. So:
$$\begin{align}
M^{*}- \frac{1}{2}  & < a \leq M^{*} \\
M^{*}+ \frac{1}{2}  & < a+1 \leq M^{*}+ 1
\end{align}
$$
We find $a+1$, which is an element of $\mathbb{N}$ bigger than $M^{*}$

So $M^{*}$ can't have been an upper bound at all. Contradiction! Therefore the property is true.

## $\forall \epsilon  >0\in \mathbb{R}, \exists n\in\mathbb{N}, \frac{1}{n}<\epsilon$

Consider any $\epsilon>0$. From a previous result, $\frac{1}{\epsilon}$ is also positive

Archimedean property tells us that $\exists n\in \mathbb{N}$ such that $n> \frac{1}{\epsilon}$

By the previous result that $a<b\to \frac{1}{a}> \frac{1}{b}$ we have
$$
n> \frac{1}{e} \to \frac{1}{n}< \frac{1}{\frac{1}{e}} \to \frac{1}{n}< e
$$
[[Nested Interval Theorem]]


## Sup exists


## SUp exists

