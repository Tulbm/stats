---
{"dg-publish":true,"dg-path":"STATS/Intro to Stats/quantile-quantile plots (QQ plot).md","permalink":"/stats/intro-to-stats/quantile-quantile-plots-qq-plot/","created":"2024-03-23T03:27:42.243-04:00","updated":"2025-07-07T17:21:02.443-04:00"}
---

- plots the observed sample values against quantiles of a theoretical distribution
	- if the data actually comes from that type of distribution, then points will fall roughly on a straight line
- normal quantile-quantile plot (normal QQ plot)
	- checking the normality assumption
		- data roughly on the line $\rightarrow$ data is approximately normally distributed
		- ![](https://i.imgur.com/cONHLI0.png)
			- normally compare against the standard normal distribution (see middle is 0)
			- if skewed = skewness is on the opposite side of the original distribution's skewness
- different distributions
	- right-skewed
		- normally its a hard cap on the left side (think logs with 0)
			- normal would have it going outliers->middle->outliers
			- skewness makes it start at the "middle"
		- ![](https://i.imgur.com/aciEDub.png)
	- left-skewed
		- hard cap on the right side
			- refer to right
		- ![](https://i.imgur.com/PfFRLhk.png)
	- under-dispersed
		- less outliers
		- everything tends to the z-score 0
			- when the percentile that the outliers normally are starts, everything is still close to the mean
		- ![](https://i.imgur.com/qEy1Crf.png)
	- over-dispersed
		- more outliers
			- the percentile where it should be getting close to the mean still has outliers (more concentration)
