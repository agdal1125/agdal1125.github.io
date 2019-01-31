---
layout: post
title: Gradient Boosting
tags:
- statistics
- machine learning
- gradient

mathjax: true
---

# Concept of Gradient Boosting

## Boosting

In Machine Learning, Boosting refers to creating a stronger and more accurate learner by combining weak and simple learners. In other words, it is a technique of producing a stronger model by ensembling weak models. The principle that lies behind this concept is that integration of models may complement problems that individual models face.

--- 

## Gradient Boosting

##### Loss/Cost Function

Simply Saying, the learning (training) of machine is achieved by finding parameters that minimizes loss function.

Loss function (or cost fuction) is a function that maps the difference between estimated value and real value.

Of course, the objective of using loss function is to minimize it; a method to achieve optimization.


##### Gradient Descent

**Gradient Descent** is one of the methods used to find the optimal parameters when solving minimization problem of loss function.

By calculating the partial derivative of the loss function with respect to parameters, **gradient** (or slope) can be calculated. Since the gradient tells how much the output of a function changes by the changing the input, it can be used to direct the model to reach its local minimum.


##### References

https://en.wikipedia.org/wiki/Gradient_boosting
http://4four.us/article/2017/05/gradient-boosting-simply

