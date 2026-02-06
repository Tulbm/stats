---
dg-publish: true
---
Let $(X,d)$ be a [[Metric Space]] and let $f:X\to X$ be a function. Any $\bar{x}\in X$ such that $f(\bar{x})=\bar{x}$ is called a fixed point of $f$
- can always be found by solving $x=f(x)$ for $x$ (although sometimes hard)


Let $(X,d)$ be a metric space and let $f:X\to X$. Suppose $\bar{x}$ is a fixed point of $f.$ 

If there exists $r>0$ such that for all $x$ satisfying $0<d(x,\bar{x})<r,$ $f^{\mathrm{o}n}(x)\to \bar{x}$ as $n\to \infty$, then $\bar{x}$ is an attractive fixed point of $f.$ The set $B_{r}(\bar{x})$ is then called a **basin of attraction** of $f$

If for any $r>0$, there exists $x\in B_{r}(\bar{x})$ such that $x\neq \bar{x}$ and some $n\in \mathbb{N}$ such that $f^{\mathrm{o}n}(x)\notin B_{r}(\bar{x}),$ then $\bar{x}$ is a repulsive fixed point of $f$
- there are points $x$ arbitrarily close to $\bar{x}$ so the sequence of iterates eventually moves away from $\bar{x}$

Let $(X,d)$ be a metric space and let $f:X\to X$. Suppose $\bar{x}$ is a fixed point of $f$.
- If $\lvert f'(\bar{x}) \rvert<1,\bar{x}$ is attractive
- If $\lvert f'(\bar{x}) \rvert>1,\bar{x}$ is repulsive


# Examples

## Fixed point
$f:\mathbb{R}\to \mathbb{R}$, $f(x)=  \frac{1}{3}x -2$

$x= f(x)\to x= \frac{1}{3}x -2\to \frac{2}{3}x = -2\to x= -3$

$f:\mathbb{R}\to \mathbb{R},$ $f(x)= \frac{1}{4}x^{2}$

$$
\begin{align}
x &  =f(x)  \\
x & = \frac{1}{4}x^{2}  \\
0 & = \frac{1}{4}x^{2}-x \\
0 & = x\left( \frac{1}{4}x -1 \right) \to x=0\text{ or  } x=4
\end{align}
$$
$f'(x)= \frac{1}{2}x$
We see that
- $f'(0)= \frac{1}{2}(0)=0<1$ $\to$ the fixed point $0$ is attractive
- $f'(4)= \frac{1}{2}4=2>1\to$ the fixed point $4$ is repulsive




$f:\mathbb{R}^{2}\to\mathbb{R}^{2}$ such that 
$$
f(x)=\begin{pmatrix}
1 & 3  \\
-1 & 2 
\end{pmatrix} \mathbf{x} +\begin{pmatrix}
2  \\
0
\end{pmatrix}
$$

$$
\begin{align}
\begin{pmatrix}
x_{1} \\
x_{2} 
\end{pmatrix} & = \begin{pmatrix}
1 & 3  \\
-1 & 2
\end{pmatrix} \begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix} + \begin{pmatrix}
2 \\
0
\end{pmatrix} \\
 & \to \begin{cases}
x_{1}=x_{1}+ 3x_{2}+2 \\
x_{2}=-x_{1}+ 2x_{2}
\end{cases} \\
 & \to \begin{cases}
-2=3x_{2} \to x_{2} = - \frac{2}{3} \\
x_{1}=x_{2}\to x_{1} = - \frac{2}{3}
\end{cases}
\end{align}
$$
So
$$
\begin{pmatrix}
x_{1} \\
x_{2} 
\end{pmatrix}= \begin{pmatrix}
- \frac{2}{3} \\
- \frac{2}{3}
\end{pmatrix} \text{ is a fixed point of } f
$$

## Basin of attraction

$f(x)=\frac{1}{4}x^{2}$, determine the largest possible basin of attraction for the fixed point $\bar{x}=0$

It is sufficient to find $x$ such that 
$$
|f(x)|<|x|
$$
Applying to the function:
$$
\left\lvert  \frac{1}{4}x^{2}  \right\rvert <\lvert x \rvert \to \frac{1}{4}x^{2} <\lvert x \rvert 
$$
Case $x>0:$
$$\begin{align}
\frac{1}{4}x^{2}  & <x \\
\frac{1}{4}x^{2} - x  & <0 \\
x\left(  \frac{1}{4}x -1 \right)  & <0
\end{align}
$$
roots on $x=0,x=4$ $\Longrightarrow$ True for $x\in(0,4)$

Case $x<0:$
$$\begin{align}
\frac{1}{4}x^{2}  & <-x \\
\frac{1}{4}x^{2} + x  & < 0 \\
x\left( \frac{1}{4}x + 1\right)  & <0
\end{align}
$$
True for $x\in(-4,0)$

($x=0$ is certainly in the basin of attraction of $\bar{x}=0$)

So considering all cases, the largest basin of attraction of $\bar{x}=0$ is $x\in(-4,4)$
