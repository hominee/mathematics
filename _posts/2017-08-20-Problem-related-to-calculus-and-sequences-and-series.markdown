---
layout: post
title: Problem related to calculus and sequences and series
tag:
 - calculus
 - sequences-and-series

description: Problem related to calculus and sequences and series

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Does the series $$\sum \limits_{n=2}^{\infty }\frac{n^{\log n}}{(\log n)^{n}}$$ converge?

<!–-break-–>


we are  trying  to find out now whether the series
$$\sum_{n=2}^{\infty } a_{n}$$ converges or not when

 $$ 
a_n = \frac{n^{\log n}}{(\log n)^{n}}
 $$ 

Again, we  tried d'Alembert $$\frac{a_{n+1}}{a_{n}}$$,   Cauchy condensation test $$\sum \limits_{n=2}^{\infty } 2^{n}a_{2^n}$$, and they both didn't work for me.
we  can't use Stirling, nor the integral test.
Edit: we are  searching for a solution which uses sequences theorems and doesn't involve functions.

# Answer 


A comparison test will work here; the key is to write both numerator and denominator in terms of exponentials with bases not involving $$n$$.  Note that the numerator is $$e^{\log^2 n}$$, which is less than $$e^{n/2}$$ for sufficiently large $$n$$.  The denominator is $$e^{n \log \log n}$$, which is greater than $$e^n$$ for sufficiently large $$n$$; so for all sufficiently large $$n$$ the terms are less than $$e^{-n/2}$$ and thus the series converges.

