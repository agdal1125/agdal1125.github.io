---
layout: post
title: Parametric vs Non-parametric
tags:
- Parametric
- Non-parametric
- Population
- Sample
mathjax: true
---

Statistics have two main branches: descriptive statistics and inferential statistics. 

**Descriptive Statistics** tries to "describe" the data by summarizing it with the use various measurements. For example, let's say that you are a teacher responsible for 40 students in your class. How would you answer the questions like this?

- How tall are your students?

Are you going to name all the students and their height? This would be the most exact answer, but take a lot of time. Instead, you can say, "my students are 140cm in average, and they are all similar except for a few who are shorter". This definitely does not tell all about your student's height, but provides a ballpark figure. In terms of statistics, this answer is given by combining **central tendency** (*average*) and the **spread or variability** (*all similar except for a few*). 

&nbsp;

The other branch is **Inferential Statistics**, where "inference" or "prediction" is made with given data. Unlike descriptive statistics that focuses only on explaining the given data in an efficient and effective way, inferential statistics tries to go beyond the given data. Just like the image below:



<img src="https://eliamdur.com/wp-content/uploads/2018/08/Eleohabt-1110x550.jpg">

<p align="center" style="font-size: 10pt;">source: https://eliamdur.com/index.php/2018/09/08/the-blind-men-and-the-elephant/   illustration by Hans Moller</p>
The blind men are trying to guess what this "thing" is by touching a part of an elephant. In statistics, the elephant is **population**, which is the actual or whole picture that we are trying to infer. The parts of elephant that blind men are touching are **samples**. Simply saying, inferential statistics is about guessing the    elephant from what you touch; inferring population from samples.

Finally, we are all on the same page now! Let's talk about this post's main topic: parametric vs non-parametric.

<br>

### Parametric Statistics

<br>

>  **"Parameter** (Statistical Parameter; Population Parameter) is a quantity entering into the probability distribution of a statistics or a random variable" <sup>1</sup>

Can you tell the difference between parameter and variable? This can be a first step of understanding the difference between parametric and non-parametric statistics. 

- "Variables are quantities which vary from individual to individual."<sup>2</sup>
- "Parameters do not relate to actual measurements, but to quantities defining a theoretical model".<sup>3</sup>

Parameters are values that refer to specific family of distribution. It can be used to define model or altered to see how model changes. In short, we should not treat values from data as parameters. 

Let's look at the mathematical expression below:

$$X \sim N(3,2^2)$$

We consider 3 and 2 as parameters, but not as variables. This is because 3 and 2 are mean and variance that can define a particular distribution in the family of normal distribution. They are **"quantities defining a theoretical model"**, which in this case is a Gaussian distribution.

So, parametric statistics has assumption in its base line; the sample data is derived from a particular population distribution with a fixed number of parameters. Therefore, linear regression, logistic regression and student t-test are examples of parametric statistics. 

<br>

### Non-Parametric Statistics

<br>

If parametric statistics has assumption, is non-parametric statistics assumption-free? 

**No**. Non-parametric statistics do not have assumptions in terms of distribution. It is true that non-parametric statistics has a fewer assumptions than parametric statistics, but there still are other assumptions depending on methods. ([Lists of non-parametric methods](https://en.wikipedia.org/wiki/Nonparametric_statistics#Methods))

Non-parametric methods are usually used when the data is in an ordinal variable or rank. Order statistics is a branch of non-parametric statistics that is relevant to this. You are advised to use non-parametric methods when:

- Sample size is small to risk making assumptions
- Data is not symmetric
- Data has too many important outliers. (When the median represents the central tendency better than the mean)

<br>

<br>

### It's Up to You

<br>

Usually, parametric statistics are favored over non-parametric statistics. This is because parametric statistics are more powerful than non-parametric ones, **if the assumptions are correct**. Because non-parametric methods do not make assumptions with distribution and according parameters, it is safer but less powerful. Using which type of statistics would differ by data, situation and context. 

Just like everything else, choosing between the two statistics depends on the context, as there is no absolute rule in our world. 

<br>

#### Citations



<sup>1</sup>  [Kotz, S.](https://en.wikipedia.org/wiki/Samuel_Kotz); et al., eds. (2006), "Parameter", *Encyclopedia of Statistical Sciences*, [Wiley](https://en.wikipedia.org/wiki/Wiley_(publisher)).

<sup>2</sup> *BMJ* 1999;318:1667 (https://www.bmj.com/content/318/7199/1667)

<sup>3</sup> *BMJ* 1999;318:1667 (https://www.bmj.com/content/318/7199/1667)