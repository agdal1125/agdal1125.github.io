---
layout: post
title: Bias-Variance Tradeoff
tags:
- Bias
- Variance
- Machine Learning
mathjax: true
---

## Choose 2 from 3 
### (feat. $3\choose2$ Your College Life)



| Choose 2                                                     |                         Consequences                         |
| ------------------------------------------------------------ | :----------------------------------------------------------: |
| <img src="https://pics.me.me/social-l-life-good-grades-choose-two-enough-sleep-choose-2239262.png" width="300" align="left" vertical-align="bottom"> | <img src="http://s3.favim.com/orig/45/grade-lol-sleep-social-life-troll-Favim.com-408205.jpg" width="300" align="right" vertical-align="bottom"> |

&nbsp;

At some point of life, you might have seen this popular meme. Although this meme assumes that the three options are mutually exclusive with binary values, it teaches the lesson that you can't always have everything. In economics, they call this opportunity cost, where "the loss of potential gain from other alternatives occurs when one alternative is chosen". (In short, it's a trade-off) This type of "trade-off" situation also appears when you try to build a machine learning model: **Bias-Variance Trade-off**

<br>

## Choose one? Low Bias vs. Low Variance

&nbsp;

<img src="https://pbs.twimg.com/media/CpWDWuSW8AQUuCk.jpg" width="400">

&nbsp;

The image above provides intuitive definition of bias and variance.**Bias** in statistics is a difference between an estimator's expected value and the true value or the estimated parameter. **Variance** refers to the fluctuations of modeling. Every machine learning objective is to create a model with low bias and low variance. However, this is practically impossible, as variance and bias are in a "tug of war" relationship. 

&nbsp;

#### Proof using Mathematical Expression

Let's assume that we would like to fit a model $y = f(x) + \epsilon$. $y$ is our target or predicting variable and $f(x)$ is a true function that we want to approximate. $\hat{f}(x)$ is our model and $\epsilon$ is the noise with zero mean and variance $\sigma^2$. 

We want our model to be as accurate or close as the true function. Thus, mean squared error between $y$ and $\hat{f}(x)$ is computed and we would want to minimize that value.

&nbsp;

##### Objective: minimize $E[(y- \hat{f}(x))^2]$

- Bias of our function is:
    $ Bias[\hat{f}(x)] = E[\hat{f}(x)] - E[f(x)]$
- Variance of our functions is:
    $ Variance[\hat{f}(x)] = E[\hat{f}(x)^2] - E[f(x)]^2$

&nbsp;


Let's write 
- $\hat{f}(x)$ ---> $\hat{f}$
- $f(x)$ ---> $f$

&nbsp;

Because $y=f$, we can derive this equation like this:

<img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/8c9708ee63cacf05f3bdbba9170fd8c687eecd03" width="700">

&nbsp;

Thus: 

 $E[(y- \hat{f}^2]= (Bias[\hat{f}])^2 + Variance[\hat{f}] + \sigma^2$

- $\sigma^2$: irreducible error

<br>

Now, here is the thing. We know that squared values are always non-negative, and variance is also non-negative. In this sense, the values in the equation are always non-negative. Since the left side of equation can be minimized and $\sigma^2$ is an according constant, only Bias and Variance are left to toggle. Therefore we can know that if we lower Bias, Variance increases and vice versa. 
This is why low bias and variance for a model cannot be achieved. So, we have to make a compromise between variance and bias like the image below:

&nbsp;

<img src="https://lh4.googleusercontent.com/k7fm8oOB8fY3S57dOzc1MUsRjeSLSBKX8ZvMOvV3JZKXRzrM7OhCvIF2En5ahfzJHcW8uxDaF0bd3dYc4_HK52JVXd_SJ6pVrAOjHm1b3QSSC9Ne_t5VmrKto15BmF_kn4mN_64dirU" width="500">



<br>

## How to Overcome this Dilemma





<br>



References:
- https://web.stanford.edu/class/stats202/content/lec2.pdf
- https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff
- https://www.opentutorials.org/module/3653/22071