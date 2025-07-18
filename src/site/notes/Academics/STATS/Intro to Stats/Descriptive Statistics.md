---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/Descriptive Statistics.md","permalink":"/stats/intro-to-stats/descriptive-statistics/","created":"2024-01-17T13:34:35.650-05:00","updated":"2025-07-07T17:21:02.302-04:00"}
---

## Categorical Variables
- categorical variable
	- a variable that falls into one of two or more categories
		- categories like blood type, each person only falls in one category
	- frequency = number of occurences
	- relative frequency = proportion/percentage
	- example
		- roadrage accidents in germany
		- ![](https://i.imgur.com/Y0GFtAF.png)
			- pie chart = good for seeing how big the bigger is, bad when there are multiple tiny slices
- ways of organizing graphs with categorical variables
	- ordinal
		- ordered from most frequent category to less frequent 
	- nominal
		- random order?, cause its not alphabetical
	- side-by-side bar charts
		- ![](https://i.imgur.com/THOaJbr.png)
	- stacked bar charts
		- ![](https://i.imgur.com/xD4eDYb.png)
## Quantitative Variables
- quantitative variables
	- a numeric variable that represents a measurable quantity
	- we plot the values of the variables and how often these values occur
		- days after receiving virus that guinea pigs died
		- ![](https://i.imgur.com/xc2EwZo.png)
- can be illustrated in a variety of ways
	- histograms
		- ![](https://i.imgur.com/xc2EwZo.png)
	- box plots
	- dot plots
	- scatterplots
		- when we have 2+ quantitive variables
		- analyzed using simple ___ regression and correlation
		- ![](https://i.imgur.com/ZL3bL0L.png)
	- time series plots
		- used to visualize observations that occur in time order
		- ![](https://i.imgur.com/iNoC9BA.png)
- important considerations when analyzing the data
	- where the center of the distribution is located
		- mean, median
	- how much variability there is
		- variance, standard deviation
	- are there any outliers?
		- extreme values
	- the shape of the distribution
		- is it skewed?
- distribution shapes
	- symmetric distributions
		- ![](https://i.imgur.com/aySnmcA.png)
	- bimodal distributions
	- skewed distributions
		- to the left
			- like grades, lot of people ~90
			- ![](https://i.imgur.com/WHDP20X.png)
		- to the right/positively skewed
			- common with time from something
			- can always stretch to the right, but bounded at 0
			- ![](https://i.imgur.com/bhKBB1A.png)
			- 
## Numerical Measures
- assume that the data is from a sample, and does not represent the entire population

## Measures of Central Tendency
- Measures of Central Tendency
	- mean
		- more impacted by outliers/extreme values
		- represented by $\bar x$ = sample mean
			- estimates population mean (mu) $\mu$
		- $$\bar x = \frac{\sum_{i=1}^nx_i}{n}$$
	- median
		- splits the observation in the middle
			- ![](https://i.imgur.com/ZrJuCen.png)
		- the value that falls in the middle when the data are ordered from smallest to largest
			- if n is odd, the median is the middle value
			- if n is even, the median is the average of the two middle values
	- mode
		- the most frequently occurring observation
		- not used very often
	- trimmed mean
	- weighted mean
	- midrange
	- harmonic mean
	- geometric mean
## Measures of variability
- Measures of variability
	- range
		- maximum - minimum
		- or both max and min
			- R gives the values themselves
	- the best measures of variability are based on deviations from the mean
		- for any data set, the sum of the deviations (values - mean) = 0
		- Mean Absolute Deviation (MAD)
			- the average distance from the mean
				- not very useful
				- $$MAD = \frac{\sum|x_i-x|}{n}$$
			- usually just uses the squared distance from the mean (sample variance)
		- $Var(X)$ = $\sigma
{ #2}
$
			- $Var(X) = E[(X-\upmu )^2]$
				- $E[(X-\upmu )^2] = E(X^2) - [E(X)]^2$
				- average squared distance from the true mean
					- something distant = exaggerated effect
			- $Var(X)=\frac{\sum(x_i-\mu)^2}{n}$ 
		- $s^2$ (sample variance) estimates $\sigma
{ #2}
$ (population variance)
			- $s^2 = \frac{\sum(x_i-\bar x)^2}{n-1}$ 
			- n-1 instead of n
				- sample mean makes the number the smallest possible value, but true mean could be anywhere, so just have the -1 to have a better estimation
		- sample standard deviation
			- square root of the sample variance
			- s always $\geq$ MAD
			- $\bar x$ = sample mean, estimation of population mean
			- $$s = \sqrt {s^2}=\sqrt{\frac{\sum (x_i-\bar x)^2}{n-1}}$$
				- $s^2$ estimates $\sigma
{ #2}
$ (population variance)
			- empirical rule
				- for mount shaped distributions:
					- Approximately 68% of the observations lie within 1 standard deviation of the mean
					- Approximately 95% of the observations lie within 2 standard deviations of the mean
					- All or almost all of the observations lie within 3 standard deviations of the mean
					- ![](https://i.imgur.com/XBKmEEd.png)
		- Z-score
			- the sample z-score for the ith observation 
				- zi = (xi - xbar)/s
				- measures how many standard deviations the observation is above or below the mean
				- ![](https://i.imgur.com/EwMSFcg.png)
			- average z score = 0
				- theres negatives and positives
			- sd of z-scores = 1
			- rephrasing empirical rule
				- ~68% of z-scores lie between -1 and 1
				- ~95% of z-scores lie between -2 and 2
				- ~almost all z-scores lie between -3 and 3
[[Academics/STATS/Intro to Stats/Percentiles\|Percentiles]]
# Linear Transformations
- x* = a + bx
- some measures change with the transformation (F to C)
	- new mean = a + b * original mean
		- times 4 or -4 = increases distance between the mean by 4 times
		- times 1 or -1 doesnt change sd
	- new median = a + b * original median
- additive constant (a) does not affect the measures of variability
	- new sd = |b| x original sd
	- new variance = b^2 x original variance
	- new IQR = |b| x original IQR
	- ![](https://i.imgur.com/mCTBhp1.png)
- not all transformations
	- log, sqrt are calculated differently, these are just simple bc its + and *