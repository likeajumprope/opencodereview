---
title: "Why most research findings are false"
date: 2023-01-27T10:53:14+11:00
Description: "Post"
Tags: []
Categories: []
DisableComments: true
draft: false
ploty: true
---

In his famous paper ["Why most research findings are false"](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.0020124) Dr. John Ioannidis proofs that most research findings are false. Given that his paper is quite technical, I will go over his rationale here again.

## Concepts

### R: the relationship between true and false relationships in a field

The first concept that is introduced is *R* which is considered to be *the relationship between "true relationships" and "no relationships"* in all tests in a certain field.

When the number of true relationships in a field = 0.2 and the number of no relationships = 0.8 then:

{{< highlight py3 "style=autumn" >}} R = 0.2/0.8 = 0.25{{< /highlight >}}
Thus, *R* is just the ratio of true and false relationships before any study has been undertaken. Or, if you would select randomly, you you would find that 30% of tests turn out true and 70% turn out false.

From this, it is also easy to conclude that the pre-study probability of getting a true test is:

{{< highlight py3 "style=autumn" >}} R/R+1 = 0.25/(0.25+1) = 0.2  {{< /highlight >}}

which is exactly what we have defined before.

# plotly test
{{< load-plotly >}}
{{< plotly json="/mtbruno.json" height="500px" >}}