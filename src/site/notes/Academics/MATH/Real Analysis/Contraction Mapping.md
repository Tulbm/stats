---
dg-publish: true
---
Let $(X,d_{X})$ be a [[Metric Space]] and suppose that $f:X\to X$. $f$ is called a contraction mapping if $f$ is a [[Lipschitz Function]] with Lipschitz constant $c$ such that $c<1$
$$
d(f(x),f(y)) \leq c\ d(x,y), \quad \text{where }c\in  [0,1)
$$
Contraction mappings can be thought of as functions that bring points closer together (shrinking)

Contraction mappings are functions that always possess exactly one [[Fixed point]] that is also attractive



# Examples

Let $f:\mathbb{R} \to \mathbb{R}$ such that $f(x)=kx^{2},$ where $k$ is a real constant. Find $k$ such that $f$ is contractive on $S=[0,1]\subset \mathbb{R}$

Consider that 
$$
\begin{align}
d(f(x),f(y)) & = \lvert f(x)-f(y) \rvert  \\
 & = \lvert kx^{2}-ky^{2} \rvert  \\
 & = \lvert k \rvert \lvert  x^{2}-y^{2} \rvert  \\
 & =\lvert k \rvert  \lvert  x-y \rvert \lvert x+ y \rvert \\  
\end{align}
$$
Now for $S=[0,1]$ we have $\lvert x+y \rvert$ is no bigger than 2. So
$$
d(f(x),f(y)) = \lvert k \rvert \lvert x-y \rvert \lvert x+ y \rvert \leq 2 \lvert  k \rvert  \lvert x-y \rvert 
$$
This creates a suitable contraction factor as long as $\lvert k \rvert< \frac{1}{2}$



Consider $f:\mathbb{R}\to \mathbb{R}$ such that $f(x)= \frac{1}{3}x - \frac{1}{10}.$

a) Verify that $f$ is a contraction on $(\mathbb{R},\lvert \cdot \rvert)$
We must show $\lvert f(x)-f(y) \rvert\leq c\lvert x-y \rvert,$ where $c\in [0,1)$

Here, LS =
$$
\left\lvert  \left( \frac{1}{3}x- \frac{1}{10} \right)- \left( \frac{1}{3}y - \frac{1}{10}\right)  \right\rvert = \left\lvert  \frac{1}{3}x - \frac{1}{3}y  \right\rvert = \frac{1}{3} \lvert x-y \rvert  
$$
Thus $\lvert f(x)-f(y) \rvert\leq \frac{1}{3}\lvert x-y \rvert$

b) Find the fixed point of $f:$ 
$$
x=f(x)\to x=\frac{1}{3}x- \frac{1}{10} \to \frac{2}{3}x = - \frac{1}{10}\to x = - \frac{3}{20}
$$
c) Show that the fixed point is attractive
$$
f'(x)= \frac{1}{3}\to f'\left( - \frac{3}{20} \right)= \frac{1}{3}<1
$$
$\therefore$ the fixed point is attractive ([[Fixed point]] theorem)


