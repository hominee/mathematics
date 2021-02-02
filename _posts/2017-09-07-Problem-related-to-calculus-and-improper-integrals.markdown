---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - integration
 - definite-integrals
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What is the value of the integral$$\int_{0}^{+\infty} \frac{1-\cos t}{t} \, e^{-t} \, \mathrm{d}t$$?

<!–-break-–>


we have a question about evaluating



$$

\int_{0}^{\infty} \frac{1-\cos t}{t}  \, e^{-t} \, \mathrm{d} t

$$




Since $$\lim_{t \to 0} \frac{1-\cos(t)}{t}  =0$$, we know that the integrand is integrable near $$t=0$$.
But when evaluating the integral, how do you deal with the $$t$$ in the denominator of the integrand?
.

# Answer 


Consider


$$

\mathcal{I}(a)=\int_0^{\infty}\frac{1-\cos at}{t}e^{-t}dt.

$$


Differentiating w.r.t. $$a$$, we find


$$

\mathcal{I}'(a)=\int_0^{\infty}\sin at\;e^{-t}dt=\frac{a}{1+a^2}.

$$


Now integrating back and using that $$\mathcal{I}(0)=0$$ yields


$$

\mathcal{I}(a)=\int_0^a\frac{a\,da}{1+a^2}=\frac12\ln\left(1+a^2\right).

$$


It remains to set $$a=1$$.

