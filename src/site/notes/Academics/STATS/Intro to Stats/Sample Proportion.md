---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Sample Proportion.md","permalink":"/stats/intro-to-stats/sample-proportion/","created":"2024-04-01T13:34:06.182-04:00","updated":"2025-07-07T17:21:02.522-04:00"}
---

- sample proportion ( $\hat{p}$ )  
	- estimates the population proportion $p$
		- proportion of the population that would do x
	- single point estimate of $p$ 
		- don't know how close to $p$ $\hat{p}$ is, as p is unknown
		- we use mathematical arguments based on the [[Academics/STATS/Intro to Stats/Sampling Distributions\|Sampling Distributions]] of $\hat{p}$ to make statements
			- like margin of error, range
			- 0.43 accurate within 0.03 19 times out of 20
				- (0.40, 0.46) = 95% confidence interval (CI) for $p$
- for large sample sizes, $\hat{p}$ distribution is approximately [[Academics/STATS/Intro to Stats/Normal Distribution\|normal]]
	- normal approximation is best when n is large and $p = 0.5$
	- reasonable with 
		- $n \hat{p}\geq 15\text{ and }n(1-\hat{p})\geq 15$
		- n large, p cant be close to 0 or 1
- $\hat{p}$ estimates $p$
	- [[Discrete Random Variables\|binomial random variable]] $\hat{p}=\frac{X}{n}$
		- $E(\hat{p})=p, Var(\hat{p})=\frac{p(1-p)}{n}$
		- $SE(\hat{p})=\sqrt{ \frac{\hat{p}(1-\hat{p})}{n} }$ as we can't use statistic $p$
	-  number of individual in the sample with the characteristic of interest / total number of individuals in the sample
	- for [[Academics/STATS/Intro to Stats/Central Limit Theorem\|large sample sizes]] $\hat{p}$ is approximately normal

Suppose $X \sim Bin(n,p)$. Let $Y=\frac{X}{n}$ represent the sample proportion of successes

Mean$$\begin{align}
  E(Y)=  E\left( \frac{X}{n} \right) & =\frac{1}{n}E(X)=\frac{1}{n}np=p
\end{align}
$$Variance $$\begin{align}
Var(Y)= Var\left( \frac{X}{n} \right)   & =\frac{1}{n^2}Var(X) \\
 & =\frac{1}{n^2}np(1-p) \\
 & =\frac{p(1-p)}{n}=\frac{pq}{n}
\end{align}
$$

