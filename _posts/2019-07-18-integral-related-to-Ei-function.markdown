---
layout: post
title: integral related to Ei function
tags:
  - integral 
  - closed-form
  - Ei-function
  - real-analysis
  
description:  
  integral related to Ei function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$

\int_{-\infty}^0\operatorname{Ei}^3x\,dx

$$


<!–-break-–>

Let $$\operatorname{Ei}x$$ denote the [exponential integral](http://mathworld.wolfram.com/ExponentialIntegral.html):

$$
\operatorname{Ei}x=-\int_{-x}^\infty\frac{e^{-t}}tdt.\tag1
$$

It's not difficult to find that

$$
\int\operatorname{Ei}x\,dx=x\,\operatorname{Ei}x-e^x,\tag2
$$


$$
\int\operatorname{Ei}^2x\,dx=x\,\operatorname{Ei}^2x-2\,e^x\operatorname{Ei}x+2\,\operatorname{Ei}(2x)\tag3
$$

and

$$
\int_{-\infty}^0\operatorname{Ei}x\,dx=-1,\tag4
$$


$$
\int_{-\infty}^0\operatorname{Ei}^2x\,dx=\ln4.\tag5
$$


---
Is it possible generalize these results for higher powers of $$\operatorname{Ei}x$$?  
In particular, are there closed forms for

$$
\int\operatorname{Ei}^3x\,dx\tag6
$$

or

$$
\int_{-\infty}^0\operatorname{Ei}^3x\,dx\ ?\tag7
$$



# Answer

First note that 
$$
\int_{-\infty}^{0} \text{Ei}^{3}(x) \ dx = -\int_{0}^{\infty} \text{E}_{1}^{3}(x) \ dx. 
$$


Then integrating by parts,


$$
 - \int_{0}^{\infty} \text{E}_{1}^{3}(x) \ dx = -x \text{E}_{1}^{3}(x) \Big|^{\infty}_{0} - 3 \int^{\infty}_{0} \text{E}_{1}^{3}(x) e^{-x} \ dx. 
$$


Since $$E_{1}(x)$$ behaves like $$-\log x$$ near $$x=0$$ and $$ \displaystyle\frac{e^{-x}}{x}$$ near $$\infty$$,  the boundary terms vanish.

And


$$
 \begin{align*} \int_{0}^{\infty} \text{E}_{1}(x) \text{E}_{1}(x) e^{-x} \ dx  &= \int_{0}^{\infty} \int_{1}^{\infty} \int_{1}^{\infty} \frac{e^{-xy}}{y} \frac{e^{-xz}}{z} e^{-x} \ dy \ dz \ dx \\ &= \int_{1}^{\infty} \int_{1}^{\infty} \int_{0}^{\infty} \frac{1}{yz} e^{-(y+z+1)x} \ dx \ dy \ dz \\ &= \int_{1}^{\infty} \int_{1}^{\infty} \frac{1}{yz} \frac{1}{y+z+1} \ dy \ dz \\ &= \int_{1}^{\infty} \int_{1}^{\infty} \frac{1}{z} \frac{1}{1+z} \left( \frac{1}{y} - \frac{1}{y+z+1} \right) \ dy \ dz \\ &= \int_{1}^{\infty} \frac{\log(z+2)}{z(1+z)} \ dz \\ &=  \log 2 \int_{1}^{\infty} \left( \frac{1}{z} - \frac{1}{1+z} \right) \ dz + \lim_{b \to \infty} \Bigg( \int_{1}^{b}  \frac{\log (1+ \frac{z}{2})}{z} \ dz  \\ &- \int_{1}^{b} \frac{\log (1+ \frac{z}{2})}{1+z}  \ dz \Bigg) \\ &= \log^{2}(2) + \lim_{b \to \infty} \left[- \text{Li}_{2} \left(-\frac{z}{2} \right) \Big|^{b}_{1} - \int_{1}^{b} \frac{\log(1+ \frac{z}{2})}{1+z} \ dz \right] \end{align*}
$$


where


$$
 \begin{align*} \int \frac{\log(1+ \frac{z}{2})}{1+z} \ dz &= \int \frac{\log (1+u)}{u} \ du - \log (2) \int\frac{1}{u} \ du \\ &= - \text{Li}_{2}(-u) - \log(2) \log u +C 
\\ &= - \text{Li}_{2}(-z-1) - \log(2) \log(z+1) + C. \end{align*}
$$


Therefore,


$$
 \begin{align*} \int_{-\infty}^{0} \text{Ei}^{3}(x) \ dx &= - 3 \log^{2}(2) - 3 \text{Li}_{2} \left(- \frac{1}{2} \right)  + 3 \text{Li}_{2}(-2) + 3 \log^{2}(2) \\  & + 3 \lim_{b \to \infty} \left[\text{Li}_{2} \left(-\frac{b}{2} \right) - \text{Li}_{2}(-b-1)  - \log(2) \log(b+1) \right] \\ &= -3 \text{Li}_{2} \left(- \frac{1}{2} \right)  + 3 \text{Li}_{2}(-2) - \frac{3 \log^{2}(2)}{2} \\ &\approx -3.68568. \end{align*}
$$


That limit can be evaluated by hand by using the inversion formula for the dilogarithm.

*See the second edit for a better way to evaluate that log integral.

---

**EDIT**:

As Lucian pointed out in the comments, the answer can be simplified using the inversion formula.

Specifically,


$$
 \int_{-\infty}^{0} \text{Ei}(x)^{3} \ dx= - \frac{\pi^{2}}{2} - 3 \log^{2}(2) - 6 \text{Li}_{2} \left( -\frac{1}{2}\right).
$$


Wolfram Alpha states than an alternative form of the expression on the right is 
$$
-3 \text{Li}_{2} \left(\frac{1}{4} \right) - 6 \log^{2}(2). 
$$


---

**SECOND EDIT**:

A better way to evaluate 
$$
\int_{1}^{\infty} \frac{\log(z+2)}{z(1+z)} \, dz
$$
 is to make the substitution $$u = \frac{1}{z}$$.

Then 
$$
 \int_{1}^{\infty} \frac{\log(z+2)}{z(1+z)} \, dz = \int_{0}^{1} \frac{\log(1+2u)}{1+u} \, du - \int_{0}^{1} \frac{\log(u)}{1+u} \, du
$$


where


$$
 \begin{align*} \int_{0}^{1} \frac{\log(1+2u)}{1+u} \, du &= \log(1+2u) \log(2+2u)\Bigg|_{0}^{1} - 2\int_{0}^{1} \frac{\log(2+2u)}{1+2u} \, du \\ &= \log(3) \log(4)- \int_{0}^{2}\frac{\log(2+v)}{1+v} \ dv \\ &= \log(3) \log(4) - \int_{1}^{3} \frac{\log(1+w)}{w} \ dw \\ &=\log(3) \log(4) + \text{Li}_{2}(-3) -\text{Li}_{2}(-1) \\ &= 2\log(3) \log(2) + \text{Li}_{2}(-3) + \frac{\pi^{2}}{12} \end{align*}
$$


and


$$
 \int_{0}^{1} \frac{\log(1+u)}{u} \, du = -\frac{\pi^{2}}{12}.
$$


So we get the equivalent answer


$$
\int_{-\infty}^{0} \text{Ei}^{3}(x) \, dx = -6 \log(3) \log(2)  -3 \text{Li}_{2}(-3) - \frac{\pi^{2}}{2} \approx -3.68568 .
$$
