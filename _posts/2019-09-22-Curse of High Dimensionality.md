---
 layout: post
title: The Curse of High Dimension
tags:
- Dimension
- Analysis
mathjax: true
---

<p align="middle" style="font-size: 11px">
  <img src="https://i.chzbgr.com/full/8249495040/h680F83E7/" width="500">source: https://cheezburger.com/8249495040</p>

<br>

It's a common knowledge that, we live in the 3-Dimensional space. 

We know that line represents 1-dimensional space, the square represents 2-dimensional space and a cube represents 3-dimensional space. However, not many people would be able to tell the definition of dimension. Dimension is an inevitable topic to data science, as more and more variables are included in the datasets. This post will start with definition of dimension and discuss about **the curse of dimension** in Data Science.

<br>

## Dimension

<br>

The dictionary meaning of dimension in general is "a measurable extent of some kind, such as length, breadth, depth or height"<sup>1</sup>. In this context, we can think of dimension as a way of representing particular physical quantities. Probably the most intuitive and easy way of explaining it is the definition below:

&nbsp;

> Dimension is the least number of coordinates required to describe any point within it. <sup>2</sup>&nbsp;

| 1-Dimension | 2-Dimension | 3-Dimension |
| :---------: | :---------: | :---------: |
|     (x)     |    (x,y)    |   (x,y,z)   |

&nbsp;

More mathematical way of expressing this concept is:

> When [linearly independent](https://agdal1125.github.io/2019/06/20/LA_terms_1.html) vectors span $S$, dimension is the number of linearly independent vectors in the basis for $S$.

&nbsp;

Still confused? Let's look at this data then:

| Index | Height(cm) | Weight(kg) | Foot size(mm) | Waist Size(cm) | Gender (M:1, F:0, O:2) |
| :---: | :--------: | :--------: | :-----------: | :------------: | :--------------------: |
|   0   |    175     |     80     |      265      |       83       |           1            |
|   1   |    180     |     68     |      280      |       79       |           1            |
|  ...  |    ...     |    ...     |      ...      |      ...       |          ...           |
|  999  |    162     |     48     |      235      |       66       |           0            |

&nbsp;

This data seems like a body measurement of a thousand people. There are height, weight, foot size and waist size. Let's say that we want to predict the gender variable with the other four variables. What do you think the dimension of this data is? 

Of course, including our dependent variable (or predicting variable), the dimension of this data is 5. We can create a vector with index 1 into (180,68,280,79,1). We can notice that the least number of coordinates required to describe this data is the number of variables. In a very simple way to put this, dimension of data corresponds to the number of variables in our analysis.

<br>

## Sparsity: The Curse

<br>

When you perform data analysis, there is a high chance that you will have more than 5 variables. In that case, your dimension would get larger. When dimensions get larger, the number of coordinates that it can cover grows exponentially. In other words, the matrix that you are working on would be a **sparse matrix**. (Most of the elements in the matrix are filled with 0). This means that amount of data need to generate good performance also grows exponentially. Moreover, the visualization would get much more harder when dimensions increase.

<p align="middle" style="font-size: 11px">
  <img src="https://dziganto.github.io/assets/images/sparse_matrix.png?raw=true" width="300"> a sparse matrix</p>

> *"A matrix is sparse if many of its coefficients are zero. The interest in sparsity arises because its exploitation can lead to enormous computational savings and because many large matrix problems that occur in practice are sparse"*<sup>3</sup>

&nbsp;

The curse that sparsity afflicts can be categorized into two perspectives: Space complexity and Time complexity

&nbsp;

#### Space Complexity

If matrix is sparse, many of its elements are zero. This suggests that even though there are a little number of non-zero entries in the matrix, all the zeros should be stored into the computer memory as well. In short,   memory would be definitely wasted by storing unmeaningful values, causing massive inefficiency in terms of storage. The larger the matrix and dimension gets, the more memory would be wasted in an exponential way.

&nbsp;

#### Time Complexity

What if our machine learning model tries to perform operations on the sparse matrix? Since most of the entries are zero-values, lots of time will be spent on doing meaningless calculations with zeros. This can be problematic when our model is complex and requires many calculations.

<br>

<br>



Citations:

$^1$https://www.lexico.com/en/definition/dimension 

<sup>2</sup>https://web.archive.org/web/20140111191053/http://curious.astro.cornell.edu/question.php?number=4

<sup>3</sup>pg.1, [Direct Methods for Sparse Matrices](http://amzn.to/2DcsQVU), Second Edition, 2017.



References:
- https://web.stanford.edu/class/stats202/content/lec2.pdf

- https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff

- https://www.opentutorials.org/module/3653/22071

- Direct Methods for Sparse Matrices](http://amzn.to/2DcsQVU), Second Edition, 2017

- https://machinelearningmastery.com/sparse-matrices-for-machine-learning/

  



