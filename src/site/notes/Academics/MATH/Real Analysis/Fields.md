---
dg-publish: true
---
A set $F$, coupled with two operations which satisfy the field axioms, is 

# Useful definitions
For $x,y\in\mathbb{R}$ we define the subtraction operation as:
$$
x-y=x+(-y)
$$
For $x,y\in\mathbb{R}$ we define the division operation as:
$$
x\div y=x\left( \frac{1}{y} \right)
$$
which as convention we may write as $\frac{x}{y}$
# Field Axioms
Let $+$ and $\times$ be binary operations on $\mathcal{R}$. Supposing $x,y,z\in\mathbb{R}$, these operations are:
- commutative, so that $x+y=y+x$
- associative, so that $(x+y)+z=x+(y+z)$ and $(x\times y)\times z=x\times(y\times z)$

Additive Identity
- There exists a real number 0 such that $x+0=x$ for all $x\in \mathbb{R}$
Multiplicative Identity
- There exists a real number 1 such that $x\times1=x$ for all $x\in\mathbb{R}$
Additive Inverse
- For every $x\in\mathbb{R}$ there exists an element $(-x)\in\mathbb{R}$ such that $x+(-x)=0$
Multiplicative Inverse
- For every nonzero $x\in\mathbb{R}$ there exists an element $\left( \frac{1}{x} \right)$ such that $x\times\left( \frac{1}{x} \right)=1$
Distributive Property
- Multiplication distributes over addition. That is, for $x,y,z\in\mathbb{R}$ we have that $x(y+z)=xy+xz$

# Proofs
Examples/Related

## 0 is the unique additive identity for $\mathbb{R}$

Suppose both $a$ and $b$ are additive identities.
Thus for any $x\in\mathbb{R}$ we must have that 
$$
\begin{align}
x+a=x &  & x+b=x
\end{align}
$$
Therefore from the two equations we have that
$$
x+a=x+b
$$
Then we have that
$$\begin{align}
(-x)+x+a & = (-x)+x+b  & (\text{Additive Inverse})\\
0+a & =0+b   & \text{(Additive Identities)}\\
a & =b
\end{align}
$$

Alternative proof:
Suppose $\exists\ a$ such that  $x+a=x$ for $x\in\mathbb{R}$
Then 
$$
\begin{align}
a & =a+0  \\
 & =a+x+(-x) \\
 & = x+(-x) = 0
\end{align}
$$

## $-0=0$
By definition of the additive inverse, $0+(-0)=0$ 
and as $0$ is the additive identity we have $0+(-0)=(-0)$
As both left sides are equal, we have that $0=-0$

## $\forall x\in\mathbb{R},\ -(-x)=x$

$$\begin{align}
-(-x)+(-x) &=0 \\
-(-x)+(-x)+x & =0+x \\
-(-x)+0   & =x \\
-(-x) & =x
\end{align}
$$

$$
\begin{align}
-(-x) & = -(-x)+0 \\
 & =-(-x)+(-x)+x \\
 & =0+x \\
-(-x) & =x
\end{align}
$$

# $(-1)x=-x$
$x\in\mathbb{R}$

$$
\begin{align}
(-1)x & = (-1)x+0 \\
 & = (-1)x +x+(-x) \\
 & =(-1)x+1\cdot x + (-x) \\
 & =x(-1+1)+(-x) \\
 & =x(0)+(-x) \\
 & =0 +(-x) \\
 & =(-x)
\end{align}
$$

# $0x=0$

$$
\begin{align}
 0\cdot x & = x(0+0) =0x+0x \\
\end{align}
$$
$$
\begin{align}
0 & =-(0x)+0x \\
 & =-(0x)+0x+0x \quad \text{ from above} \\
 & =0+0x \\
 & =0x
\end{align}
$$

# $x=(x^{-1})^{-1}$

$$
\begin{align}
x & = x \cdot 1 \\
 & = x \cdot x^{-1} \cdot (x^{-1})^{-1} \\
 & = 1 \cdot (x^{-1})^{-1} \\
 & =(x^{-1})^{-1}
\end{align}
$$

# $x^{-1}$ is unique

Assume theres $a$ and $b$ that are the multiplicative inverse

So we know that:
- $x\cdot a=1$
- $x \cdot b=1$

Then
$$\begin{align}
x\cdot a  & = x\cdot b \\
x^{-1}\cdot x \cdot a & = x^{-1}\cdot x \cdot b \\
1 \cdot a & = 1 \cdot b  \\
a & =b
\end{align}
$$

