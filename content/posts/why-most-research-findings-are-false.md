---
title: "Why most research findings are false"
date: 2023-01-27T10:53:14+11:00
Description: "Post"
Tags: ['reproducibility']
Categories: []
DisableComments: true
draft: false
---

In his famous paper ["Why most published research findings are false"](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.0020124) Dr. John Ioannidis proofs that most research findings are false. Given that his paper is quite technical, I will go over his rationale here again.

## Concepts

### 1. R: the prior probability

The first concept that is introduced is *R* which is considered to be *the relationship between "true relationships" and "no relationships"* in all tests in a certain field.

When the number of true relationships in a field = 0.2 and the number of no relationships = 0.8 then:

{{< highlight py3 "style=autumn" >}} R = 0.2/0.8 = 0.25{{< /highlight >}}
Thus, *R* is just the ratio of true and false relationships before any study has been undertaken. Or, if you would select randomly, you you would find that 30% of tests turn out true and 70% turn out false.

From this, it is also easy to conclude that the pre-study probability of getting a true test is:

{{< highlight py3 "style=autumn" >}} R/R+1 = 0.25/(0.25+1) = 0.2  {{< /highlight >}}

```
R = R/R+1 = 0.25/(0.25+1) = 0.2 
````


which is exactly what we have defined before.

Taking into account the prior probability of a research finding being true or false is actually an important step. To illustrate that consider this:  A researcher group presents data that shows that a certain brain region is associated with the full symptom spectrum of depression. We know by now that such one-to-one mappings between a certain brain region and a specific disorder does not exist. This makes such finding *a priori* very unlikely and might be a first indicator that the finding might be not replicable. 

### 2. The relationship between power, sample size, effect size and type I error $\alpha$.

A second very important concept is the relationship of certain probabilities within the statistical testing framework.

