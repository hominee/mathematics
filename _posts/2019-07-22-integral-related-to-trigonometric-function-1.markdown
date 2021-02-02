---
layout: post
title: integral related to trigonometric function 1
tags:
  - integral  
  - closed-form
  - trigonometric-function
  - real-analysis
  
description:  
  integral related to trigonometric function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Integral of :

$$

\int_{-\infty}^{+\infty}{\mathrm dx\over x^2}\cdot\left(2-{\sin x\over \sin\left({x\over 2}\right)}\right)^{n+1}={2n\choose n}\pi

$$


 
<!–-break-–>


# Answer

The given integral equals

$$
 I(n) = 2^{n+1}\int_{\mathbb{R}}\frac{(1-\cos(x/2))^{n+1}}{x^2}\,dx = 2^n\int_{\mathbb{R}}\frac{(1-\cos z)^{n+1}}{z^2}\,dz \tag{1}
$$

or:

$$
 I(n) = 2^{2n+2}\int_{0}^{+\infty}\frac{\sin^{2n+2}(z/2)}{z^2}\,dz = 4^n\int_{\mathbb{R}}\frac{\sin^{2n+2}(z)}{z^2}\,dz \tag{2} 
$$

that can be computed through the Fourier cosine series of $$\sin^{2n+2}(z)$$, since

$$
 \int_{\mathbb{R}}\frac{1-\cos(mx)}{x^2}\,dx = m\pi.\tag{3}
$$

In particular, since $$\sin(z)=\frac{e^{iz}-e^{-iz}}{2i}$$,

$$
 \sin^{2n+2}(z) = \frac{1}{(2i)^{2n+2}}\sum_{k=0}^{2n+2}\binom{2n+2}{k}\exp\left((2k-2n-2)iz\right)(-1)^{k} \tag{4}
$$

equals:

$$
 \frac{1}{(2i)^{2n+2}}\sum_{k=1}^{n+1}\binom{2n+2}{n+1+k}\left(1-\cos(kz)\right)(-1)^k \tag{5} 
$$

and the problem boils down to the computation of the combinatorial sum

$$
 \sum_{k=1}^{n+1}\binom{2n+2}{n+1+k}k(-1)^k \tag{6}
$$

that is pretty simple. As an alternative, once we reach $$(2)$$ we may directly invoke [Lagrange's inversion theorem][1] and Cauchy's integral formula to derive that the answer is directly related with the coefficients of the Taylor series of $$\arcsin(z)$$ at the origin.


  [1]: https://en.wikipedia.org/wiki/Lagrange_inversion_theorem