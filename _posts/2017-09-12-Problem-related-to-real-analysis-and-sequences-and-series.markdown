---
layout: post
title: Problem related to real analysis and sequences and series
tag:
 - real-analysis
 - sequences-and-series

description: Problem related to real analysis and sequences and series

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Evaluate:: $$ 2 \sum_{n=1}^\infty \frac{(-1)^{n+1}}{n+1}\left( 1 + \frac12 +\cdots + \frac 1n\right) $$

<!–-break-–>


How to evaluate the series:


$$

  2 \sum_{n=1}^\infty \frac{(-1)^{n+1}}{n+1}\left( 1 + \frac12 + \cdots + \frac 1n\right) 

$$


According to Mathematica, this converges to $$ (\log 2)^2 $$.

# Answer 


Recall that, formally,


$$


\left(\sum_{n=1}^{\infty} a_n\right)\left(\sum_{n=1}^{\infty} b_n\right) = \sum_{n=1}^{\infty} c_{n+1},

$$


where


$$


c_n = \sum_{k=1}^{n-1} a_k b_{n-k}.


$$


If the series $$\sum c_{n+1}$$ converges, then the above equality is actually true.  You seem to know how to show this, so I'll just demonstrate the formal aspect of the problem.
Let $$a_n = b_n = \frac{(-1)^{n}}{n}$$.  Then


$$


a_k b_{n-k} = \frac{(-1)^n}{k(n-k)} = \frac{(-1)^n}{n}\left(\frac{1}{k}+\frac{1}{n-k}\right),


$$


so that


$$


\begin{align*}
c_n &= \frac{(-1)^n}{n} \sum_{k=1}^{n-1} \left(\frac{1}{k}+\frac{1}{n-k}\right) \\
&= 2\frac{(-1)^n}{n} \sum_{k=1}^{n-1} \frac{1}{k}.
\end{align*}


$$


We therefore have


$$


2 \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n+1} \sum_{k=1}^{n} \frac{1}{k} = \left(\sum_{n=1}^{\infty} \frac{(-1)^n}{n}\right)^2 = (-\log 2)^2 = (\log 2)^2.


$$



