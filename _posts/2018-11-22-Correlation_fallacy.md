---
layout: post
title: Misunderstanding Correlation & Base Rate Fallacy
comments: true
tags:
- correlation
- statistics
- causation
- base rate fallacy
- base rate neglect

mathjax: true
---



## Correlation does not imply Causation

<br>



<p align="right" style = "font-size: 11px">
  <img src="https://www.statisticshowto.datasciencecentral.com/wp-content/uploads/2016/03/spurious-correlation-2.png" width="700">source: https://www.statisticshowto.datasciencecentral.com/spurious-correlation/</p>

&nbsp;

"We can definitely save astronaut's life by using seatbelts in the car!"

You would probably laugh at this statement, because it is pretty obvious that this is a **spurious correlation**. Many research papers and people make mistakes by associating correlation with causality. 

**"Correlation does not imply causation"**. It does not guarantee anything, but only shows a possibility

<br>

​	*A.  Strong positive correlation between annual ice-cream sales and number of drownings*

​	*B.  Strong positive correlation between number of bars and churches in the city*

​	*C.  Strong positive correlation between life expenctancy and hormone supplements for middle aged*

<br>

The following correlations above are all fallacious. More logical reason or cause of *A* would be seasonal changes. You would eat more ice cream and swim on the hot summer than in the cold winter. *B* is just an observation based on different size of cities. Of course you would have more churches and bars in New York than in Alaska. *C* is a bit tricky, but "money" turns out to be the causal factor behind this correlation. The richer you are, the more you can afford to spend on your health.

Likewise, high correlation fools us to think that there is an actual casual relationship between the two variables. Here are some types of correlation mistakes:

<p></p>
1. **Spurious Correlation**

   All the examples that we have talked about above, is spurious correlation. This is a deceptive association due to some other variables in between them. Season, size of the city, money were the hidden key variables in these cases. 

   &nbsp;

2. **Coincidental Correlation**

   "Annual number of people drowned by falling into a swimming pool has high correlation with the annual number of films Nicholas Cage appeared in". The two figures are just a coincidence. We cannot blame Nicholas Cage for the death of all drowned people in the swimming pool. This is what we call coincidental correlation.  

&nbsp;

Once again, Correlation does not lead to Causation. So, be careful with your correlation coefficient. 
Also, try to think about the images below.

<img src="/assets/images/egg_yes.png" width="700">

<br>

<img src="/assets/images/egg_no.png" width="700">

&nbsp;&nbsp;

## Base Rate Fallacy (Base Rate Neglect)

<br>

Base rate fallacy is another logical error that we are often exposed to. We are prone to jumping into conclusions without thinking about the whole picture. This happens when we make irrational decisions based on our bias or belief, in favor of statistical probability or ignore general  . 

**Base rate** is the probability of event also known as prior probabilities in Bayesian term. In an easy way to put this, it is "a percentage of a population that demonstrates some characteristics"<sup>1</sup>. Obviously, when base rate is ignored or neglected, fallacy occurs. Here's an example:

<br>

> - 0.5% of students cheat on their quiz
>
> - Teachers catch cheaters with a 5% false positive rate (type 1 error; caught cheating but innocent in fact)
>
> - Teachers examine all 1000 students taking their quiz
>
> Now, Michael is caught by teachers as a cheater. What would be the chance that he is innocent?

<br>

Base rate fallacy occurs when people think that Michael is innocent by 5%, only considering information on the second bullet point. 

In fact, 1000 students will be examined. Among these students **only 5 students will cheat**(the base rate), **but the teachers will catch 50 students as cheaters**. In this sense, Mike will be innocent by 90% (45/50) chance.

<br>
*Most smart women with very high IQ scores date someone else dumber than them*

Now we all know that this is not surprising if we think of the base rate; super smart women are more likely to encounter people dumber than them. 

<br>

<br>

References

<sup>1</sup> https://link.springer.com/referenceworkentry/10.1007%2F978-0-387-79061-9_289

