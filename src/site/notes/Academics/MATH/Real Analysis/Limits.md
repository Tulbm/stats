---
dg-publish: true
---
Let $f$ be a function, and let $a,L$ be real constants. Suppose that 
$$
\forall \epsilon>0, \exists \delta >0 : 0<|x-a|<\delta\to |f(x)-L|<\epsilon
$$
- we say that $\lim_{ x\to a }f(x)=L$

For this definition, we need:
- a defined [[Metric Space]] for input and outputs, which do not need to be equal
- The point $a$ must be a [[Limit point]] 

A more formal definition:

Let $(X,d_{X})$ and $Y,d_{Y}$ be metric spaces. Let $S\subseteq X$ and $f:S\to Y$ be a function. If $a$ is a limit point of $S,$ we say that the $\lim_{ x \to a }f(x)=L$ if 
$$
\forall \epsilon>0,\exists\delta>0: x\in  S \text{ and }0<d_{X}(x,a)<\delta \to d_{Y}(f(x),L)<\epsilon
$$
- $0<d_{X}$ is important, as we only let get close to $a$, not equal to $a$

# Theorems

## If the limit exists, $\lim_{ x \to a }f(x)$ is unique

Suppose that both 
$$
\lim_{ x \to a } f(x)=L\quad \text{ and }\quad \lim_{ x \to a } f(x)= M
$$
Consider any given $\epsilon>0,$ we may define $\epsilon_{1}= \frac{1}{2}\epsilon.$

Since $\lim_{ x \to a }f(x)=L$ then $\exists\delta$ so that $d_{x}(x,a)<\delta\to$ $d_{y}(f(x),L)<\epsilon_{1}$
And since $\lim_{ x \to a }f(x)=M$, there also $\exists \delta_{2}$ so that $d_{x}(x,a)<\delta_{2}\to d_{y}(f(x),M)<\epsilon_{1}$

So for $\delta= \text{min}\{ \delta_{1},\delta_{2} \},$ we have that if $0<d_{x}(x,a)<\delta$ then:
- $d_{y}(f(x),L)<\epsilon_{1}\Longrightarrow d_{y}(f(x),L)< \frac{\epsilon}{2}$
- $d_{y}(f(x),M)<\epsilon_{1}\Longrightarrow d_{y}(f(x),M)< \frac{\epsilon}{2}$

We wish to show that $L=M$, so consider
$$
\begin{align}
d_{y}(L,M)  & \leq d_{y}(L,f(x)) + d_{y}(f(x),M) \\
 & < \frac{\epsilon}{2} + \frac{\epsilon}{2} \\
 & = \epsilon
\end{align}
$$
So $d_{y}(L,M)<\epsilon$ for all $\epsilon>0$. The only way this is true is if $L=M$

## $\lim_{ x \to a }f(x)=L\iff \forall \{ x_{n} \}\in X$ of distinct points, if $\{ x_{n} \}$ converges to $a$, then $\{ f(x_{n}) \}$ converges to $L$


# Examples
$\lim_{ x \to 1 }4x-3=1$

Let $\epsilon>0$ be given, and then define $\delta = \frac{\epsilon}{4}$. Then consider that if
$$
\begin{align}
0  < |x-1| &  < \delta \\
 |x-1| & < \frac{\epsilon}{4} \\
 4|x-1|  & < \epsilon \\
|4x-4| &< \epsilon \\
|(4x-3)-1| & <\epsilon
\end{align}
$$