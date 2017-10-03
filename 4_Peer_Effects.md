---
title: "Pre-Analysis Plan: 4. Peer effects"
author: "Adam Altmejd"
thanks: "Stockholm School of Economics, adam@altmejd.se"
date: "2017-10-03"
output:
  pdf_document:
    toc: false
---

# Peer Effects

Due to time constraints I have not been able to explore this research question to its fullest, but it is stated here for the sake of completeness. In the data set, most of the students that are randomized into fields will be in admission groups that are based on high school grades. For example to be admitted to medical school one usually needs a perfect GPA to even participate in the randomization. While a perfect high school GPA does not guarantee admission to medical school, a good enough score on the standardized test Högskoleprovet does. Most students hence do the test as well to increase their chances. This means that even though all students that are randomized have the same GPA, we will have another measure of performance that is independent from the random assignment and varies over applicants.

Using the scores from Högskoleprovet, I can look at the effect on everyone in a class from randomly getting smarter class mates. The model that I will test will look something like this:

For each class $c$, divide the students into those that were randomly admitted and those that were admitted deterministically, denoted $c_r$ and $c_d$ respectively. Then look at the average GPA after finishing university of the second group, $\text{GPA}_{c_d}$ and see how it is affected by the average test scores in the group that was randomly admitted on grades ($\text{TestScore}_{c_r}$).

$$
\text{GPA}_{c_d} = \alpha + \beta \text{TestScore}_{c_r} + X_i \gamma + \varepsilon_{c}
$$

The initial data set will not contain standardized test results. We will thus be able to register a new version of this pre-analysis plan before receiving the data needed for this analysis.