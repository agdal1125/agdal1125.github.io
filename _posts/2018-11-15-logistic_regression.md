---
layout: post
title: Logistic Regression
tags:
- statistics
- classification
- supervised learning
- regression

mathjax: true
---
# Logistic Regression

- Logistic Model is a statistical model that uses a logistic function to classify dependent variablea.

- In General, Logistic Regression is used for binary classification. (Pass/Fail, Alive/Dead, Win/Lose, etc...)

- As its purpose is mainly in binary classification, the model is often used for supervised machine learning.

- The dependent variables are labeled as 0 or 1.

- If the probability of predicting dependent variable to 0 is above 50%, the dependent variable will be classified as 0. Else, it would be classified as 1.

The Logistic Model derived from linear regression. If we set y as the probability of predicting one of the two dependent variables, classification becomes easy. 

If y > 0.5, it will be labeled as dependent variable A. If y < 0.5, it will be labeled as dependent variable B.

$$y = ax+b$$

However, as we can see from the linear regression model above, y and x can have infinite values. As the name suggests, the logistic model is derived from the linear equation by transforming it with __logit function__. 

### Logit Function

Logit function, or log-odds is __the logarithm__ of the __odds__(relative probability the event will happen) 

$$ odds : \frac{p}{1-p}$$
p is the probability that the event will happen. Thus, the logit function and inverse logit function is:

$$ logit(p)= ln\frac{p}{1-p}$$

### Logistic Function
Using the logit function, the linear model can be transformed as following equation:

$$ logit(p)= ln\frac{p}{1-p}= ax + b $$
$$ \frac{1-p}{p}= \frac{1}{e^{ax+b}} $$
$$  p= \frac{e^{ax+b}}{e^{ax+b}+1} $$

