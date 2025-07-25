---
{"dg-publish":true,"dg-path":"STATS/Math Stats 1/Random Variables.md","permalink":"/stats/math-stats-1/random-variables/","created":"2024-10-03T16:59:53.445-04:00","updated":"2025-07-07T18:02:31.436-04:00"}
---

A random variable X is a function that maps the sample space $S$ to the real line; 
- for each element $w \in S, X(w)\in R$
(workable values are numbers)

Capital letters will usually be the random variable, and lowercase their realized value

# Discrete Random Variables

| $w\in S$ | HHH           | HHT           | HTH           | ... |
| -------- | ------------- | ------------- | ------------- | --- |
| $P(w)$   | $\frac{1}{8}$ | $\frac{1}{8}$ | $\frac{1}{8}$ | ... |
| $X(w)$   | $3$           | $2$           | $2$           | ... |
Each value of $X$ has a certain chance of happening

| $X$      | 0             | 1             | 2             | 3             |
| -------- | ------------- | ------------- | ------------- | ------------- |
| $P(X=x)$ | $\frac{1}{8}$ | $\frac{3}{8}$ | $\frac{3}{8}$ | $\frac{1}{8}$ |
For every $x$ outside of the domain $X$, $P(X=x)=0$

# Continuous Random Variables


# stats1

a random variables is a quantitative variable whose observed value is partly due to chance
	- random variable x realized value
		- random variable = X, Y, Z etc (theoretical quantity)
		- realized value/realization of the random variable(x)
		- P(X = x)
			- P(X = 5%) for example
	- tossing coins, sampling randomly
	- sometimes we don't know the value of the variable until the experiment, but we may know characteristics of its distribution
- random variables can be either discrete or continuous
	- discrete = have a countable set of possible units
		- no in-between the values
			- yes or no, how many eggs broken
		- (n+1) makes sense
		- ![](https://i.imgur.com/f9pDzz4.png)
	- continuous = have an infinite number of possible values
		- [[Continuous Random Variables\|Continuous Random Variables]]
		- all values in an interval
			- weight, temperature, time
		- needs calculus
		- ![](https://i.imgur.com/y13h4uZ.png)
