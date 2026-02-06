---
dg-publish: true
---

$$
\left|\sum_{i=1}^{n} u_{i}v_{i}\right| \leq \sqrt{ \sum_{i=1}^{n} u_{i}^{2} } \sqrt{ \sum_{i=1}^{n} v_{i}^{2} }
$$

Sometimes stated in terms of norms and inner products
$$\begin{align}
|(u_{i}v_{i})|  & \leq | | u_{i} | | \ || v_{i}| | \\
 & \text{ or}  \\
(u_{i}v_{i})^{2}  & \leq || u_{i}| |^{2} \ | | v_{i}| | ^{2}
\end{align}
$$
In integral form:
$$
\left|\int_a^bf(x)g(x)dx\right|\leq\left(\int_a^bf(x)^2dx\right)^{1/2}\left(\int_a^bg(x)^2dx\right)^{1/2}
$$
# Proof
We have two cases. First, if either $\mathbf{u}$ or $\mathbf{v}$ is a vectors of zeros:
$$
LS=0\quad RS=0
$$
And the case where both $\mathbf{u}$ and $\mathbf{v}$ are non-zero. Consider the expression
$$
\sum_{i=1}^{n} (v_{i}-\lambda u_{i})^{2}
$$
Since this is a sum of squares, the expression is non-negative, and zero only when $v=\lambda u$
$$\begin{align}
0  & \leq \sum_{i}^{n} (v_{i}-\lambda u_{i})^{2} \\
  & \leq \sum _{i=1}^{n} (v_{i}^{2} - 2\lambda u_{i}v_{i} + \lambda^{2}u_{i}^{2} ) \\
 & \leq \sum_{i=1}^{n}v_{i}^{2} - 2 \lambda \sum_{i=1}^{n} u_{i}v_{i} + \lambda^{2} \sum u_{i}^{2} \\
\end{align}
$$
This statement will hold true no matter the value of $\lambda$, so out goal is to pick a quantity $\lambda$ that gives us the inequality we are looking for.
$$
\lambda = \frac{\sum u_{i}v_{i}}{\sum u_{i}^{2}}
$$
Then:
$$
\begin{align}
0  & \leq \sum_{i=1}^{n} v_{i}^{2} -2  \frac{\sum u_{i}v_{i}}{\sum u_{i}^{2}} \sum_{i}^{n} u_{i}v_{i} + \left(  \frac{\sum u_{i}v_{i}}{\sum u_{i}^{2}} \right)^{2} \sum_{i=1}^{n} u_{i}^{2} \\
0 & \leq \sum_{i=1}^{n} v_{i}^{2} - 2  \frac{\left( \sum u_{i}v_{i} \right)^{2}}{\sum u_{i}^{2}} +  \frac{\left( \sum u_{i}v_{i} \right)^{2}}{\sum u_{i}^{2}} \\
0 &  \leq \sum_{i=1}^{n } v_{i}^{2} - \frac{\left( \sum u_{i}v_{i} \right)^{2}}{\sum u_{i}^{2}} \\
\frac{\left( \sum u_{i}v_{i} \right)^{2}}{\sum u_{i}^{2}} & \leq \sum_{i=1}^n v_{i}^{2} \\
\left( \sum_{i=1}^n u_{i}v_{i} \right)^{2}  & \leq \sum_{i=1}^n u_{i}^{2} \sum_{i=1}^nv_{i}^{2} \\
\sum_{i=1}^n u_{i}v_{i}  & \leq \sqrt{ \sum_{i=1}^n  u_{i}^{2} } \sqrt{ \sum_{i=1}^n  v_{i}^{2} }
\end{align}
$$


