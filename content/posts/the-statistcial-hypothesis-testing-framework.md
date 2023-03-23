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

### 2. The relationship between power, sample size, effect size and type I error alpha

A second very important concept is the relationship of certain probabilities within the framework of statistical hypothesis testing.

| Type of choice      | Null hypothesis             | Alternative hypothesis |
|---------------------|-----------------------------|------------------------|
| Erroneous choice    | type I error (alpha)        | type II error (beta)   |
| Correct choice      | correctly accept the null hypothesis  | correctly accept the alternative hypothesis (power)  |

Alpha is the level of significance that is used to determine whether a null hypothesis can be rejected. Power (1- beta) is the probability of correctly rejecting the null hypothesis when it is false.

{{<table “table table-striped table-bordered">}}
|———-|———-|———-|
| Item 1   | Item 2   | Item 3   |
| Item 1a  | Item 2a  | Item 3a  |
{{</table>}}