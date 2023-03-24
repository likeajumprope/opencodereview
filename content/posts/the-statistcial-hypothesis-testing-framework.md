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


There are several important concepts in statistics that are closely related when it comes to hypothesis testing. Alpha is the level of significance that is used to determine whether a null hypothesis can be rejected. It is usually set to 0.05 (one sided testing) or 0.025 (two sides testing). Power is the probability of correctly rejecting  the null hypothesis when it is false, and accepting the alternative hypothesis. Sample size refers to the number N of observations in a study. Effect size is a measure of the magnitude of a difference or relationship in the data, for example between to populations. 


| Type of choice      | Null hypothesis               | Alternative hypothesis  |
|:--------------------:|:----------------------------:|:------------------------:|
| Erroneous choice    | type I error (alpha)          | type II error (beta)     |
| Correct choice      | correctly accept the      | correctly accept the    |
|                     | null hypothesis               |alternative hypothesis (power)|

These concepts are interconnected because the choice of ,\\(\alpha\\)sample size, and effect size can all impact the power of a statistical test. For example, increasing the sample size can increase power, while decreasing alpha can decrease power. Similarly, larger effect sizes are more likely to be detected with greater power, while smaller effect sizes may require larger sample sizes to achieve the same level of power.

![image alt text](/images/power_failure_effect.png)

