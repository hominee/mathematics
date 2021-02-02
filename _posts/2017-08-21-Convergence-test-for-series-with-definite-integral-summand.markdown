---
layout: post
title: Convergence test for series with definite integral summand
tag:
 - real-analysis
 - sequences-and-series

description: Convergence test for series with definite integral summand

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Convergence test for series with definite integral summand

<!–-break-–>


we  was asked by a friend this problem: Show whether the series

 $$ 
\sum_{n = 1}^{\infty} \int_{0}^{1 / \sqrt{n}} \frac{\mathrm{e}^{x} - 1}{1 + x} \mathop{}\!\mathrm{d} x
 $$ 

converges.
Now the integral does not have a closed form, and the summand evidently vanishes as $$n \to \infty$$. we 've tried to apply all convergence tests that we  could find, but none seem to work in this case. Many of them (d'Alembert, Dirichlet, etc.) try to evaluate $$\displaystyle \frac{a_{n + 1}}{a_{n}}$$ and then do something about it, but in this case, when the summand is a definite integral, this fraction doesn't seem to simply things much... Nor does it seem to simply things to evaluate the square root $$\sqrt{\lvert a_{n}\rvert}$$ or the integral $$\displaystyle \int_{1}^{\infty} a_{n} \mathop{}\!\mathrm{d} n$$. The Cauchy condensation test evaluates $$2^{n} a_{2^{n}}$$, which also doesn't seem to lead anywhere...
we  think the reason the aforementioned tests don't seem to work (based on my trial anyway...maybe they do and we are  just not seeing it) is that the summand is an integral. Hence we  was wondering if there is a convergence test which works for series with definite integral summand?
Edit: As Jack pointed out below, there is no need for a test specifically for series with integral summand. (we t's techniques and tricks combined with available tests)
.

# Answer 


For $$n >0$$ , we have 
 $$ 
0\le x \le1
 $$ 

thus

 $$ 
e^x-1\ge x 
 $$ 

and

 $$ 
\frac {1}{1+x}\geq \frac {1}{2}. 
 $$ 

from this

 $$ 
\int_0^\frac {1}{\sqrt {n}}\frac {e^x-1}{1+x}dx\geq \frac {1}{2}\Bigl [\frac {x^2}{2}\Bigr]_0^\frac {1}{\sqrt {n}} 
 $$ 


 $$ 
\geq \frac {1}{4n} 
 $$ 

the series is Divergent.

