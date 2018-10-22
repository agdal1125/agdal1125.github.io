---
layout: post
title: Naive Bayes Classifier
tags:
- statistics
- bayesian
- machine learning
mathjax: true
---
&nbsp;

## Naive Bayes Classifier
&nbsp;

Naive Bayes is one of the machine learning techniques used for classification and prediction. Obviously, it involves [Bayesian Theorem](/2018/10/10/Bayes-Theorem.html). The classifier assumes that all **explanatory variables are independent to each other** respectively contributing to the response variable.

#### Advantage

- Naive Bayes classifier can be trained effectively on Supervised Learning Environment, because it does not require a lot of data for training.

- Despite its simplicity and design, it has been proven to work well in various complex situations

    
&nbsp;
&nbsp;

### Model

Naives Bayes Model is conditional probabilistic model. The $$n$$ features (independent explanatory variables) are represented as vector $$\mathbf x = (x_1,x_2,x_3,x_4,....x_n)$$,  which is the data given for instance classification. 

The instance probabilities are $$p(C_k \vert x_1,...,x_n)$$. In other words, the probability is calculated for all $$K$$ (or $$C_k$$) possible outcomes. 

&nbsp;
&nbsp;

<div style="text-align:center">Instance Probability Model</div>

$$p(C_k \vert \mathbf x) \biggl(= p(C_k \vert x_1,...,x_n)\biggr) = {p(C_k)*p(\mathbf x \vert C_k) \over p(\mathbf x)} $$

&nbsp;
&nbsp;
&nbsp;

The denominator $p(\mathbf x)$ is always the same, so when comparing probability between instances and find the best classification, the numerator part is the one that only matters.

Using the characteristics of conditional probability and if the explanatory variables are independent, the numerator part above can be altered like this:
<div style="text-align:center">.</div>
<div style="text-align:center">.</div>
<div style="text-align:center">.</div>
&nbsp;
&nbsp;

<div style="text-align:center">Altered Numerator</div>

$$\begin{align}
p(C_k)*p(\mathbf x \vert C_k) \\
& = p(C_k)*p(x_1,...,x_n \vert C_k)\\

& = p(x_1,...,x_n,C_k)\\

& = p(x_1 \vert x_2,..,x_n,C_k)*p(x_2,...,x_n,C_k)\\
  
& = p(x_1 \vert x_2,..,x_n)*p(x_2 \vert x_3,...,
  x_n)*p(x_3,...,x_n,C_k)\\
  
& = ...\\
  
& = p(x_1 \vert x_2,..,x_n,C_k)*p(x_2 \vert x_3,...,x_n,C_k)*p(x_3 \vert x_4,...,x_n,C_k)...*p(x_{n} \vert C_k)*p(C_k)\\
  
& = p(x_1 \vert C_k)*p(x_2 \vert C_k)*p(x_3 \vert C_k)...*p(x_{n-1} \vert C_k)*p(x_n \vert C_k)\\
  \end{align}$$


Thus, the final model can be written as:

$$
p(C_k \vert \mathbf x) \varpropto p(C_k)*\prod_{i=1}^{n} p(x_i \vert C_k)
$$

In short, the Naive Bayes Classifier is product of all conditional probablities of explanatory variables to the given category and the probability of category itself.

