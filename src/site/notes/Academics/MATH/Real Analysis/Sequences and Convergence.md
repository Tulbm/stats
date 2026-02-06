---
dg-publish: true
---
A sequence
$$
\{ a_{i} \}^{\infty}_{i=1} = a_{1}, a_{2}, a_{3},\dots
$$
is said to converge to a number $x$ if $\forall \epsilon>0\ \exists N \in \mathbb{N}$ so that if $n> N$ we have 
$$
d(a_{n},x)< \epsilon
$$
- we can find an index in the sequence where the distance starts getting smaller than the tiny $\epsilon$ (arbitrarily close to $x$)

We call the associated sequence $\{ a_{i} \}^{\infty}_{i=N}$ the $N^{\text{th}}$ tail of the sequence.
- if an $N^{\text{th}}$ tail of a sequence converges, then the sequence itself also converges

A constant sequence is one in which all terms are equal
- an eventually-constant sequence is a sequence that has a constant tail

A subsequence is simply an ordered selection of terms from another sequence
- if $\{ c_{n} \}$ is a subsequence of $\{ b_{n} \}$, and $\{ b_{n} \}$ is a subsequence of $\{ a_{n} \}$, then it must be the case that $\{ c_{n} \}$ is a subsequence of $\{ a_{n} \}$

For any bounded subset $S$ of $\mathbb{R}$, there exists sequences whose elements are in $S$ that converges to $\text{sup}S$ and $\text{inf}S$
# Theorems

Let $\{ a_{i} \}$ be a sequence in a metric space $(X,d)$. 
## The following statements are equivalent:
1. The sequence $\{ a_{i} \}$ converges to $L\in X$
2. For every open set $S$ containing $L$, there exists a natural number $N$ such that for all $n>N,a_{n}\in S$
3. For every $\epsilon>0,$ there exists a natural number $N$ such that if $n>N$, then $a_{n}\in B_{\epsilon}(L)$

### Proof
$(1)\to (2)$

If $(1)$ is true, by hypothesis $\{ a_{i} \}$ converges to $L$
- $\forall \epsilon>0, \exists N\in \mathbb{N}$ so that $n>N\to d(a_{n},L)<\epsilon$

Now to get to $(2)$ consider any open set $S$ containing L. Since $S$ is open, there exists $r>0$ such that $B_{r}(L)$ is completely contained in $S$. 

$\{ a_{i} \}$ converges to $L$, so (setting $\epsilon=r$) there exists $N\in \mathbb{N}$ such that $\forall n >N, d(a_{n},L)<r$

In other words, $a_{n}\in B_{r}(L)$ for all $n>N$, and since $B_{r}(L)\subseteq S$, we have that $a_{n}\in S$ as well.

$(2)\to (3)$
Suppose: For every open set $S$ containing $L$, there exists a natural number $N$ such that for all $n>N,a_{n}\in S$

We must prove: For every $\epsilon>0,$ there exists a natural number $N$ such that if $n>N$, then $a_{n}\in B_{\epsilon}(L)$

We note that $B_{\epsilon}(L)$ is itself an open set containing $L$. $(2)$ says any open set will have $N$ such that $n>N\to a_{n}\in B_{\epsilon}(L)$. Thus $(3)$ holds

$(3)\to (1)$
Suppose: For every $\epsilon>0,$ there exists a natural number $N$ such that if $n>N$, then $a_{n}\in B_{\epsilon}(L)$

We must prove: $\{ a_{i} \}$ converges to $L$, i.e. $\forall \epsilon>0, \ \exists N\in \mathbb{N}$ s.t. $n>N\to d(a_{n},L)<\epsilon$

We can see that if $a_{n}\in B_{\epsilon}(L)$ (true by hypothesis) then by definition of balls, $d(a_{n},L)<\epsilon$, which gives us the conclusion.


## Any convergent sequence is bounded

A sequence that converges to some $L$ is a bounded set, all of its elements can fit inside some finite-radius ball
### Proof
Suppose we have a sequence $\{ a_{n} \}$ that converges to some element $L$. That means 
$$
\forall \epsilon >0, \exists N\in  \mathbb{N}\ | \ n>N \to d(a_{n},L)< \epsilon
$$
Therefore, given $\epsilon>0$, we know that all $\{ a_{n} \}_{n> N}$ must exist within $B_{\epsilon}(L)$ (an infinite number of them)
This leaves a finite number of elements $a_{1},a_{2},\dots,a_{N}$

Since there are a finite number of these,
$$
\underset{ i=1\dots N }{ \text{max} } \{ d(a_{i},L) \}
$$
is a well-defined and finite quantity. Let this max be $r$. Then choosing $r^{*}=\text{max}\{ \epsilon,r \}$ all elements of $\{ a_{n} \}$ must be contained in $B_{r^{*}}(L)$ and thus $\{ a_{n} \}$ is bounded
# Theorems in $(\mathbb{R}, |\cdot|)$
Let $\{ a_{n} \}$ be a sequence of real numbers
## Let $\{ a_{n} \}$ be a sequence that converges to $L\in \mathbb{R}$. Then, the related sequence $\{ |a_{n}| \}$ converges to $|L|$

$-1,-1.9,-1.99,\dots$ converges to $-2$
Then
$1,1.9,1.99,\dots$ converges to $2$

Important to note the converse is not true.

$-1,1,-1,1,-1,\dots$ does not converge
But the related sequence $1,1,1,1,\dots$ does


## Suppose that $k\in \mathbb{R}$ and that $a_{n}\geq k$ for each natural number $n$. If this sequence converges to a number $L$, then it must be the case that $L\geq k$

Proof by contradiction: Suppose instead that $L<k$

Then if $\{ a_{n} \}$ converges to $L$, then $\forall \epsilon>0$ there exists $N\in \mathbb{N}$ so that $n>N \to d(a_{n},L)= |a_{n}-L| <\epsilon$

But if we let $\epsilon \leq k-L$, then
$$
\begin{align}
|a_{n}-L|  & <\epsilon \\
|a_{n}-L |  & < k - L \\
L-k+ L  & < a_{n}  < L + k - L \\
2L - k  & <a_{n}  < k
\end{align}
$$

By hypothesis, each $a_{n}\geq k$, so we arrive at a contradiction.
Therefore it must be the case that $L\geq k$


- Similarly, if $a_{n}\leq k$ for each $n$ and $a_{n}$ converges to $L$, then $L\leq k$

## Let $\{ a_{n} \}$ and $\{ b_{n} \}$ be sequences of real numbers that converge to $L$ and $M$ respectively. If $a_{n}\geq b_{n}\forall n$ then $L>M$

## Sequence arithmetic
Suppose that $\{ a_{n} \}$ converges to $L$ while $\{ b_{n} \}$ converges to $M$. Then
1. $\{ a_{n}+b_{n} \}$ converges to $L+M$
2. $\{ a_{n}-b_{n} \}$ converges to $L-m$
3. $\{ a_{n}b_{n} \}$ converges to $LM$
4. $ka_{n}$ converges to $kL$ for any real constant $k$
5. $\left\{  \dfrac{a_{n}}{b_{n}}  \right\}$ converges to $\dfrac{L}{M}$ as long as $b_{i}$ and $M$ are not zero

### Proofs

1. 
By hypothesis, $\{ a_{n} \}\to L$ while $\{ b_{n} \}\to M$

That means $\forall \epsilon_{1}>0,\epsilon_{2}>0, \ \exists N_{1},N_{2}\in \mathbb{N}$ such that:
- $n>N_{1}\Rightarrow |a_{n}-L|<\epsilon_{1}$
- $n>N_{2}\Rightarrow |b_{n}-M|<\epsilon_{2}$
If $n>\text{max}\{ N_{1},N_{2} \},$ then both inequalities hold

So we have
- $-\epsilon_{1}<a_{n}-L<\epsilon_{1}$
- $-\epsilon_{2}<b_{n}-M<\epsilon_{2}$
Summing both:
$$
\begin{align}
-\epsilon_{1}-\epsilon_{2} & <(a_{n}-L) + (b_{n}-M) < \epsilon_{1}+\epsilon_{2} \\
-(\epsilon_{1}+\epsilon_{2})  & < a_{n}+b_{n}- (L+M) < \epsilon_{1}+ \epsilon_{2} \\
 & | a_{n}+ b_{n}-(L+M)| < \epsilon_{1}+ \epsilon_{2}
\end{align}
$$
Then let $\epsilon>0$ be $\epsilon=\epsilon_{1}+ \epsilon_{2}$. We have show that there exists an $N=\text{max}\{ N_{1},N_{2} \}$ such that for $n>N,\ |a_{n}+ b_{n} - (L+ M)| < \epsilon$

That means that $\{ a_{n}+ b_{n} \}$ converges to $L+ M$

