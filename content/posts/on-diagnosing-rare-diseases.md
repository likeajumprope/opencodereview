---
title: "On diagnosing rare diseases"
date: 2023-02-27T10:53:14+11:00
Description: "Post"
Tags: ['bayestheorem', 'statistics']
Categories: []
DisableComments: true
draft: false
math: true
---

In this post, I want to dive into the interesting relationship between conditional and marginal probability within the Bayesian framework and how it can trick us into misleading conclusions.

Let's assume a patient presents with some symptoms S in an  emergency department. The symptoms are highly specific for a very rare disease D. How likely is it that the patient has the disease D given those symptoms S?

Let's just first define some terms amd the setting for this diagnosis.

### Marginal probability P(D)
First of all, despite the symptoms, the overall prevalence of the disease D is very rare. Let's assumed it's prevalence in the population is only P(D+) = 0.001 thus only 0.1% of individuals in the population have the disorder. We call this general probability  P(D+) *marginal* probability. This term originates from the location of the probability in a 2 x 2 truth table: in the margins of the table.

### Conditional probability P(S|D)

However, we have also defined that the patient presents with a lot of symptoms S that point towards the disease D.
Let's say that the patient shows all the symptoms S that are usually present in the disease D. We call this probability of the symptoms given that D is present *conditional probability* SP(S+|D+). In our case, we have defined that the patient shows all the symptoms that are associated with the disease D, so P(S|D) is rather high. Let's say P(S+|D+) = 0.9.

### Bayes Theorem

What wer are really interested in, however is not P(S+|D+), but the posterior probability P(D+|S+), or, how likely is it that the person has the disease, given the symptoms S+?

According to Bayes' theorem, we can compute the posterior probability:

$$
P(D+|S+)=\frac{P(D+) P(S+|D+)}{P(S+)}
$$

we have P(D+) = 0.001 and P(S+|D+) = 0.9, but what is still missing to calculate the posterior probability is the probability of P(S+).

The probability P(S+) is composed of two conditional probabilities: The probability that the symptom is present while the disease is present P(S+|D+) and the probability that the symptom is present while teh disease is absent P(S+|D-). 

We now have again to weight those probabilities again by the marginal probabilities P(D+) and P (D-):

$$
P(S+)=[P(D+)×P(S+∣D+)]+[P(D−)×P(S+∣D−)]
$$

### Prevalence, sensitivity and specificity

Terms that are often used in test theory are sensitivity, specificity and prevalence. It turns out that those terms coincide with the probabilities that we have just discussed!

- *Prevalence* is the marginal probability (in our case that the disease is present): P(D+).
- *Sensitivity* is a conditional probability (in our case that the symptoms are present given that the disease is present): P(S+|D+). In our case, the sensitivity specifies how "sensitive" the symptoms are for the disease.
- *Specificity* describes the probability that the symptoms are not present when the disease is not present: P(S-|D-).
