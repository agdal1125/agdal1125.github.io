---
layout: post
title: Spearman Correlation
comments: true
tags: 
- python3
- statistics
---
## Correlation

Correlation is a concept that is used to measure the association between variables, whether they are related or not. If the variables are related examining whether the relationship is positive or negative, or whether a specific model can explain the relationship. (Linear, non-linear)

&nbsp;

For example, pearson correlation measure the **"linearity"** of two continuous variables, assuming that the two variables follow normal distribution.

&nbsp;
&nbsp;
&nbsp;

### Spearman Correlation ($\rho$)

- Spearman's Correlation measures the correlation between two variables, taking their rankings into account. It evaluates the variables in a **non-parametric way**; meaning that it uses statistical method where data is not required to follow a normal distribution. In other words, Spearman correlation *does not assume anything about the distribution of data.*

-  The correlation is calcuated as a following equation: $\rho = 1 - frac{6\sum \d_{i}^{2}}{n(n^2-1)}$

