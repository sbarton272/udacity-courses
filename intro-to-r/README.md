# Helpful Functions

https://www.rdocumentation.org/

## Functions

- sum(x, na.rm = TRUE)
- mad vs std, mad better balanced
```> mad(x)
[1] 185.32499999999998863
> sd(x)
[1] 144.48183276799889541
```
- `2*sqrt(6/n)` rule of thumb for large skew
- `fivenum` similar to quartiles
- `boxplot.stats`
- `scale` z score (mean norm, std norm)
- `bwplot(~weight | feed, data = chickwts)` compare box plots

## Plots

- stripchart (timeseries)
- pareto.chart
- plot
    - scatter by default
    - `type='l'` for line
    - subsequent `points` and `lines` calls can add things to existing plot

### ggplot2

- qplot
    - scatter by default
    - `geom="line"` for line plot
    - When done with categorical it does bar plot
    - `geom='boxplot'`
    - `interaction(var1, var2)` does pairings

## Libs

- qcc: pareto
- aplpack: stem/leaf
- e1071: kurtosis
- highcharter: nice charts
- shinydashboard: dashboards in shiny
- flexdashboard: dashboard layout
- dygraphs: nice time series charts
- lattice: xyplot
- tidyverse: texr file parse

## Stats

- *Chebychev’s Rule*: The proportion of observations within k standard deviations of the mean is at least 1 − 1/k2, i.e., at least 75%, 89%, and 94% of the data are within 2, 3, and 4 standard deviations of the mean, respectively.
- Confidence interval:
  - The standard way is called the Wald interval and is an approximation because it assumes the proportion
  - The Wilson interval is a bit more scientific and applies an upper bound
  - To calculate sample size you can either estimate the proportion or use an upper bound estimate with worst case proportion of 0.5
  - For small population sizes, the hypergeometric model can be used instead of the binomial (all of these above cases come from knowing a proportion comes from a binomial distribution)
- Good p-val definition:
  - The p-value, or observed significance level, of a hypothesis test is the probability when the null hypothesis is true of obtaining the observed value of the test statistic (such as pˆ) or values more extreme – meaning, in the direction of the alternative hypothesis
