---
layout: post
title: Problem related to sequences and series and harmonic numbers
tag:
 - sequences-and-series
 - inequality
 - harmonic-numbers

description: Problem related to sequences and series and harmonic numbers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Can one show that $$\sum_{n=1}^N\frac{1}{n} -\log N - \gamma \leqslant \frac{1}{2N}$$ without using the Euler-Maclaurin formula?

<!–-break-–>


we would like to prove that


$$


\sum_{n=1}^N\frac{1}{n} -\log N - \gamma \leqslant \frac{1}{2N}


$$


without using the Euler-Maclaurin summation formula. The motivation for this is that we have come very close to doing so (see the answer provided below) but annoyingly have not actually proved the above.
Some may ask why we don't just use the formula. we are  writing a set of analytic number theory notes for my own use and it seems an unwieldy result to introduce and prove, given that the above inequality is all we need, and given that we have gotten so close without using Euler-Maclaurin!
.

# Answer 


Let 


$$

\gamma_n = \sum_{k=1}^n \frac{1}{k} - \log n.

$$


Our goal is to show that


$$

\gamma_n - \lim_{m \to \infty} \gamma_m \leq \frac{1}{2n}.

$$


It is enough to show that, for $$n<m$$, we have


$$

\gamma_n - \gamma_m \leq \frac{1}{2n}.

$$


This has the advantage of dealing solely with finite quantities.
Now, 


$$

\gamma_n - \gamma_m = \int_{n}^m \frac{dt}{t} - \sum_{k=n+1}^m \frac{1}{k} =\sum_{j=n}^{m-1} \int_{j}^{j+1} \left( \frac{1}{t} - \frac{1}{j+1} \right) \cdot dt .

$$


At this point, if we were at a chalkboard rather than a keyboard, we would draw a picture. Draw the hyperbola $$y=1/x$$ and mark off the interval between $$x=n$$ and $$x=m$$. Divide this into $$m-n$$ vertical bars of width $$1$$. Each bar stretches up to touch the hyperbola at its right corner. There is a little wedge, bounded by $$x=j$$, $$y=1/(j+1)$$ and $$y=1/x$$. We are adding up the area of each of these wedges.1
Because $$y=1/x$$ is convex, the area of this wedge is less than that of the right triangle with vertices at $$(j,1/(j+1))$$, $$(j+1, 1/(j+1))$$ and $$(j,1/j)$$. This triangle has base $$1$$ and height $$1/j - 1/(j+1)$$, so its area is $$(1/2) (1/j - 1/(j+1))$$. So the quantity of interest is


$$

\leq \sum_{j=n}^{m-1} \frac{1}{2} \left( \frac{1}{j} - \frac{1}{j+1} \right) = \frac{1}{2} \left( \frac{1}{n} - \frac{1}{m} \right) \leq \frac{1}{2n}.

$$


Of course, this is just a standard proof of Euler-Maclaurin summation, but it is a lot more geometric and easy to follow in this special case.
1 By the way, since this area is positive, we also get the corollary that $$\gamma_n - \gamma_m > 0$$, so $$\gamma_n - \gamma >0$$, another useful bound.

