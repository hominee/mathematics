---
layout: post
title: integral related to floor function 3
tags:
  - integration   
  - definite-integrals
  - closed-form
  - floor-integral
  - real-analysis
  
description:  
  integral related to floor function 3
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$
\int_{0}^{1}\frac{dx}{\left\lfloor 1-\log_2 x\right\rfloor}
$$


<!–-break-–>


# Answer

The integrand function is constant on a sequence of intervals, in particular:

$$
I=\int_{0}^{1}\frac{dx}{\left\lfloor 1-\log_2 x\right\rfloor}=\sum_{n=1}^{+\infty}\frac{2^{1-n}-2^{-n}}{n}
=\sum_{n=1}^{\infty}\frac{2^{-n}}{n}=\log 2.
$$