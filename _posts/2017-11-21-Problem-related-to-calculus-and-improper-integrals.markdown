---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - definite-integrals
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Evaluating $$\int\limits_0^\infty \frac{e^x}{1+e^{2x}}\mathrm dx$$, alternate methods

<!–-break-–>


Problem:
Evaluate 

$$

\displaystyle\int\limits_0^\infty \frac{e^x}{1+e^{2x}}\mathrm dx

$$


My progress: 
we have actually solved the problem, but we fear that we may not have used the "desired" methods.

Using substitution $$u = e^x$$, we can rewrite the integral and get 

$$

 \arctan(e^x)\bigg\|_0^\infty 

$$


Then we need to evaluate the limit 

$$

\displaystyle\left(\lim\limits_{x\to\infty}\arctan(e^x)\right) - \arctan(e^0)

$$


Now, this is where we think my solution differs from the intended method (which we don't know what is).

When we evaluate the above limit, we realize that $$\tan(x)$$ has a vertical asymptote for $$x = \frac\pi2$$, which means that $$\arctan(x)$$ has a horizontal asymptote for $$y = \frac\pi2$$, and is continuously increasing.

Then, since $$x\to\infty \Rightarrow e^x\to\infty$$, we can conclude that 

$$

\displaystyle\lim\limits_{x\to\infty}\arctan(e^x) = \frac\pi2

$$

 which gives the final answer 

$$

\displaystyle\int\limits_0^\infty \frac{e^x}{1+e^{2x}}\mathrm dx = \left(\lim\limits_{x\to\infty}\arctan(e^x)\right) - \arctan(e^0) = \frac\pi2 - \frac\pi4 = \underline{\underline{\frac\pi4}}

$$


My question:
Is there a more "calculating" way of evaluating the aforementioned limit? I.
e.
 using some general rules of limits rather than intuition? Bear in mind, we like my own solution.
 It was satisfying.
 we just feel like there is something else we should know, which we are  missing out on.


# Answer 


If you want to avoid the limit to infinity, you can use the change of variable $$e^x=1/u$$ instead, and get

$$

\int_0^\infty\frac{e^x}{1+e^{2x}}dx=\int_1^0\frac{-\frac{du}{u^2}}{1+\frac1{u^2}}=-\int_1^0\frac{du}{1+u^2}=-\arctan(u)\Big\|_1^0=\frac\pi4.

$$



