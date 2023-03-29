---
title: "The statistical hypothesis testing framework"
date: 2023-02-27T10:53:14+11:00
Description: "Post"
Tags: ['reproducibility','statistics']
Categories: []
DisableComments: true
draft: false
math: true
---

### The relationship between power, sample size, effect size and type I error alpha

A second very important concept is the relationship of certain probabilities within the framework of statistical hypothesis testing.


There are several important concepts in statistics that are closely related when it comes to hypothesis testing. 


- \\(\alpha\\)  is the level of error that is accepted for erroneously rejecting the null hypothesis (although it is true) e rejected. It is usually set to 0.05 (one sided testing) or 0.025 (two sides testing). 

- Power is the probability of correctly rejecting  the null hypothesis when it is false, and accepting the alternative hypothesis. 

- Sample size refers to the number N of observations in a study. 

- Effect size is a measure of the magnitude of a difference or relationship in the data, for example between to populations. 

![image hypotheses](/images/experimental_results.png)


These concepts are interconnected because the choice of \\(\alpha\\) sample size, and effect size can all impact the power \\(1 - \beta\\)  of a statistical test. For example, increasing the sample size can increase power, while decreasing alpha can decrease power. Similarly, larger effect sizes are more likely to be detected with greater power, while smaller effect sizes may require larger sample sizes to achieve the same level of power.

![image power failure](/images/power_failure_effect.png)

## The relationship between standard deviation and effect size

The effect size \\(\delta\\) is the difference between two group means \\(\mu_1\\)
and \\(\mu_2\\) (the peaks in the figure above) divided by the standard deviation \\(\sigma\\)

Effect size \\(\delta\\) \\(= \frac{ \mu_1 -  \mu_2}{ \sigma}\\)

as we can see, the effect that can be detected is directly related to the standard deviation \\(\sigma\\).

To given an example:

Let's assume we have two group means \\(\mu_1\\) = 0.4 and \\(\mu_2\\) = 0.2 and two standard deviations \\(\sigma_1\\) = 0.5 and \\(\sigma_2\\) = 0.8. Let's just plug in the means  into the formula above:

Effect size \\(\delta\\) \\(= \frac{ 0.4 -  0.2}{ \sigma}\\)

From the above we can directly see that the  resulting effect size from those group means depends on the standard deviation in the denominator. 

Let's just test that:

Effect size \\(\delta\\) \\(= \frac{ 0.2 }{ 0.5}\\) = 0.4

Effect size \\(\delta\\) \\(= \frac{ 0.2 }{ 0.8}\\) = 0.25

Visually, this relationship becomes clear: A smaller standard deviation means a "narrower" distribution and less overlap between the curves. Thus, the effect size is an expression of how precise one is to measure a certain difference between two group means.

So, what makes a standard deviation small?

## What makes the standard deviation small?

First of all, let's remind ourselves of the relationship between variance and standard deviation:

Var =  \\({\sigma}^2\\)

thus: \\({\sigma}\\) = \\(\sqrt{Var}\\)

Let's just remind ourselves that the variance is just the averaged squared difference of each point in the data set from the mean:

Var = \\(\frac{\sum_{i=1}^{n}(x_i - \mu)^2} {n}\\)

From ththe above we can see that teh variance Var is directly related to N (larger N leads to smaller variance) - and if we take the root to get back to the standard deviation: 

\\({\sigma}\\) = \\(\frac{\sqrt{\sum_{i=1}^{n}(x_i - \mu)^2}} {\sqrt{n}}\\)

Thus, as we can see, the standard deviation is directly related to \\(\sqrt(n)\\) - the larger the sample size, the smaller the standard deviation.



References: [This paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7745163/) and [this website](https://sphweb.bumc.bu.edu/otlt/mph-modules/bs/bs704_power/bs704_power_print.html) are really nice.