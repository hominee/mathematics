---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - integration
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Generalizing the trick for integrating $$\int_{-\infty}^\infty e^{-x^2}\mathrm dx$$?

<!–-break-–>


There is a well-known trick for integrating $$\int_{-\infty}^\infty e^{-x^2}\mathrm dx$$, which is to write it as $$\sqrt{\int_{-\infty}^\infty e^{-x^2}\mathrm dx\int_{-\infty}^\infty e^{-y^2}\mathrm dy}$$, which can then be reexpressed in polar coordinates as an easy integral.
 Is this trick a one-hit wonder, or are there other cases where this trick works and is also necessary? It seems to depend on the defining property of the exponential function that $$f(a+b)=f(a)f(b)$$, which would make me think that it would only allow fairly trivial generalizations, e.
g.
, to $$\int_{-\infty}^\infty 7^{-x^2}\mathrm dx$$ or $$\int_{-\infty}^\infty a^{bx^2+cx+d}\mathrm dx$$.

Can it be adapted through rotation in the complex plane to do integrals like $$\int_{-\infty}^\infty \sin(x^2)\mathrm dx$$? Here we find myself confused by trying to simultaneously visualize both the complex plane and the $$(x,y)$$ plane.

WP http://en.
wikipedia.
org/wiki/Gaussian_integral discusses integrals that have a similar form and seem to require different methods, but I'd be more interested in integrals that have different forms but can be conquered by the same trick.

The trick involves expanding from 1 dimension to 2.
 Is there a useful generalization where you expand from $$m$$ dimensions to $$n$$?
This is not homework.


# Answer 


we would like to answer to your question about Fresnel integral as we did this in my undergraduate studies. So, let us consider the integrals


$$

S_1=\int_{-\infty}^\infty dx\sin(x^2) \qquad C_1=\int_{-\infty}^\infty dx\cos(x^2).

$$


We want to apply the same technique used for Gauss integral in this case and consider the two-dimensional integrals


$$

S_2=\int_{-\infty}^\infty\int_{-\infty}^\infty dxdy\sin(x^2+y^2) \qquad C_2=\int_{-\infty}^\infty\int_{-\infty}^\infty dxdy\cos(x^2+y^2).

$$


If you go to polar coordinates, these integrals doe not converge. So, we introduce a convergence factor in the following way


$$

S_2(\epsilon)=\int_{-\infty}^\infty\int_{-\infty}^\infty dxdy e^{-\epsilon(x^2+y^2)}\sin(x^2+y^2)

$$

 


$$

C_2(\epsilon)=\int_{-\infty}^\infty\int_{-\infty}^\infty dxdy e^{-\epsilon(x^2+y^2)}\cos(x^2+y^2).

$$


Then one has, moving to polar coordinates,


$$

S_2(\epsilon)=2\pi\int_0^\infty \rho d\rho e^{-\epsilon\rho^2}\sin(\rho^2) \qquad C_2(\epsilon)=2\pi\int_0^\infty \rho d\rho e^{-\epsilon\rho^2}\cos(\rho^2)

$$


that is


$$

S_2(\epsilon)=\pi\int_0^\infty dx e^{-\epsilon x}\sin(x) \qquad C_2(\epsilon)=\pi\int_0^\infty dx e^{-\epsilon x}\cos(x).

$$


These integrals are well known and give


$$

S_2(\epsilon)=\frac{\pi}{1+\epsilon^2} \qquad C_2(\epsilon)=\frac{\epsilon\pi}{1+\epsilon^2}

$$


noting that integration variables are dummy. Now, in this case one can take the limit for $$\epsilon\rightarrow 0$$ producing


$$

S_2=\int_{-\infty}^\infty\int_{-\infty}^\infty dxdy\sin(x^2+y^2)=\pi \qquad C_2=\int_{-\infty}^\infty\int_{-\infty}^\infty dxdy\cos(x^2+y^2)=0

$$


By applying simple trigonometric formulas you will get back the value of the Fresnel integrals. But now, as a bonus, you have got the value of these integrals in two dimensions.

