---
layout: post
title: Problem related to definite integrals and bessel functions
tag:
 - definite-integrals
 - improper-integrals
 - bessel-functions

description: Problem related to definite integrals and bessel functions

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proof $$\int_0^\infty \frac{\exp(-\sqrt{x^2+y^2})}{x^2+y^2}dx = \frac{\pi}{2}\left(\frac{1}{y} - K_0(y)L_{-1}(y) - K_1(y)L_{0}(y)\right)$$

<!–-break-–>


In this topic the following integral was solved 


$$

\int_0^\infty \frac{\exp\left(-\sqrt{x^2+y^2}\right)}{x^2+y^2}dx = \frac{\pi}{2}\left(\frac{1}{y} - K_0(y)L_{-1}(y) - 
    K_1(y)L_{0}(y)\right).

$$


Sadly it is not shown how the integral was derived. It is mentioned that the result was found by rewriting the integral, taking the derivative of the integral and solving the resulting differential equation.
Has anybody an idea how this was achieved?
we are  trying to get an idea to solve a similar integral


$$

\int_0^\infty \frac{\exp\left(- \beta \sqrt{x^2+y^2}\right)}{x^2+y^2} \cos(b \, x) dx.
$$


**Edit**: $$L$$ seems to be the modified Struve functions and $$K$$ is the modified Bessel function of the second kind.

# Answer 


The proof for the first integral is given as follows:
Using the Fourier-Cosine-Transforms


$$

\frac{1}{x^2+y^2} \mapsto \frac{\pi}{y}\mathrm{e}^{-s\,y}

$$




$$

\exp\left(-\sqrt{x^2+y^2}\right) \mapsto \frac{y}{\sqrt{s^2+1}} \, \mathrm{K}_1(y \, \sqrt{s^2+1})

$$


results in the integral


$$

\int_{s=0}^\infty \frac{\pi}{\sqrt{s^2+1}}\mathrm{e}^{-s\,y} \, \mathrm{K}_1(y \, \sqrt{s^2+1}) ds

$$


Using the integral representation of the Bessel function


$$

\mathrm{K}_1(y \, \sqrt{s^2+1})=\frac{1}{4} \,y \, \sqrt{s^2+1} \int_{t=0}^\infty \mathrm{e}^{-t-\frac{y^2 \, (s^2+1)}{4 \,t}} \frac{1}{t^2} dt

$$


and changing the order of integration leads to


$$

\int_{t=0}^\infty \int_{s=0}^\infty \frac{\pi\,y}{4}\mathrm{e}^{-s\,y} \, \mathrm{e}^{-t-\frac{y^2 \, (s^2+1)}{4 \,t}} \frac{1}{t^2} \, ds \, dt

$$


Integration with respect to s gives


$$

\int_{t=0}^\infty \, \mathrm{e}^{-\frac{y^2}{4t}}\,\frac{\pi^{3/2}}{4\,t^{3/2}}\, (1-\mathrm{erf}(\sqrt{t}))dt

$$


Splitting the integral gives


$$

\int_{t=0}^\infty \, \mathrm{e}^{-\frac{y^2}{4t}}\,\frac{\pi^{3/2}}{4\,t^{3/2}}\, dt = \frac{\pi^2}{2} \, \frac{1}{y}

$$




$$

\int_{t=0}^\infty \, -\mathrm{e}^{-\frac{y^2}{4t}}\,\frac{\pi^{3/2}}{4\,t^{3/2}}\, \mathrm{erf}(\sqrt{t})dt = -\frac{\pi^2}{2} \left [K_0(y) \mathbf{L}_{-1}(y) + K_1(y) \mathbf{L}_{0}(y)\right]

$$


The last integral was proven here.
Sadly this still does not help me with my problem, since it does not work for the integral including cos$$(b\,x)$$.

