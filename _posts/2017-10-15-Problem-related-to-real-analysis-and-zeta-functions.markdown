---
layout: post
title: Problem related to real analysis and zeta functions
tag:
 - real-analysis
 - sequences-and-series
 - complex-analysis
 - zeta-functions

description: Problem related to real analysis and zeta functions

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to prove that $$\frac{\zeta(2) }{2}+\frac{\zeta (4)}{2^3}+\frac{\zeta (6)}{2^5}+\frac{\zeta (8)}{2^7}+\cdots=1$$?

<!–-break-–>


How can one prove this identity? 



$$

\frac{\zeta(2) }{2}+\frac{\zeta (4)}{2^3}+\frac{\zeta (6)}{2^5}+\frac{\zeta (8)}{2^7}+\cdots=1

$$




There is a formula for $$\zeta$$ values at even integers, but it involves Bernoulli numbers; simply plugging it in does not appear to be an efficient approach.


# Answer 


Since


$$

\zeta(2n) = \frac{1}{(2n-1)!}\int_{0}^{+\infty}\frac{x^{2n-1}}{e^x-1}\,dx 

$$


we have:


$$

\sum_{n=1}^{+\infty}\frac{\zeta(2n)}{2^{2n-1}} = \int_{0}^{+\infty}\frac{\sinh(x/2)}{e^x-1}\,dx =\frac{1}{2}\int_{0}^{+\infty}e^{-x/2}\,dx = \color{red}{1}.

$$



