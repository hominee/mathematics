---
layout: post
title: Problem related to calculus and riemann zeta
tag:
 - calculus
 - real-analysis
 - sequences-and-series
 - complex-analysis
 - riemann-zeta

description: Problem related to calculus and riemann zeta

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Nice proofs of $$\zeta(4) = \frac{\pi^4}{90}$$?

<!–-break-–>


we know some nice ways to prove that $$\zeta(2) = \sum_{n=1}^{\infty} \frac{1}{n^2} = \pi^2/6$$.  For example, see Robin Chapman's list or the answers to the question "Different methods to compute $$\sum_{n=1}^{\infty} \frac{1}{n^2}$$?"
Are there any nice ways to prove that 

$$

\zeta(4) = \sum_{n=1}^{\infty} \frac{1}{n^4} = \frac{\pi^4}{90}?

$$


we already know some proofs that give all values of $$\zeta(n)$$ for positive even integers $$n$$ (like #7 on Robin Chapman's list or Qiaochu Yuan's answer in the linked question).  we are  not so much interested in those kinds of proofs as we are  those that are specifically for $$\zeta(4)$$.
we would be particularly interested in a proof that isn't an adaption of one that $$\zeta(2) = \pi^2/6$$.

# Answer 


In the same spirit of the 1st proof of this answer. If we substitute  $$\pi $$ for $$ x $$ in the Fourier trigonometric series expansion of $$%
f(x)=x^{4}$$, with $$-\pi \leq x\leq \pi $$, 


$$

x^{4}=\frac{1}{5}\pi ^{4}+\sum_{n=1}^{\infty }\frac{8n^{2}\pi ^{2}-48}{n^{4}}\cos n\pi \cdot \cos nx,

$$


we obtain


$$

\begin{eqnarray*}
\pi ^{4} &=&\frac{1}{5}\pi ^{4}+\sum_{n=1}^{\infty }\frac{8n^{2}\pi ^{2}-48}{n^{4}}\cos ^{2}n\pi  \\
 &=&\frac{1}{5}\pi ^{4}+8\pi ^{2}\sum_{n=1}^{\infty }\frac{1}{n^{2}}
-48\sum_{n=1}^{\infty }\frac{1}{n^{4}}.
\end{eqnarray*}

$$


Hence


$$

\sum_{n=1}^{\infty }\frac{1}{n^{4}}=\frac{\pi ^{4}}{48}\left( -1+\frac{1}{5}+
\frac{8}{6}\right) =\frac{\pi ^{4}}{48}\cdot \frac{8}{15}=\frac{1}{90}\pi
^{4}.

$$



