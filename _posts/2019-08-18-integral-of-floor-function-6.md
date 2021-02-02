---
layout: post
title: integral related to floor function 6
tags:
  - integration   
  - definite-integrals
  - closed-form
  - floor-integral
  - real-analysis
  
description:  
  integral related to floor function 6
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$
\int \left \lfloor\frac{1}{x}\right\rfloor \mathrm{d}x
$$


<!–-break-–>


# Answer

The function:

$$
\left\lfloor\frac{1}{x}\right\rfloor
$$

is equal to $$n$$ on the interval $$\left(\frac{1}{n+1},\frac{1}{n}\right)$$,so if we try to determine the 
integral from $$t>0$$ to $$1$$, we can let $$n=\left\lfloor\frac{1}{t}\right\rfloor$$ and we have constant
 value $$1$$ on range $$(\frac{1}{2},1)$$, constant value $$2$$ on range $$(\frac{1}{3},\frac{1}{2})$$, etc. 
 So since $$t<\frac{1}{n}$$, we get terms for each interval $$(\frac{1}{k+1},\frac{1}{k})$$ when $$k<n.$$  
 The length of the $$k$$th interval is $$\frac{1}{k(k+1)}$$ and the value of the function is $$k$$ on this 
 interval, so the integral on this interval is $$\frac{1}{k+1}$$.  So the integral from $\frac{1}{n}$ to $$1$$
 is $$1/2 + 1/3 + 1/4 + ... + 1/n$$.  Then then integral from $$t$$ to $$\frac{1}{n}$$ is the length of the 
 interval times $$n$$, which is $$n(\frac{1}{n} - t) = 1-nt$$.  So the total is:

$$
\int_t^1 \,\left\lfloor\frac{1}{x}\right\rfloor\, dx = 1 - t{\left\lfloor\frac{1}{t}\right\rfloor} + 
\sum_{i=2}^{\left\lfloor\frac{1}{t}\right\rfloor}\frac{1}{i}
$$

The indefinite integral, then, is the opposite of this:

$$
x\left\lfloor\frac{1}{x}\right\rfloor - \sum_{i=2}^{\left\lfloor\frac{1}{x}\right\rfloor}\frac{1}{i} + C
$$