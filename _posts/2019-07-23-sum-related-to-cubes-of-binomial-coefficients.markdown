---
layout: post
title: sum related to cubes of binomial coefficients
tags:
  - sum  
  - closed-form
  - binomial-coefficients
  - real-analysis
  
description:  
  sum related to cubes of binomial coefficients
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :


$$

\sum_{n=0}^{\infty}{\binom{2n}{n}^3\over 2^{6n}}={\pi\over \Gamma^4\left({3\over 4}\right)}

$$


<!–-break-–>


# Answer

use the standard evaluation

$$

\binom{2n}{n}\cdot{\pi\over 2^{2n}}=\int_{0}^{\pi}\cos^{2n}{u}\:\mathrm du\tag1

$$

 to deduce

$$

\sum_{n=0}^{\infty}{\binom{2n}{n}^3\over 2^{6n}}=\frac1{\pi^3}\cdot\int \!\int\!\int_{\large\left[0,\pi\right]^3}\frac{du\:d\nu\:dw}{1-\cos u \cos \nu \cos w} \tag2

$$

 the latter integral is one of [Watson's triple integrals][1] which have  been evaluated by Watson ("Three Triple Integrals." Quart. J. Math., Oxford Ser. 2 10, 266-276, 1939) using clever and elementary changes of variable (see [here][1]):

$$

\frac1{\pi^3}\cdot\int \!\int\!\int_{\large\left[0,\pi\right]^3}\frac{du\:d\nu\:dw}{1-\cos u \cos \nu \cos w} = {\Gamma^4\left({1\over 4}\right)\over 4\pi^3}={\pi\over \Gamma^4\left({3\over 4}\right)}.\tag3

$$



  [1]: http://mathworld.wolfram.com/WatsonsTripleIntegrals.html