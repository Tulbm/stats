---
dg-publish: true
---
Let $(X,d_{X})$ and $(Y,d_{Y})$ be [[Metric Space]]s, and let $f:X\to Y$ be a function. If $a$ is a limit point of $X$, then $f$ is **continuous** at $a$ if $\lim_{ x \to a }f(x)=f(a)$

# Theorems

## $f$ is continuous at $a$ $\iff$ given any sequence $\{ x_{n} \}\in X$ converging to $a$, the sequence $\{ f(x_{n}) \}$ converges to $f(a)$

$\Longrightarrow$
Suppose $f$ is continuous at $a.$ Then $\forall \epsilon>0\ \exists \delta>0,$ such that 
$$
d_{X}(x,a)<\delta \Longrightarrow d_{Y}(f(x),f(a))<\epsilon \quad (1)
$$
Now consider a sequence $\{ x_{n} \}\in X$ converging to $a$. We know there exists $N\in \mathbb{N}$ such that $n>N$ then $d_{X}(x_{n},a)<$ anything, we choose $\delta$, $d_{X}(x_{n},a)<\delta$

Suppose $\{ f(x_{n}) \}$ doesn't converge to $f(a)$ (looking for a contradiction)

Then there must be some $\epsilon>0$ for which $B_{\epsilon}(f(a))$ contains no points of $\{ f(x_{n}) \},$ ie. $d_{Y}(f(a),f(x_{n}))\geq \epsilon$. But this contradicts $(1)!$

$\Longleftarrow$
Suppose $\{ x_{n} \}\to a$, then $\forall \delta>0$ we can find $N_{1}\in \mathbb{N}$ such that 
$$
n>N_{1}\to d(x_{n},a)<\delta \quad 
$$
by hypothesis this implies that
$$
\forall \epsilon>0, \exists N_{2}\in  \mathbb{N} :n>N_{2}\to d(f(x_{n}),f(a)) < \epsilon
$$

Consider any $\epsilon>0,$ let $N^{*}=\text{max}\{ N_{1},N_{2} \}$

So for $n>N^{*},$ 
$$
d_{X}(x_{n},a)<\delta \to d_{Y}(f(x_{n}),f(a))<\epsilon
$$
which is the definition of continuity

## $f$ is continuous $\iff$ the [[Inverse Image]] of every open subset of $Y$ is an open subset of $X$

Let $(X,d_{X})$ and $(Y,d_{Y})$ be [[Metric Space]]s and let $f:X\to Y$.

$\Longrightarrow$
Assume $f$ is continuous on $X.$ Let $S_{Y}$ be any open subset of $Y$, and consider $a\in f^{-1}(S),$ so that $f(a)\in S_{Y}$

Since $S_{Y}$ is open in $Y$, there exists $\epsilon>0$ such that
$$
B_{\epsilon}(f(a)) \subseteq S_{Y}
$$
Given this $\epsilon,$ consider now the continuity of $f:$
$$
\exists \delta>0: d_{X}(x,a)<\delta \to d_{Y}(f(x),f(a)) <\epsilon
$$
Any $x\in B_{\delta}(a)$ thus maps through $f$ to elements
$$
f(x)\in B_{\epsilon}(f(a)) \subseteq S_{Y}
$$
making any such $x\in f^{-1}(S_{Y}).$ So $B_{\delta}(a)\subseteq f^{-1}(S_{Y})$

Thus any given $a\in f^{-1}(S_{Y}),\ B_{\delta}(a) \subseteq f^{-1}(S_{Y}),$ making $f^{-1}(S_{Y})$ open in $X.$

$\Longleftarrow$
Suppose the inverse image of every open subset of $Y$ is an open subset of $X$

By hypothesis, given $S_{Y}$ open in $Y,$ $f^{-1}(S_{Y})$ is open in $X.$ Consider any $a\in X$ and let $\epsilon>0$ be given.

Then $B_{\epsilon}(f(a))$ is an open subset of $Y.$ So, by hypothesis, $f^{-1}(B_{\epsilon}(f(a)))$ is open in $X.$ So:
$$
\exists \delta>0: B_{\delta}(a)\subseteq f^{-1}(B_{\epsilon}(f(a)))
$$

- note $a$ is certainly an element of $f^{-1}(B_{\epsilon}(f(a)))$ since $f(a)\in B_{\epsilon}(f(a))$

This means all elements of $B_{\delta}(a)$ are mapped by $f$ to $B_{\epsilon}(f(a))$, meaning that
$$d_{X}(x,a)<\delta\to d_{Y}(f(x),f(a))<\epsilon$$
which gives us the continuity of $f$

# Examples

Let $(X,d_{X})$ and $(Y,d_{Y})$ be metric spaces. Suppose $f:X\to Y$ is a function and that $f(x)=k$ for all $x\in X$, where $k\in Y$. Prove that $f$ is continuous.

We want to prove that for any $a\in X$ that is a limit point:
$$
\forall \epsilon>0, \exists \delta>0: d_{X}(x,a)<\delta \to d_{Y}(f(x),f(a))<\epsilon
$$
Consider that since $f(x)=k\ \forall x\in X$, then $f(a)=k$ as well.

Thus given any $\epsilon>0$, we see that 
$$
d_{Y}(f(x),f(a))= d_{Y}(k,k)=0 <\epsilon
$$
So the property is true given any positive $\delta$ at all
