---
dg-publish: true
---
Closely-related notion to [[Continuity]], but defined for functions, instead of single points.

Let $X$ and $Y$ be metric spaces, let $S\subseteq X,$ and let $f:X\to Y$ be a function. $f$ is said to be **uniformly continuous** if
$$
\forall \epsilon>0 \exists \delta>0 : d_{X}(a,b)<\delta \ \forall a,b\in  S \to d_{Y}(f(a),f(b))<\epsilon
$$

# Theorems

## $f$ is a [[Lipschitz Function]] $\to f$ is uniformly continuous

Let $(X,d_{X})$ and $(Y,d_{Y})$ be metric spaces with $f:X\to Y$. Prove that if $f$ is Lipschitz on $S\subset X$, then $f$ must be uniformly continuous on $S$

If $f$ is Lipschitz, then
$$
d_{Y}(f(x),f(y))\leq cd_{X}(x,y) \ \forall x,y \in  S
$$
Let $\epsilon>0$ be given, and choose any $\delta \leq \epsilon/c$, $c\in \mathbb{R}^{+}$

Then if $d_{X}(x,y)<\delta$ then by $f$ being Lipschitz we have
$$
\begin{align}
d_{Y}(f(x),f(y))  & \leq cd_{X}(x,y)  \\
 & < c\delta \\
 & \leq c\left( \frac{\epsilon}{c} \right)  \\
 & =\epsilon
\end{align}
$$
Thus, $d_{X}(x,y)<\delta$ implies $d_{Y}(f(x),f(y))<\epsilon$ for any $x,y\in S$.

$\therefore f$ is uniformly continuous




# Examples

$f(x)= \frac{1}{x}$ is continuous at every point of $(0,\infty).$ But it is not uniformly continuous on $(0,\infty)$

Pick $\epsilon = \frac{1}{2},$ then if we try to find a $\delta$ for the distance between $a,b$, that makes $d(f(a),f(b))< \frac{1}{2}.$ But no single $\delta$ can work for all choices of $a$ and $b$
- Though $f(x)= \frac{1}{x}$ is uniformly continuous on any interval $[k,\infty]$ where $k>0$


$f(x)=\sqrt{ x }$ is a uniformly continuous function on $[0,\infty)$
- show that if $|x-y|<\delta\ \forall x,y\in[0,\infty)$ that $|\sqrt{ x }-\sqrt{ y }|<\epsilon$

Consider that
$$
\begin{align}
\lvert \sqrt{ x }-\sqrt{ y } \rvert ^{2}  & = \lvert \sqrt{ x }-\sqrt{ y } \rvert \lvert \sqrt{ x }-\sqrt{ y } \rvert  \\
 & \leq \lvert \sqrt{ x }-\sqrt{ y } \rvert  \lvert \sqrt{ x }+ \sqrt{ y } \rvert  \\
 & = |x-y| 
\end{align}
$$
Now given $\epsilon>0,$ choose $\delta\leq \epsilon^{2}.$

Then if $\lvert x-y \rvert< \delta$ then
$$
\begin{align}
\lvert \sqrt{ x }-\sqrt{ y } \rvert ^{2}  & \leq \lvert x-y \rvert <\delta \leq \epsilon^{2} \\
\lvert \sqrt{ x }-\sqrt{ y } \rvert ^{2} & < \epsilon^{2}
\end{align}
$$
Both sides are positive/non-negative so we may take the square root of both sides:
$$
\lvert \sqrt{ x }-\sqrt{ y } \rvert < \epsilon
$$


