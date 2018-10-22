---
layout: post
title: Bayes' Probability
tags:
- statistics
- bayesian
- probability
mathjax: true
---
&nbsp;

## Bayes' Theory  
&nbsp;

In probabilistic study, there are two main stream approaches:

1. Frequentist Approach( *the classic probability* )
    - Define probability as an event's relative frequency in a large number of trials when performed infinite times
    - $$P(x) = \lim_{n_t -> \infty} \frac{n_x}{n_t}$$
    - $$n_t$$ is total number of trials and $$n_x$$ is number of that event $$x$$ occurred and $$P(x)$$ is the probability
    - However, application of frequentist approach is nearly impossible in the real word, because you cannot simply try everything infinite amount of times. It is difficult to apply real world problems...
       

&nbsp;
&nbsp;

2. Bayesian Approach
    - Define probability as a **"degree of belief"**. It is subjective, but not random
    - Experience and data are used to **update** the probability
    - Practical to apply in real world problems!!
    
    - Bayesian Theorem: 
    $$P(H|E) = {P(H \bigcap E) \over P(E)} = \frac{P(E|H)*P(H)}{P(E)} =  \frac{P(E|H)*P(H)}{P(H)*P(E|H) + P(H^c)*P(E|H^c)}$$
         
         - $$ P(H) $$ is called the prior probability, the probability that you know before the "update" 
         
         - $$ P(H \vert E) $$ is called the posterior probability, the updated probability with new information
         
         - The Bayesian Theorem uses conditional probability to update prior probability to posterior probability


&nbsp;
&nbsp;
&nbsp;
&nbsp;


> #### Conditional Probability
>
> $$P(A \vert B) = {P(A \cap B) \over P(B)} $$ 
> - Given that event B occurred, the chance that $$P(A)$$ also occurred. (probability of A given B)
> - if the two events A and B are completely independent,  $$P(A \vert B) = P(A)$$
> - This implies that information of B is irrelevant or useless when you want to know A

&nbsp;
&nbsp;


## Example

Let's say that a mother is in her 40s. She got a positive reaction from X-ray examination of breast cancer. What is her probability of really having a breast cancer?

- Probability that women in her 40s will have a breast cancer is 1%
- Probability that cancer patient of women in 40s will be diagnosed positive from X-ray examination is 90%
- Probability that healthy women in 40s will be diagnosed positive from X-ray examination is 5%

> #### Solution
> The probability that we want to know is $$P( c \vert p)$$ 
>
> Given informations are:
> - $$P(c)$$ = 0.01 
> - $$P(p \vert c)$$ = 0.9
> - $$P (p \vert c^c)$$ = 0.05
>
> Using the Bayes theorem:
> $$P(c \vert p) = {P(c)*P(p \vert c) \over P(p)}$$
>
> So all we need to know is the value of $$P(p)$$ which is:
> ##### $$P(p) = P(p|c)*P(c) + P(p|c^c)*P(c^c) = 0.9*0.01 + 0.05*0.99 = 0.0585$$
>
> The final calculation of what we want to know would be: 
> 0.01 * 0.9 / 0.0585 = 0.15384...
>
> Thus, the probability that a mother will have breast cancer, given that her X-ray examination was positive is about 15%
