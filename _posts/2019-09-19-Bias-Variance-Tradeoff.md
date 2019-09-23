---
layout: post
title: Bias-Variance Tradeoff
tags:
- Bias
- Variance
- Machine Learning
mathjax: true
---

## Choose one? Low Bias vs. Low Variance



An archer tries to shoot 100 arrows to his target. Low bias refers to a situation where archer's shots are relatively clustered close to the center of the target. Low variance refers to a situation where the archer's shots were well-clustered and consistent. A good archer would make his shots with low bias and low variance. This is exactly what our machine learning model should be trained to do. 

&nbsp;

<img src="https://pbs.twimg.com/media/CpWDWuSW8AQUuCk.jpg" width="400">

&nbsp;

The image above provides intuitive definition of bias and variance. **Bias** in statistics is a difference between an expected value of estimator and the "real" value of the estimated parameter. On the other hand **Variance** refers to the fluctuations of modeling. 

Bias occurs when you fail to learn from the training data. If the archer does not practice much, it is more probable that he would miss the center. This is called **underfitting**; your model fails to learn from the training data.

If the archer does his practice, he would generate "low variance" result. The more archer trains the lesser spread of arrow shots would become. However, if the target changes, **low variance high bias** result will be shown in that target. This is because the archer trained too much on a specifically shaped target. This is called **overfitting**; your model trains too much on the dataset, that it fails to predict on other dataset or real life. 

Every machine learning model would want to have low bias and low variance. We want all of our arrows (estimation) to hit the very center of target (real values). However, this is practically impossible, as variance and bias are in a "tug of war" relationship. 

<br>

## Trade off

### (feat. $3\choose2$ Your College Life)



| Choose 2                                                     |                         Consequences                         |
| ------------------------------------------------------------ | :----------------------------------------------------------: |
| <img src="https://pics.me.me/social-l-life-good-grades-choose-two-enough-sleep-choose-2239262.png" width="300" align="left" vertical-align="bottom"> | <img src="http://s3.favim.com/orig/45/grade-lol-sleep-social-life-troll-Favim.com-408205.jpg" width="300" align="right" vertical-align="bottom"> |

&nbsp;

At some point of life, you might have seen this popular meme. Although it assumes that the three options have binary values (either you can have it or not) in a mutually exclusive way, it teaches the lesson that you can't always have everything. In economics, this problem can be associated to opportunity cost, where "the loss of potential gain from other alternatives occurs when one alternative is chosen"$^1$ (In short, it's a trade-off). Bias and Variance also have this type of "trade-off" relationship, in a supervised machine learning model.

<br>

#### Proof using Mathematical Expression

Let's assume that we would like to fit a model $y = f(x) + \epsilon$. $y$ is our target variable and $f(x)$ is a true or real function that we want to approximate. $\hat{f}(x)$ is our model and $\epsilon$ is the noise with zero mean and variance $\sigma^2$.  We want our model to be as accurate or close as the true function and "close" in mathematics are usually defined with a small difference. To achieve this, mean squared error between $y$ and $\hat{f}(x)$ is computed for minimization. 

&nbsp;

Objective: **minimize $E[(y- \hat{f}(x))^2]$**

- Bias of our function is:
    $ Bias[\hat{f}(x)] = E[\hat{f}(x)] - E[f(x)]$
- Variance of our functions is:
    $ Variance[\hat{f}(x)] = E[\hat{f}(x)^2] - E[f(x)]^2$

&nbsp;


Let's write 
- $\hat{f}(x)$ as  $\hat{f}$
- $f(x)$ as  $f$

&nbsp;

Because $y=f$, we can derive this equation like this:

<img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/8c9708ee63cacf05f3bdbba9170fd8c687eecd03" width="700">

&nbsp;

Therefore: 

 $E[(y- \hat{f}^2]= (Bias[\hat{f}])^2 + Variance[\hat{f}] + \sigma^2$

- $\sigma^2$: irreducible error

<br>

Now, here's the thing. We know that squared values are always non-negative, and variance is also non-negative. In this sense, the values in the equation are always non-negative. Since the left side of equation can be minimized and $\sigma^2$ is an according constant, only Bias and Variance are left to toggle. Therefore we can know that if we lower bias, variance increases and vice versa; the tug of war between the two has been explained. This is why low bias and variance for a model cannot be both achieved. So, we have to make a compromise between variance and bias like the image below:

&nbsp;

<img src="https://lh4.googleusercontent.com/k7fm8oOB8fY3S57dOzc1MUsRjeSLSBKX8ZvMOvV3JZKXRzrM7OhCvIF2En5ahfzJHcW8uxDaF0bd3dYc4_HK52JVXd_SJ6pVrAOjHm1b3QSSC9Ne_t5VmrKto15BmF_kn4mN_64dirU" width="500">

<br>

<br>



Citations:

$^1$ https://www.lexico.com/en/definition/opportunity_cost



References:
- https://web.stanford.edu/class/stats202/content/lec2.pdf
- https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff
- https://www.opentutorials.org/module/3653/22071



