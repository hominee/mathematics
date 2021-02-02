---
layout: post
title: Problem related to calculus and definite integrals
tag:
 - calculus
 - integration
 - definite-integrals

description: Problem related to calculus and definite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Integral: $$\int_0^\infty \tan^{-1}\left(\frac{2ax}{x^2+c^2} \right)\sin(bx) \; dx$$

<!–-break-–>

prophpbb.
com/post2652.
html?sid=d6641d4d4a3726f1b27bbb4b98ca840a and the solution uses contour integration.
 we are  wondering if there is a way to solve it without using contour integration.
 we tried differentiating wrt $$a$$ and $$c$$ but in both cases, the resulting expression was dirty which made me reluctant to proceed further.
 we are  out of ideas for this one.
 Thanks!
.


# Answer 


In order to prove the final result we will need to state a lemma that will be used later.

Lemma$$\require{autoload-all}$$ $$1$$:


$$

\int_0^\infty \! \frac{\cos(bx)}{x^2+\alpha} \mathrm{d}x = \frac{\pi e^{-b\sqrt{\alpha}}}{2b\sqrt{\alpha}}\tag{1}

$$


Proof here.

Consider


$$

we = \int_0^\infty\!\! \tan^{-1}\left(\frac{2ax}{x^2+c^2} \right)\sin(bx) \; \mathrm{d}x

$$


Integrate by parts


$$

we = \int_0^\infty \!\!\frac{2 a \left(c^2-x^2\right) \cos (b x)}{x^4 +(4 a^2+2 c^2) x^2+c^4} \; \mathrm{d}x

$$


Decompose this function by partial fractions 

$$

\frac{2 a \left(c^2-x^2\right) }{x^4 +(4 a^2+2 c^2) x^2+c^4} = \frac{a_-}{x^2+x_0} + \frac{a_+}{x^2+x_1}

$$


It so happens that


$$

x_0 = 2 a^2+2 a\sqrt{a^2+c^2}+c^2,\quad x_1 = 2 a^2-2a \sqrt{a^2+ c^2}+c^2

$$




$$

a_- =\frac{2a(c^2+x_0)}{x_1-x_0}, \quad a_+ = \frac{2a(c^2+x_1)}{x_0-x_1}

$$




**Note** that both $$x_0$$ and $$x_1$$ are greater than $$0$$.

Re-write the integral


$$




$$
\begin{align*}
 we &= a_-\int_0^{\infty} \!\! \frac{\cos(bx)}{x^2+x_0} \, \mathrm{d}x + a_+\int_0^{\infty} \!\! \frac{\cos(bx)}{x^2+x_1} \, \mathrm{d}x\\[.3cm] &= \frac{2a(c^2+x_0)}{x_1-x_0}\int_0^{\infty} \!\! \frac{\cos(bx)}{x^2+x_0} \, \mathrm{d}x +\frac{2a(c^2+x_1)}{x_0-x_1}\int_0^{\infty} \!\! \frac{\cos(bx)}{x^2+x_1} \, \mathrm{d}x
\end{align*}


$$

$$


Using $$(1)$$:


$$




$$
\begin{align*}
 we &= \frac{2a(c^2+x_0)}{x_1-x_0}\cdot\frac{\pi e^{-b\sqrt{x_0}}}{2b\sqrt{x_0}} - \frac{2a(c^2+x_1)}{x_1-x_0}\cdot\frac{\pi e^{-b\sqrt{x_1}}}{2b\sqrt{x_1}}\\[.3cm] &= \left(\frac{a\pi}{b(x_1-x_0)}\right)\left(\frac{(c^2+x_0)e^{-\sqrt{x_0}}}{\sqrt{x_0}} - \frac{(c^2+x_1)e^{-\sqrt{x_1}}}{\sqrt{x_1}}\right)
\end{align*}


$$

$$



we will digress here to state (without proof but easily verified) that 

$$

\frac{c^2+x_0}{\sqrt{x_0}}= \frac{c^2+x_1}{\sqrt{x_1}} = \frac{x_1-x_0}{2a}.

$$

 This allows us a tremendous simplification so that we can write


$$




$$
\begin{align*}
 we = \left(\frac{\pi}{2b}\right)\left(e^{-b\sqrt{x_1}}-e^{-b\sqrt{x_0}} \right). 
\end{align*}


$$

$$


It can also be shown that 


$$

\sqrt{x_1} = -a+\sqrt{a^2+c^2}

$$

 


$$

\sqrt{x_0} = a+\sqrt{a^2+c^2}

$$

 
Simply square each side to find the desired equality.
We can now complete the proof:


$$




$$
\begin{align*}
 we &= \frac{\pi}{2b}\left(e^{-b\sqrt{x_1}}-e^{-b\sqrt{x_0}} \right) \\[.2cm]
&=  \frac{\pi}{2b}\left(\exp\left(ab-b\sqrt{a^2+c^2}\right)-\exp\left(-ab-b\sqrt{a^2+c^2}\right) \right) \\[.2cm]
&=  \frac{\pi}{b}\exp\left(-b\sqrt{a^2+c^2}\right)\frac12(\exp(ab)-\exp(ab)) \\[.2cm]
&= \dfrac{\pi}{b}\exp\left(-b\sqrt{a^2+c^2}\right)\sinh{ab}
\end{align*}


$$

$$


If you are interested in working through the simplifications that we did not prove, we recommend that you begin by squaring each side after verifying that each side shares the same sign.

