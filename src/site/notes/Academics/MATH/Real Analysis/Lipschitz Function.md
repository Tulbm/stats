---
dg-publish: true
---
Let $X$ and $Y$ be [[Metric Space]]s and let $f:X\to Y$ be a function. Let $c$ be a positive real number. If
$$
d_{Y}(f(x),f(y))\leq cd_{X}(x,y) \ \forall x,y \in  X
$$
then $f$ is a Lipschitz function with Lipschitz constant $c$
- caps how fast a function can grow


If absolute value is used as out metric we obtain:
$$
\begin{align}
\lvert f(x)-f(y) \rvert   & \leq c\lvert x-y \rvert  \\
 \left\lvert  \frac{f(x)-f(y)}{x-y}  \right\rvert & \leq  c
\end{align}
$$
- the slope of $f$ is $\leq c$ 

# Theorems

# Examples

## $f(x)=ax+ b$
$f:\mathbb{R}\to \mathbb{R}$

The slope of $f(x)=ax+ b$ is $a$, which is bounded above by $|a|.$
Thus $f$ is Lipschitz with Lipschitz constant $c=\lvert a \rvert$

With definition:
$$
\begin{align}
\lvert f(x)-f(y) \rvert  & = \lvert (ax+ b)- (ay+ b) \rvert  \\
 & = \lvert ax-ay \rvert  \\
 & = \lvert a \rvert \lvert x-y \rvert  \\
d_{Y}(f(x),f(y))  & =\lvert a \rvert d_{X}(x,y) \\
d_{Y}(f(x),f(y))  & \leq c d_{X}(x,y)
\end{align}
$$

## $f(x)=\sqrt{ x }$
not Lipschitz on $(0,\infty)$
Lipschitz on $[k,\infty)$

Looking at the magnitude of the slope
$$\begin{align}
\lvert f(x)-f(y) \rvert  & = \lvert \sqrt{ x }-\sqrt{ y } \rvert  \\
 & = \left\lvert  \frac{\sqrt{ x }-\sqrt{ y }}{(\sqrt{ x }-\sqrt{ y })(\sqrt{ x }+\sqrt{ y })}  \right\rvert  \\
 & = \frac{1}{\sqrt{ x }+\sqrt{ y }}
\end{align}
$$
The biggest value for $\frac{1}{\sqrt{ x }+\sqrt{ y }}$ occurs when $x=y=c$. When $0$ is included this is undefined, and converges to $\infty.$

When the function is bounded between $[k,\infty)$, it occurs at $x=y=k$. So we have a bound $c$ = $\frac{1}{2\sqrt{ k }}$

Note that for $f(x)=\sqrt{ x }$ then $f'(x)=\frac{1}{2\sqrt{ x }}$

