---
title: "Pre-Analysis Plan: 5. Education and Financial Decision Making"
author: "Adam Altmejd and Thomas Jansson"
thanks: "Stockholm School of Economics, adam@altmejd.se"
date: "2018-02-28"
---

# Introduction

Stock market participation varies greatly between socio economic groups, potentially exacerbating wealth inequality. In many countries far less than half the population own stocks or mutual funds, and while Sweden is in the absolute top, participation is still only at around 70% [@Guiso2013_household_finance]. While most Swedish citizens get some exposure to the stock market through the pension system participation is clearly correlated with wealth, income and education [@Mankiw1991_consumption_stockholders;@Haliassos1995_why_few; @Guiso2003_household_stockholding].

In this project we plan to study how education influences household financial sophistication. While the amount of college education is positively associated with income in general, there is quite substantial return heterogeneity between fields [@Kirkeboen2016_field_study]. We study if the same is true for financial decisions. Can one explain sophistication completely by the overall increase in wealth and earnings from education, or do some fields (like finance and business) actually increase financial literacy and make people better investors?

@Christiansen2008_are_economists use different quasi-experimental methods to look specifically at economists and find that they are indeed more likely to hold stocks. In their sample of Danish households, having an economics education increases stock market participation on both the individual and the household level. Our project is in part an extension of this paper. But we use a proper natural experiment to robustly measure the causal effect of different fields of education and are thus able to better account for both selection into fields that provide finance education as well as the the income and wealth heterogeneity between fields that could otherwise bias the results.

Previous research using Swedish wealth data has shown that while the asset holdings of Swedes are quite well diversified, wealthy and highly educated individuals are more likely to enter the market and also to make better trading decisions [@Calvet2009_fight_flight]. Education and financial sophistication is associated with faster portfolio rebalancing, but also higher volatility. @Calvet2007_out_assessing show that since educated household invest more aggressively they also incur larger return losses from under diversification and @Vissing-Jorgensen2003_perspectives_behavioral finds evidence of a clear relationship between financial rationality and wealth. Last, @Almenberg2015_gender_stock find a substantial gender gap in stock market participation, but it diminishes when controlling for financial literacy.

While these results make it abundantly clear that a relationship between education and financial literacy exists, most studies are unable to tease out any causal mechanisms. It is possible that wealthier individuals invest more time into managing their portfolio, or that they select into education programs that provide classes in finance. By better understanding to what extent education improves financial literacy and decision making, this project will evaluate a route towards improving stock market participation, alleviating the gender gap in financial literacy, and, in the long run, potentially decreasing overall wealth inequality.

# Data

The data set presented in chapter 1 is extended with information about individual financial wealth. Data on the wealth holdings of Swedish citizens is only available between 1999 and 2007. The wealth registry includes disaggregated data on all global assets held by each individual on December 31st of each year. The data also includes debt, pension savings and interest rate payments. This level of detail allows us to really pin down the financial behavior of individuals, and actually analyze changes is positions over time. We can thus also study within-individual differences increases accuracy of estimates.

# Analytical Framework

In our main analysis we study two margins, the extensive (does the individual engage in the stock market) and the intensive (how much of an individuals wealth is in stocks, and how well are they performing). For the sake of simplicity we here only discuss the extensive margin. The other models would simply have different dependent variables for returns and exposure.

We would like to estimate

$$
\mathbb{I}(\text{Owns stocks or mutual funds}_i) = y_i = \alpha + \beta \text{Financial Educ}_i + \varepsilon_i,
$$

where the left-hand side indicator function takes the value $1$ if individual $i$ participates in the stock market. However, as was alluded to above, the $\beta$ coefficient in such a model would be biased. People interested in financial education are also interested in holding stock and would thus select into both. To get around this problem we need to instrument financial education with the admission lotteries in a 2SLS specification. The second stage would then be

$$
y_i = \alpha + \beta \text{Financial Educ}_i + X_i\gamma + \varepsilon_i,
$$

and the first stage

$$
\text{Financial Educ}_i = \alpha + \pi z_i + X_i\gamma + u_i.
$$

Here, education is instrumented by $z_i$, a dummy variable taking the value $1$ if the applicant is successfully randomized into a program that includes financial education. The endogeneous dependent variable $\text{Financial Educ}$, on the other hand, is $1$ whenever the applicant has degree from a program that includes financial education. $X_i$ is a set of controls, importantly consisting of fixed effects for the interaction of fields and institutions that the applicant is randomized between, to control for individual preferences.

<!--
## Spillover Effects

If a member of the household takes finance classes it is possible that he or she will aid other family members in their decisions. These spill over effects could potentially be large, impacting both the household but also parents and siblings. We will identify family ties and estimate increases in returns and stock market participation on the whole family. -->


# References