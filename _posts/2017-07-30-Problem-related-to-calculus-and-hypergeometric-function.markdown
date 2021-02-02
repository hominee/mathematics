---
layout: post
title: Problem related to calculus and hypergeometric function
tag:
 - calculus
 - definite-integrals
 - special-functions
 - closed-form
 - hypergeometric-function

description: Problem related to calculus and hypergeometric function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Prove $$_2F_1\left(\frac13,\frac13;\frac56;-27\right)\stackrel{\color{#808080}?}=\frac47$$

<!–-break-–>


I discovered the following conjecture numerically, but have not been able to prove it yet:

 $$ 
_2F_1\left(\frac13,\frac13;\frac56;-27\right)\stackrel{\color{#808080}?}=\frac47.\tag1
 $$ 

The equality holds with at least $$10000$$ decimal digits of precision. It can be written in equivalent forms in terms of definite integrals:

 $$ 
{\large\int}_0^1\frac{dx}{\sqrt{1-x}\ \sqrt[3]{x^2+(3x)^3}}\stackrel{\color{#808080}?}=\frac{\sqrt[3]4\,\sqrt3}{7\pi}\Gamma^3\!\!\left(\tfrac13\right),\tag2
 $$ 

or

 $$ 
{\large\int}_0^\pi\frac{d\phi}{\sqrt[3]{\sin\phi}\,\sqrt[3]{55+12\sqrt{21}\cos\phi}}\stackrel{\color{#808080}?}=\frac{\sqrt[3]4\,\sqrt3}{7\pi}\Gamma^3\!\!\left(\tfrac13\right).\tag3
 $$ 


Update: A several more equivalent forms:

 $$ 
_2F_1\left(\frac13,\frac12;\frac56;\frac{27}{28}\right)\stackrel{\color{#808080}?}=\frac{2^{\small8/3}}{7^{\small2/3}}\tag4
 $$ 


 $$ 
\int_0^\infty\frac{dx}{\sqrt[3]{55+\cosh x}}\stackrel{\color{#808080}?}=\frac{\sqrt[3]2\,\sqrt3}{7\pi}\Gamma^3\!\!\left(\tfrac13\right)\tag5
 $$ 


 $$ 
C_{\small-1/3}^{\small(1/3)}(55)\stackrel{\color{#808080}?}=\frac{3}{7\pi^2}\Gamma^3\!\!\left(\tfrac13\right)\tag6
 $$ 


 $$ 
P_{\small-1/2}^{\small1/6}(55)\stackrel{\color{#808080}?}=\frac{\sqrt2\,\sqrt[4]3\,e^{\small-\pi\,i/12}}{7^{\small13/12}\,\pi^{\small3/2}}\Gamma^2\!\!\left(\tfrac13\right)\tag7
 $$ 

where $$C_n^{(\lambda)}(x)$$ is the Gegenbauer polynomial and $$P_l^m(x)$$ is the Legendre function of the first kind.


Please suggest ideas how to prove this conjecture.
What are other points where the function $$_2F_1\left(\frac13,\frac13;\frac56;z\right)$$ takes simple special values?

.

# Answer 


The conjecture is true, as are the other cases reported in the comments
where $$f(z) := {}_2F_1 \left( \frac13, \frac13; \frac56; z \right)$$
takes algebraic values for special rational values of $$z$$.
There are a few others obtained from the symmetry $$z \leftrightarrow 1-z$$
(these $${}_2F_1$$ parameters correspond to a hyperbolic triangle group
with index $$6,6,\infty$$ at $$c=0,1,\infty$$, so the $$z=0$$ and $$z=1$$
indices coincide); e.g. $$f(-1/3) = 2 / 3^{2/3}$$ pairs with
$$f(4/3) = 3^{-2/3} (5-\sqrt{-3})/2$$.   ($$z=1/2$$ pairs with itself,
and the pair $$f(-4)$$ and $$f(5)$$ has been noted already;
the OP's $$f(-27) = -4/7$$ pairs with $$f(28) = \frac12 - \frac3{14} \sqrt{-3}$$.)
Somewhat more exotic are

 $$ 

f\big({-}4\sqrt{13}\,(4+\sqrt{13})^3\big) = \frac7{13\,U_{13}}\\
f\big({-}\sqrt{11}\,(U_{33})^{3/2}\big) = \frac{6}{11^{11/12}\, U_{33}^{1/4}},

 $$ 

with fundamental units $$U_{13}=\frac{3+\sqrt{13}}2,\;U_{33}=23+4\sqrt{33}$$ and further values at algebraic conjugates and images under
$$z \leftrightarrow 1-z$$.
In general, for $$z<1$$ the integral formula for $$f(z)$$ relates it with

 $$ 

\int_0^1 \frac{dx}{ \sqrt{1-x} \; x^{2/3} (1-zx)^{1/3} }

 $$ 

which is half of a "complete real period" for the holomorphic differential
$$dx/y$$ on the curve $$C_z : y^6 = (1-x)^3 x^4 (1-zx)^2$$.  This curve
has genus $$2$$, but is in the special family of genus-$$2$$ curves
with an automorphism of order $$3$$ (multiply $$y$$ by a cube root of unity),
for which both real periods are multiples of the real period of a
single elliptic curve $$E_z$$ (a.k.a. a complete elliptic integral).
In general the resulting formula doesn't simplify further, but when
$$E_z$$ has CM (complex multiplication) its periods can be expressed
in terms of gamma functions.  For $$z = -27$$ and the other special values
listed above, not only does $$E_z$$ have CM but the CM ring is contained in
$${\bf Z}[\rho]$$ where $$\rho = e^{2\pi i/3} = (-1+\sqrt{-3})/2$$.
Then the $$\Gamma$$ and $$\pi$$ factors of the period of $$E_z$$ exactly
match those in the integral formula, leaving us with
an algebraic value of $$f(z)$$.  It turns out that the choice $$z = -27$$
makes $$E_z$$ a curve with complex multiplication by $${\bf Z}[7\rho]$$.
The others from the comments lead to $${\bf Z}[m\rho]$$ with $$m=1,2,3,5$$,
and the examples where $$z$$ is a quadratic irrationality come from
$${\bf Z}[13\rho]$$ and $${\bf Z}[11\rho]$$.
One way to get from $$C_z$$ to $$E_z$$ is to start from the change of variable
$$u^3 = (1+cx)/x$$, which gives

 $$ 

f(z) = \int_{\root 3 \of {1-z}}^\infty \frac{3u \, du}{\sqrt{(u^3+z)(u^3+z-1)}}.

 $$ 

and identifies $$C_z$$ with the hyperelliptic curve $$v^2 = (u^3+z)(u^3+z-1)$$.
Now in general a curve $$v^2 = u^6+Au^3+B^6$$ has an involution $$\iota$$ taking
$$u$$ to $$B^2/u$$, and the quotient by $$\iota$$ is an elliptic curve;
we compute that this curve has $$j$$-invariant

 $$ 

j = 6912 \frac{(5+2r)^3}{(2-r)^3(2+r)}

 $$ 

where $$A = rB^3$$.  (There are two choices of $$\iota$$, related by
$$v \leftrightarrow -v$$, and thus two choices of $$j$$, related by
$$r \leftrightarrow -r$$; but the corresponding elliptic curves
are $$3$$-isogenous, so their periods are proportional.)
In our case $$r = A/B^3 = -(2z+1)/\sqrt{z^2+z}$$ (in which the
$$z \leftrightarrow 1-z$$ symmetry takes $$r$$ to $$-r$$).  Taking $$z=-27$$
yields $$j = -2^{15} 3^4 5^3 (52518123 \pm 11460394\sqrt{21})$$,
which are the $$j$$-invariants of the $${\bf Z}[7\rho]$$ curves;
working backwards from the $$j$$-invariants of the other
$${\bf Z}[m\rho]$$ curves we find the additional values of $$z$$
noted in the comments and earlier in this answer.

