---
layout: post
title: Problem related to complex analysis and contour integration
tag:
 - complex-analysis
 - integration
 - improper-integrals
 - contour-integration

description: Problem related to complex analysis and contour integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Evaluating $$\int_0^\infty \frac{\cos(ax)-e^{-ax}}{x \left(x^4+b^4 \right)}dx$$

<!–-break-–>


How can we evaluate 


$$

\int_0^\infty \frac{\cos(ax)-e^{-ax}}{x \left(x^4+b^4\right)}dx \quad a,b>0

$$


using Complex Analysis? This problem was given in a Complex Analysis book which we was reading.
 The answer given in it is


$$

\frac{\pi}{4b^4}e^{-ab/\sqrt{2}}\sin \left(\frac{ab}{\sqrt{2}} \right)

$$


Which function and contour should we consider?
.


# Answer 


Consider the integral


$$

\oint_C dz \frac{e^{i a z}-e^{-a z}}{z (z^4+b^4)}

$$


where $$C$$ is a quarter circle of radius $$R$$ in the first quadrant of the complex plane.  (That is, $$\Re{z} > 0$$, $$\Im{z}>0$$.)  This integral is equal to


$$

\int_0^R dx \frac{e^{i a x}-e^{-a x}}{x (x^4+b^4)} + i R \int_0^{\pi/2} d\theta \, e^{i \theta} \frac{e^{i a R e^{i \theta}}- e^{-a R e^{i \theta}}}{R e^{i \theta} (R^4 e^{i 4 \theta}+b^4)} + \int_R^0 dx \frac{e^{-a x}-e^{-i a x}}{x (x^4+b^4)}

$$


The second integral vanishes as $$R \to \infty$$.  This is because the magnitude of that integral is bounded by


$$

\frac{1}{R^4}\int_0^{\pi/2} d\theta \, e^{-\sqrt{2} a R \sin{(3 \pi/4-\theta)}} \le \frac{2}{R^4} \int_{\pi/4}^{\pi/2} d\theta \, e^{-2 \sqrt{2} a R \theta/\pi} \le \frac{\pi}{\sqrt{2} a R^5} e^{-2 a R/\pi}

$$


The contour integral is then equal to, as $$R \to \infty$$


$$

\int_0^{\infty} dx \frac{e^{i a x} + e^{-i a x} - 2 e^{-a x}}{x (x^4+b^4)}

$$




**Note** that this is twice the integral sought.
The contour integral is also equal to $$i 2 \pi$$ times the residue at the pole $$z=b e^{i \pi/4}$$, or


$$

i 2 \pi \frac{e^{i a b e^{i \pi/4}} – e^{- a b e^{i \pi/4}}}{-4 b^4}

$$


So that the integral sought after is


$$

\int_0^{\infty} dx \frac{\cos{a x}-e^{-a x}}{x (x^4+b^4)} = \frac{\pi}{2 b^4} e^{-a b/\sqrt{2}} \sin{\frac{a b}{\sqrt{2}}}

$$


This answer agrees with Mathematica.

