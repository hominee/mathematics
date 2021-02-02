---
layout: post
title: Problem related to sequences and series and zeta functions
tag:
 - sequences-and-series
 - zeta-functions

description: Problem related to sequences and series and zeta functions

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proving that $$\sum\limits_{n=2}^{\infty }\frac{\zeta (n)}{2^{n-1}}=\log(4)$$

<!–-break-–>





$$

\frac{\zeta (2)}{2}+\frac{\zeta (3)}{2^2}+\frac{\zeta (4)}{2^3}+\frac{\zeta (5)}{2^4}+.
.
.
=\log(4)

$$



we tried to prove it, but the problem with the odd zeta terms so that we don't have a function   which deals with odd terms.
we used the WolframAlpha but it couldn't recognize the calculated value is $$\log(4)$$.


# Answer 




**Note** that 

$$

\sum_{k\geqslant2}\frac{\zeta(k)}{2^{k-1}}=\sum_{k\geqslant2}\sum_{n\geqslant1}\frac{1}{n^k2^{k-1}}=\sum_{n\geqslant1}\frac1n\sum_{k\geqslant2}\frac{1}{(2n)^{k-1}}=\sum_{n\geqslant1}\frac1n\frac1{2n}\frac1{1-\frac1{2n}},

$$

 hence 

$$

\sum_{k\geqslant2}\frac{\zeta(k)}{2^{k-1}}=\sum_{n\geqslant1}\frac2{2n(2n-1)}=2\sum_{n\geqslant1}\frac1{2n-1}-\frac1{2n}=2\sum_{i\geqslant1}\frac{(-1)^{i-1}}i=2\log2.

$$

 Which is exactly one of the approaches explained to you à propos your former question (do you study the answers you receive, to understand them?).


**Edit**: More generally, for every integer $$\ell\geqslant2$$, 

$$

\sum_{k\geqslant2}\frac{\zeta(k)}{\ell^{k-1}}=\sum_z(1-z)\log(1-z),

$$

 where the sum in the RHS is over every $$\ell$$th root of unity $$z\ne1$$. For example, 

$$

\sum_{k\geqslant2}\frac{\zeta(k)}{3^{k-1}}=\frac32\log3-\sqrt3\frac\pi6\approx0.741,

$$

 and 

$$

\sum_{k\geqslant2}\frac{\zeta(k)}{4^{k-1}}=3\log2-\frac\pi2\approx0.509.

$$



