---
layout: post
title: Potentially Useful Question 
tag:
 - sequences-and-series

description: Potentially Useful Question 

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Potentially Useful Question

<!–-break-–>

 i want to solve for: 
$$\sum_{n=1}^{\infty} \dfrac{1}{n^4} =$$ ?
On my formula sheet i have:
$$\sum_{n=1}^{\infty} \dfrac{1}{n^2} = \dfrac{\pi^2}{6}$$
Which looks similar to what i want, but not quite. Might someone guide me towards the solution (or provide the solution with explanation? 
.

# Answer 


This is just a sketch of one of many possible proofs.
Step1. Prove that over the interval $$[0,2\pi]$$, the function:


$$

f(x)=\sum_{n=1}^{+\infty}\frac{\cos(nx)}{n^2}

$$


is a second degree-polynomial whose graphics passes through the points:


$$

(0,\pi^2/6),\quad (\pi,-\pi^2/12),\quad (2\pi,\pi^2/6).

$$


Step2. Deduce from Lagrange interpolation that:


$$

 f(x) = \frac{\pi^2}{6}-\frac{x(2\pi-x)}{4}.

$$


Step3. Apply Parseval's identity to $$f(x)$$:


$$

\int_{0}^{2\pi}f(x)^2\,dx = \pi\sum_{n=1}^{+\infty}\frac{1}{n^4}.

$$


Step4. Prove, through the second step, that:


$$

\int_{0}^{2\pi}f(x)^2\, dx = \frac{\pi^5}{90}.

$$


Conclusion:



$$

\zeta(4)=\sum_{n=1}^{+\infty}\frac{1}{n^4} = \frac{\pi^4}{90}.

$$




