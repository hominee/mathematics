---
layout: post
title: Closed form of Li integral 
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
description: >
  Closed form of Li integral
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Prove that

$$
 \int_0^1\frac{\operatorname{Li}_3(1-z)}{\sqrt{z(1-z)}}\mathrm dz=-\frac{\pi^3}{3}\log 2+\frac{4\pi}3\log^3 2+2\pi\zeta(3)
$$

<!–-break-–>

# Answer

Using the well-known identity:

$$
\begin{equation*}
\rm{Li}_3 (\frac{-x}{1-x}) + \rm{Li}_3 (1-x) + \rm{Li}_3 (x) = \zeta(3) + \frac{\pi ^2}{6} \ln(1-x) -\frac{1}{2} \ln(x)\ln^2 (1-x) + \frac{1}{6} \ln^3 (1-x)
\end{equation*}
$$

we obtain (the integral on RHS can be easily evaluated by differentiating beta function): 

$$
2\int_0 ^1 \frac{\rm{Li}_3 (1-x)}{ \sqrt{x(1-x)}} dx + \int _0 ^1 \frac{\rm{Li}_3 (\frac{-x}{1-x})}{ \sqrt{x(1-x)}} dx = -2 \pi \zeta(3) + \frac{8}{3} \pi \ln^3 (2) - \frac{2}{3}\pi ^3 \ln(2)
$$

By transformation $$u=x/(1-x)$, we have

$$
\int_0^1 \frac{\rm{Li}_3 (\frac{-x}{1-x})}{ \sqrt{x(1-x)}} dx = \int _0 ^\infty \frac{\rm{Li}_3 (-u)}{(1+u)\sqrt{u}} du
$$

I claim this integral is $$-6\pi \zeta(3)$$.

----------------------

To establish this value, it suffices to show, with $$\zeta(\cdot,\cdot)$$ [Hurwitz zeta function][1], 

$$
\int_0^\infty \frac{\rm{Li}_3 (-x)}{1+x} x^{s-1} = \frac{\pi}{\sin(\pi s)} [\zeta(3) -\zeta(3,1-s)] \qquad 0<s<1
$$

by [Mellin inversion theorem][2], this in turn is equivalent to, (which applies as the function tends to $$0$$ uniformly in the vertical strip  $$0<\Re(s)<1$$ thanks to the $\csc(s\pi)$ factor) for an instance of $$c$$ with $$0<c<1$$:

$$
\tag{1} \frac{\rm{Li} _3 (-x)}{1 + x} = \frac{1}{2\pi i} \int_{c - i\infty }^{c + i\infty } \frac{\pi x^{ - s}}{\sin (\pi s)}\left[ {\zeta (3) - \zeta (3,1 - s)} \right]ds \qquad x>0
$$

Note that both sides of $$(1)$$ is an analytic function for $$\Re(x) > 0$$ hence it suffices to consider the case when $$0<x<1$$. When this is the case, we can draw a vertical semicircle on the left half-plane, with vertices $$c \pm i\infty$$ then the integral on the semicircle tends to $$0$$ calculating residues at $$-1,-2,\cdots$$ gives

$$
\begin{aligned}
\frac{1}{2\pi i} \int_{c - i\infty } ^{c + i\infty } \frac{\pi x^{ - s}}{\sin (\pi s)} \left[ \zeta (3) - \zeta (3,1 - s) \right] ds
 &= \sum\limits_{n = 1}^\infty  (-x)^n \left[ \zeta (3) - \zeta (3,1 + n) \right] \\ 
 &=\sum\limits_{n = 1}^\infty  (-x)^n \sum\limits_{k = 1} ^n \frac{1}{k^3}  
 = \frac{\rm{Li}_3 (-x)}{1+x}
\end{aligned}
$$

where we exchanged two order of summations, completing the proof.


  [1]: https://en.wikipedia.org/wiki/Hurwitz_zeta_function
  [2]: https://en.wikipedia.org/wiki/Mellin_inversion_theorem