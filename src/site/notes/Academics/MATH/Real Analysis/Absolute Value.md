---
dg-publish: true
---
The absolute value of $x$, denoted by $|x|$ is defined to be:
$$
|x|=\begin{cases}
x & \text{if } x\geq 0 \\
-x  &  \text{if } x<0
\end{cases}
$$

# Properties
1. $|x|\geq 0$
2. $|x| = \text{max }(x,-x)$
3. $|x|=|-x|$
4. $|xy|=|x| |y|$
5. $|x+y|\leq |x|+|y|$
6. $|x-y|\geq |x|-|y|$ and $|x-y| \geq |y|-|x|$. 
   Thus $|x-y| \geq | |x| -|y| |$
7. Supposing $r>0,\ |x-y|<r\iff x-r<y<x+r$
- Corollary: $|x-y|>r\to y>x+r$ or $y<x-r$

# Proofs

## $|x+y|\leq |x| +|y|$

We have that for any $x,y\in\mathbb{R}$:
$$
\begin{align}
-|x|\leq  x \leq |x|\quad (1)\\
-|y|\leq  y \leq |y|\quad (2)
\end{align}
$$
Adding $(1)$ and $(2)$:
$$
\begin{align}
-|x|-|y|  & \leq x+y \leq |x| +|y| \\
-(|x|+|y|) & \leq x+ y\leq |x|+ |y| \\
0-(|x|+|y|) & \leq 0+ x+ y\leq 0+|x|+ |y| \\
0-(|x|+|y|) & \leq x+ y\leq 0+|x|+ |y| \\
|0-(x+y)| & < |x| +|y| \quad \text{ by } 7. \\
|-(x+y)| & < |x| +|y| \\
|x+y| & < |x| +|y|
\end{align}
$$

## $|a+b+c| \leq |a| + |b| + |c|$
$|(a+b)+c|\leq |a+ b| + |c|$
And $|a+b|\leq |a| + |b|$
so $|(a+b)+c|\leq |a+ b| + |c| \leq |a| + |b| + |c|$
