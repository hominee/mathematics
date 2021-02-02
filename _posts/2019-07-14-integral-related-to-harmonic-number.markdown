---
layout: post
title: sum related to harmonic-number
tags:
  - sum 
  - closed-form
  - harmonic-number
  - real-analysis
  
description:  
  sum related to harmonic-number
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$

\sum^\infty_{n=1}\frac{H_n}{2^n\,(2n+1)^2}

$$



<!–-break-–>



# Answer

I will here derive an expression for the more general problem of evaluating 
$$\sum_{n=1}^\infty \frac{H_n z^{2n+1}}{(2n+1)^2}$$ for $$\mid z \mid < 1$$ in terms of polylogarithms. 
This derivation uses the same idea as outlined by tired in the comments. The derivation contains the expression for several integrals which people might find interesting, however the derivation contains so many terms that I had to rely on mathematical software to get everything right so it's not very illuminating and it does not fully answer the question.

Mathematica code used to evaluate and simplify the integrals can be [found here](http://folk.uio.no/hansw/output.txt).

---

We start using [the identity](https://math.stackexchange.com/a/918168/147873) $$\int_0^1x^{2n}\log(x){\rm d}x = -\frac{1}{(2n+1)^2}$$ the sum can be written as an integral

$$
\sum_{n=1}^\infty \frac{H_n z^{2n+1}}{(2n+1)^2} = -z\int_0^1\sum_{n=1}^\infty (zx)^{2n}H_n\log(x)\,{\rm d}x = \int_0^1\frac{\log(x)\log(1-(zx)^2)}{1-(zx)^2}z{\rm d}x
$$


Splitting the $$\log$$ and a partial fraction decomposition gives us

$$
\sum_{n=1}^\infty \frac{H_n z^{2n+1}}{(2n+1)^2} = \frac{I(z) - I(-z) + J(z) - J(-z)}{2}
$$


where $$I(z)$$ is given by (see the end of this post for steps to derive this)


$$
I(z)=\int_0^1\frac{\log(x)\log(1+zx)}{1+zx}z{\rm d}x = \int_0^z\frac{\log(x)\log(1+x)}{1+x}{\rm d}x - \log(z)\int_0^z\frac{\log(1+x)}{1+x}{\rm d}x \\= \text{Li}_3\left(\frac{1}{1+z}\right)+\text{Li}_2\left(\frac{1}{1+z}\right) \log(1+z)-\zeta(3)+\frac{\log^3(1+z)}{3}-\frac{\log(z)\log^2(1+z)}{2}
$$

and using various polylog identities (see the end of this post) we get 

$$
I(-z) = \text{Li}_3(1-z)-\text{Li}_2(1-z) \log (1-z)-\zeta(3)-\frac{\log(z)\log^2(1-z)}{2}
$$


The last integral we need is

$$
J(z) = \int_0^1\frac{\log(x)\log(1-zx)}{1+zx}z{\rm d}x = \int_0^z\frac{\log(x)\log(1-x)}{1+x}{\rm d}x - \log(z)\int_0^z\frac{\log(1-x)}{1+x}{\rm d}x \\= -\text{Li}_3\left(\frac{1-z}{2}\right)+\text{Li}_3\left(\frac{z-1}{2z}\right)-\text{Li}_3\left(\frac{z-1}{z}\right)-\text{Li}_3(-z)+\left[\text{Li}_2\left(\frac{1-z}{2}\right)-\text{Li}_2\left(\frac{z-1}{2z}\right)+\text{Li}_2\left(\frac{z-1}{z}\right)\right]\log\left(\frac{1-z}{2z}\right)+\text{Li}_2(-z)\log(2z)\\+\frac{7\zeta(3)}{8}-\frac{1}{6}\pi^2\log(2)+\frac{1}{2}\log(2)\log(z)\log(2z)+\frac{1}{12}\pi^2\log(z)
$$

and again using polylog identities we find

$$
\begin{align*}
J(-z) = -\text{Li}_3(z)-\text{Li}_3\left(\frac{z}{z+1}\right)+\text{Li}_3\left(\frac{2z}{z+1}\right)-\text{Li}_3\left(\frac{z+1}{2}\right)+\text{Li}_2(z) \log (2z) \\
+\left[-\text{Li}_2\left(\frac{z}{z+1}\right)+\text{Li}_2\left(\frac{2z}{z+1}\right)+\text{Li}_2\left(\frac{z+1}{2}\right)\right] \\
 \log\left(\frac{z+1}{2 z}\right)-\frac{1}{2} \log (2) \log^2(z+1)-\frac{1}{2} \log ^2(2) \log (z)+\log (2) \log (2 z) \log(z+1) \\
 +\frac{1}{12} \pi ^2 \log (z)+\frac{7 \zeta(3)}{8}-\frac{\log ^3(2)}{3}
\end{align*}
$$


The reason I have choosen to give separate expressions for $$\pm z$$ is to make sure all terms are real when $$z\in (0,1)$$ so that one can apply these directly without any knowledge about the analytical continuation of the polylogarithmic functions. The expressions for $$I(z),J(z)$$ above have been compared to numerical results and agree perfectly.

Adding up we get (this equation is also double checked numerically)


$$
\matrix{2\sum_{n=1}^\infty \frac{H_nz^{2n+1}}{(2n+1)^2} &=& -\text{Li}_3\left(\frac{1-z}{2}\right)-\text{Li}_3(1-z)-\text{Li}_3(-z)+\text{Li}_3(z)-\text{Li}_3\left(\frac{z}{z-1}\right)\\&&+\text{Li}_3\left(\frac{2z}{z-1}\right)+\text{Li}_3\left(\frac{1}{1+z}\right)+\text{Li}_3\left(\frac{z}{1+z}\right)\\&&-\text{Li}_3\left(\frac{2z}{1+z}\right)+\text{Li}_3\left(\frac{1+z}{2}\right)+\text{Li}_2\left(\frac{1}{1+z}\right) \log (1+z)\\&&+\text{Li}_2(1-z) \log(1-z)+\text{Li}_2(-z) \log(2z)-\text{Li}_2(z)\log (2z)\\&&+\left[\text{Li}_2\left(\frac{1-z}{2}\right)-\text{Li}_2\left(\frac{z}{z-1}\right)+\text{Li}_2\left(\frac{2 z}{z-1}\right)\right] \log \left(\frac{1-z}{2z}\right)\\&&+\left[\text{Li}_2\left(\frac{z}{1+z}\right)-\text{Li}_2\left(\frac{2z}{1+z}\right)-\text{Li}_2\left(\frac{z+1}{2}\right)\right] \log\left(\frac{1+z}{2z}\right)\\&&-\log \left(\frac{1+z}{1-z}\right) \left[\frac{1}{2} \log\left(\frac{z}{2}\right)\log\left(1-z^2\right)+\log (2) \log (2z)\right]+\frac{1}{3}\log^3(1+z)}
$$


and right here I lost my appetite for working more on this!




$$
\bf \text{Useful polylog identities:}
$$

For real $$w>1$$ [we have](https://en.wikipedia.org/wiki/Polylogarithm#Relationship_to_other_functions)


$$
\text{Li}_2(w)+\text{Li}_2\left(\frac{1}{w}\right)=-\frac{\log^2(w)}{2}-i\pi  \log (w)+\frac{\pi ^2}{3}
$$



$$
\text{Li}_3(w)-\text{Li}_3\left(\frac{1}{w}\right) = -\frac{\log^3(w)}{6}-\frac{1}{2} i \pi\log ^2(w)+\frac{1}{3} \pi^2 \log(w)
$$





$$
\bf{\text{Derivation of I(z)}}
$$


Take $$t = \log (1 + x) $$ then the integral becomes

$$
\int_0^z\frac{\log(x)\log(1+x)}{1+x}{\rm d}x = \int_0^{\log (1 + z)} x^2 + x\log (1 + e^{-x}) {\rm d} x
$$

Now expanding the $$\log$$ in a Taylor series and integrating term-by-term gives us

$$
\frac {\log^3 (1 + z)} {3} - \sum_ {n=1}^\infty\left[\frac {1} {n^3} - \frac {1} {n^3 (1 + z)^n} - \frac {\log (1 + z)} {n^2 (1 + z)^n}\right] 
$$

The sum can then be evaluated using the definition of the [polylogarithm](https://en.wikipedia.org/wiki/Polylogarithm) and the $$\zeta$$ function.