---
layout: post
title: Error vs Residual
tags:
- Residual
- Error
- Regression
- SST
- SSE
- SSR
- RMSE

mathjax: true
---

To be honest, I have always had problems with terminologies used in Statistics. Because they sound to similar and they are expressed in similar ways, it is quite confusing. One of the confusing concepts was difference between error and residual.

<br>

### Error (Disturbance) - $\varepsilon , \epsilon$ 

In a simple way to put this, statistical error is the difference between observed value and **true** value (unobservable in most situations). The whole purpose of inferential statistics is to find properties of population using your data. 

Error is the quantity that tells how much the **truth** or **values in population** deviate from a **true model**. In Statistics, **error** is inevitable. Your observations cannot be 100% true, because how you collect data can defintely influence the observations. These types of errors are more involved with **observational error**.

Let's look at a simple linear regression equation below:

$Y_i = \beta_1 + \beta_2X_i + \epsilon_i$

<br>

We can write this as a matrix form:

$$ \bold{y} = \begin{pmatrix} y_1 \\ y_2 \\ y_3 \\ . \\ . \\ \end{pmatrix},\ \bold{X}= \begin{pmatrix} 1 &x_1 \\ 1 & x_2 \\ 1 & x_3 \\ . & . \\ . &. \\ \end{pmatrix}, \ \bold{B} =\begin{pmatrix} \beta_1 \\ \beta_2\end{pmatrix} , \ \bold{\varepsilon} = \begin{pmatrix} \epsilon_1 \\ \epsilon_2 \\ \epsilon_3 \\ . \\ .  \\ \end{pmatrix}$$

$\bold{\varepsilon} = \bold{y} - \bold{X}\bold{B}$

<br>

The error term $\epsilon_i$ is used to capture the difference between actual true value and the **true linear model** or true fit line ($\beta_1 + \beta_2X_i$) . It would be easier to think of these terms as "theoretical". You don't know them and cannot get them. This is because we don't have all data points from the population. However, we are going to use our observations to estimate the model and error.

<br>

### Residual - $r_i$

Residual is an estimate of error. It is an "observable estimate" of unobservable statistical error"<sup>1</sup>. Because we don't know the true model, we cannot calculate the error either. So we estimate the two parameters of linear model ($\hat{\beta_1}, \hat{\beta_2}$) and calculate estimate of errors.

$Y_i = \hat{\beta_1} + \hat{\beta_2}X_i + r_i$

<br>

We can write this as a matrix form:

$$ \bold{y} = \begin{pmatrix} y_1 \\ y_2 \\ y_3 \\ . \\ . \\ y_n \end{pmatrix},\ \bold{X}= \begin{pmatrix} 1 &x_1 \\ 1 & x_2 \\ 1 & x_3 \\ . & . \\ . &. \\ 1 & x_n\\ \end{pmatrix}, \ \bold{\hat{B}} =\begin{pmatrix} \hat{\beta_1} \\ \hat{\beta_2}\end{pmatrix} , \ \bold{r} = \begin{pmatrix} r_1 \\ r_2 \\ r_3 \\ . \\ . \\ r_n \end{pmatrix}$$

$\bold{r} = \bold{y} - \bold{X}\bold{\hat{B}}$

<br>

Notice that $\bold{y}$ is not the same as the one on the error. Although residuals are different from errors, the two terms are somewhat used interchangeably, because they are used instead of errors. We use residuals to find out what information has not been captured by our model. 

<br>

<img src="/assets/images/err_res.png" width="600" height="600"> 
<sup>source = "https://www.youtube.com/watch?v=snG7sa5CcJQ"</sup>











<sup>1 https://en.wikipedia.org/wiki/Errors_and_residuals</sup>