---
dg-publish: true
---
Axioms that formally define the ordering we use for the number line

$\mathbb{R}^{+}$ is a subset of $\mathbb{R}$ that satisfies:
1. If $x,y\in\mathbb{R}^{+}$ then $x+y\in\mathbb{R}^{+}$ and $xy\in R^{+}$
2. Given any $x\in\mathbb{R}$, exactly one of the following is true:
- $x$ is positive
- $-x$ is negative
- $x$ is zero

Let $\leq$ be a binary relation on $\mathbb{R}$

Then, for all $x,y\in\mathbb{R}$ we have that:
$$\begin{align}
 x\leq y  & \text{ if }y-x\in\mathbb{R}^{+}\cup \{ 0 \} \\
x<y  & \text{ if  } y-x\in\mathbb{R}^{+} \\
x \geq y  & \text{ if  } y-x\in \mathbb{R}^{-}\cup\{ 0 \}  \\
x > y  & \text{ if } y-x \in \mathbb{R}^{-}
\end{align}
$$
Given $x,y,z\in\mathbb{R}$, the relation $\leq$ satisfies three important properties:
- Reflexivity: $x\leq x$
- Anti-symmetry: If $x\leq y$ and $y\leq x$, then $x=y$
- Transitivity: If $x\leq y$ and $y\leq z$, then $x\leq z$
These properties show that $\mathbb{R}$ is a partially ordered set. Additionally, $\mathbb{R}$ is in fact a totally ordered set under $\leq$ by the property that for any given choice of $x$ and $y$ $\in \mathbb{R}$, one of these is true:
- $x<y$
- $x=y$
- $x>y$


# Examples

## 1
Given $R,S\in 2^{X}$, the power set, define $R\leq S$ if $R\subseteq S$ 
....


Now for a total ordering, we need that given any $R,S \in 2^{X}$ that exactly one of the following is true:
$$
R\subset S, R\supset S \text{ or } R=S
$$
This is not true, since we can find (for example) $R$ and $S$ that are disjoint

## 2
Consider $(X,\leq)$ where $X$ is the set of people in a family, and for $x,y\in X$ define $x\leq y$ if $y$ is a descendant of $x$

## 3 
Let $a,b,c,d,e \in \mathbb{R}$ Then:
- If $a>b$ and $c\geq d$ then $a+ c>b+d$
$a>b\to a-b\in \mathbb{R}^{+}$
$c\geq d\to c-d \in R^{+} \cup \{ 0 \}$
Consider the quantities
$$
m=a-b\in \mathbb{R}^{+}\quad \text{ and} \quad n=c-d\in \mathbb{R}^{+}\cup \{ 0 \}
$$
We consider $m+n$. We have two cases:
1. $n=0$. Then $m+n$ is the sum of a positive number and the additive identity, therefore $m+n=m\in\mathbb{R}^{+}$
2. $n\in \mathbb{R}^{+}$. Then $m+n$ is the sum of two positive numbers $\therefore$ $m+n\in \mathbb{R}^{+}$
$\therefore m+n>0$
$$
\begin{align}
\to a-b+(c-d)  & >0 \\
a+c-b-d & >0 \\
a+c -(b+d) & >0 
\end{align}
$$
Therefore by the basic definition, $a+c>b+d$

## If $a>b>0$ and $c\geq d>0$ then $ac>bd$

$a-b\in \mathbb{R}^{+}$
$c-d\in \mathbb{R}^{+}\cup \{ 0 \}$

$ac>bc$
$bc\geq bd$
$ac>bc\geq bd \to ac>bd$


## If $a>b$ and $c<0$ then $ac< bc$
$a-b\in \mathbb{R}^{+}$
$c\in \mathbb{R}^{-}$
$(a-b)c \in \mathbb{R}^{-}$

$ac-bc<0$
$ac<bc$

## $x\in \mathbb{R}, x>0 \to \frac{1}{x}>0$
Assume not. Then either:
1. $\frac{1}{x}=0$
$$
\begin{align} \\
\frac{1}{x} & =0 \\
\frac{1}{x}(x) & =0 \cdot x \\
1  & =0
\end{align}
$$
Contradiction (non sense)

2. $\frac{1}{x}<0$
$$
\begin{align}
\frac{1}{x} & <0 \\
\frac{1}{x} (x)  & < 0 \cdot x \\
1  & < 0
\end{align}
$$
Contradiction/non sense

Thus $\frac{1}{x}>0$

## $x\in \mathbb{R}, x<0 \to \frac{1}{x}<0$
Assume not. Then either:
1. $\frac{1}{x}=0$
$$
\begin{align} \\
\frac{1}{x} & =0 \\
\frac{1}{x}(x) & =0 \cdot x \\
1  & =0
\end{align}
$$
Contradiction (non sense)

2. $\frac{1}{x}>0$
$$
\begin{align}
\frac{1}{x} & >0 \\
\frac{1}{x} (x)  & < 0 \cdot x \quad \text{as }x \text{ is negative} \\
1  & < 0
\end{align}
$$
Contradiction/non sense

Thus $\frac{1}{x}<0$


## If $a$ and $b$ $\in \mathbb{R}^{*}$, have the same sign, with $a<b\to \frac{1}{a}> \frac{1}{b}$
(nonzero real numbers)

1. Suppose $a$ and $b$ are both positive and WLOG $a<b$
$$
\begin{align}
a & <b  \\
\frac{1}{a}(a)  & < \frac{1}{a}(b) \\
1 & < \frac{1}{a}(b) \\
1\left( \frac{1}{b} \right) & < \frac{1}{a} b\left( \frac{1}{b} \right) \\
\frac{1}{b} & < \frac{1}{a} \Longrightarrow \frac{1}{a}> \frac{1}{b}
\end{align}
$$
2. Suppose $a$ and $b$ are both negative with $a<b:$
$$
\begin{align}
a & <b \\
\frac{1}{a} a  & > \frac{1}{a} b \quad \text{flip as } \frac{1}{a} \text{ is negative} \\
1  & > \frac{1}{a}b \\
\frac{1}{b}(1) & < \frac{1}{a} b \left( \frac{1}{b} \right) \quad \text{ flip again}\\
\frac{1}{b} & < \frac{1}{a} \Longrightarrow \frac{1}{a}> \frac{1}{b}
\end{align}
$$
As in both cases the property holds, it is true.
## $a\in \mathbb{R}, b\in \mathbb{R}^{+}\to a<a+b$

$b\in \mathbb{R}^{+}\to$ 

$a+b - a = b \in \mathbb{R}+$
As $a+b-a \in \mathbb{R}^{+},$ we know $a+b-a>0$, thus $a+b>a\to a<a+b$

## $a\in \mathbb{R}^{+} \iff \frac{1}{a}\in \mathbb{R}^{+}$
$a \cdot \frac{1}{a}=1$

If $a\in \mathbb{R}^{+}\to a>0$
As $1>0$, $\frac{1}{a} \in \mathbb{R}^{+}$

## $\frac{1}{2}<1$

Assume $1>0$.

Then $1+ 1> 1+ 0 \to 2>1$

If $a>b$ and $c>0$ then $ac >bc$. So:
$2 \cdot \frac{1}{2} > 1\cdot \frac{1}{2}$

$1> \frac{1}{2}\to \frac{1}{2}<1$


## $a\geq 1 \to a^{2}\geq a$

$a-1 \in \mathbb{R}^{+}\cup \{  0 \}$

$a \in \mathbb{R}^{+ }$

Then $(a-1)a \in \mathbb{R}^{+} \cup \{  0 \}$
$a^{2}-a \geq 0\to a^{2} \geq a$

## $a\in \mathbb{R}^{+}$, $a<1 \to a^{2}<a$

$a>0$
$a-1<0$

$\mathbb{R}^{+}\cdot \mathbb{R}^{-}=\mathbb{R}^{-}$

$a(a-1)<0$
$a^{2}-a<0$
$a^{2}<a$

## $a\leq c \to \frac{a}{b}\leq \frac{c}{b}$
