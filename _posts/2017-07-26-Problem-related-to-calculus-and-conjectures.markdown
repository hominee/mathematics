---
layout: post
title: Problem related to calculus and conjectures
tag:
 - calculus
 - integration
 - definite-integrals
 - closed-form
 - conjectures

description: Problem related to calculus and conjectures

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Conjecture $$\int_0^1\frac{\mathrm dx}{\sqrt{1-x}\ \sqrt[4]x\ \sqrt[4]{2-x\,\sqrt3}}\stackrel?=\frac{2\,\sqrt2}{3\,\sqrt[8]3}\pi$$

<!–-break-–>



 $$ 
\int_0^1\frac{\mathrm dx}{\sqrt{1-x}\ \sqrt[4]x\ \sqrt[4]{2-x\,\sqrt3}}\stackrel?=\frac{2\,\sqrt2}{3\,\sqrt[8]3}\pi\tag1
 $$ 

The equality numerically holds up to at least $$10^4$$ decimal digits.

Can we prove that the equality is exact?

An equivalent form of this conjecture is

 $$ 
I\left(\frac{\sqrt3}2;\ \frac14,\frac14\right)\stackrel?=\frac23,\tag2
 $$ 

where $$I\left(z;\ a,b\right)$$ is the regularized beta function.

Even simpler case:

 $$ 
\int_0^1\frac{\mathrm dx}{\sqrt{1-x}\ \sqrt[6]{9-x}\ \sqrt[3]x}\stackrel?=\frac\pi{\sqrt3},\tag3
 $$ 

which is equivalent to

 $$ 
I\left(\frac19;\ \frac16,\frac13\right)\stackrel?=\frac12.\tag4
 $$ 


A related question.

# Answer 


For $$\alpha, \beta, \gamma \in (0,1)$$ satisfying $$\alpha+\beta+\gamma = 1$$ and 
$$\mu \in \mathbb{C} \setminus [1,\infty)$$, define

 $$ 

F_{\alpha\beta}(\mu) = \int_0^1\frac{dx}{x^\alpha(1-x)^\beta(1-\mu x)^\gamma}
\quad\text{ and }\quad
\Delta = \frac{\Gamma(1-\alpha)\Gamma(1-\beta)}{\Gamma(1+\gamma)}

 $$ 

When $$\mid {} \mu\mid {}  < 1$$, we can rewrite the integral $$F_{\alpha\beta}(\mu)$$ as

 
$$

\begin{align*}
F_{\alpha\beta}(\mu) 
= & \int_0^1 \frac{1}{x^\alpha(1-x)^{\beta}}\left(\sum_{n=0}^{\infty}\frac{(\gamma)_n}{n!}\mu^n x^n\right) dx
= \sum_{n=0}^{\infty}\frac{(\gamma)_n}{n!}\frac{\Gamma(n+1-\alpha)\Gamma(1-\beta)}{\Gamma(n+1+\gamma)}\mu^n\\
= & \Delta\sum_{n=0}^{\infty}\frac{(\gamma)_n (1-\alpha)_n}{n!(\gamma+1)_n}\mu^n
= \Delta\gamma \sum_{n=0}^{\infty}\frac{(1-\alpha)_n}{n!(\gamma+n)}\mu^n
\end{align*}

$$
 

This implies 

 $$ 

\mu^{-\gamma} \left(\mu\frac{\partial}{\partial \mu}\right) \mu^{\gamma} F_{\alpha\beta}(\mu) =  
\Delta\gamma \sum_{n=0}^{\infty}\frac{(1-\alpha)_n}{n!}\mu^n
= \Delta\gamma\frac{1}{(1-\mu)^{1-\alpha}}

 $$ 

and hence

 $$ 
F_{\alpha\beta}(\mu) 
= \Delta\gamma \mu^{-\gamma} \int_0^\mu \frac{\nu^{\gamma-1}d\nu}{(1-\nu)^{1-\alpha}}
= \Delta\gamma \int_0^1 \frac{t^{\gamma-1} dt}{(1-\mu t)^{1-\alpha}}
= \Delta \int_0^1 \frac{dt}{(1 - \mu t^{1/\gamma})^{1-\alpha}}
 $$ 

Notice if we substitute $$x$$ by $$y = 1-x$$, we have

 $$ 
F_{\alpha\beta}(\mu) = \int_0^1 \frac{dy}{y^\beta(1-y)^\alpha(1-\mu - \mu y)^{\gamma}}
= \frac{1}{(1-\mu)^\gamma} F_{\beta\alpha}(-\frac{\mu}{1-\mu})
 $$ 

Combine these two representations of $$F_{\alpha\beta}(\mu)$$ and let $$\omega = \left(\frac{\mu}{1-\mu}\right)^{\gamma}$$, we obtain

 $$ 
F_{\alpha\beta}(\mu) = \frac{\Delta}{(1-\mu)^{\gamma}}\int_0^1 \frac{dt}{( 1 + \omega^{1/\gamma} t^{1/\gamma})^{1-\beta}} = \frac{\Delta}{\mu^\gamma}\int_0^\omega \frac{dt}{(1 + t^{1/\gamma})^{1-\beta}}
 $$ 

Let $$(\alpha,\beta,\gamma) = (\frac14,\frac12,\frac14)$$ and $$\mu = \frac{\sqrt{3}}{2}$$, the identity we want to check becomes

 $$ 
\frac{\Gamma(\frac34)\Gamma(\frac12)}{\Gamma(\frac54) (\sqrt{3})^{1/4}}\int_0^\omega \frac{dt}{\sqrt{1+t^4}} \stackrel{?}{=} \frac{2\sqrt{2}}{3\sqrt[8]{3}} \pi\tag{*1}
 $$ 

Let $$K(m)$$ be the complete elliptic integral of the first kind associated with modulus $$m$$. i.e.

 $$ 
K(m) = \int_0^1 \frac{dx}{\sqrt{(1-x^2)(1-mx^2)}}
 $$ 

It is known that $$\displaystyle K(\frac12) = \frac{8\pi^{3/2}}{\Gamma(-\frac14)^2}$$. In term of $$K(\frac12)$$, it is easy to check $$(*1)$$ is equivalent to

 $$ 
\int_0^\omega \frac{dt}{\sqrt{1+t^4}} \stackrel{?}{=} \frac23 K(\frac12)\tag{*2}
 $$ 

To see whether this is the case, let $$\varphi(u)$$ be the inverse function of above integral.
More precisely, define $$\varphi(u)$$ by following relation:

 $$ 
u = \int_0^{\varphi(u)} \frac{dt}{\sqrt{1+t^4}}
 $$ 

Let $$\psi(u)$$ be $$\frac{1}{\sqrt{2}}(\varphi(u) + \varphi(u)^{-1})$$. It is easy to check/verify

 $$ 

\varphi'(u)^2 = 1 + \varphi(u)^4
\implies
\psi'(u)^2 = 4 (1 - \psi(u)^2)(1 - \frac12 \psi(u)^2)

 $$ 

Compare the ODE of $$\psi(u)$$ with that of a Jacobi elliptic functions with modulus $$m = \frac12$$, we find

 $$ 
\psi(u) = \text{sn}(2u + \text{constant} \mid {}  \frac12 )\tag{*3}
 $$ 

Since we are going to deal with elliptic functions/integrals with $$m = \frac12$$ only,
we will simplify our notations and drop all reference to modulus, i.e 
$$\text{sn}(u)$$ now means $$\text{sn}(u\mid {} m=\frac12)$$ and $$K$$ means $$K(m = \frac12)$$.
Over the complex plane, it is known that $$\text{sn}(u)$$ is doubly periodic with
fundamental period $$4 K$$ and $$2i K$$. It has two poles at $$i K$$ and $$(2 + i)K$$ in the fundamental domain.
When $$u = 0$$, we want $$\varphi(u) = 0$$ and hence $$\psi(u) = \infty$$. So the constant
in $$(*3)$$ has to be one of the pole. For small and positive $$u$$, we want $$\varphi(u)$$ and hence $$\psi(u)$$ to be positive. This fixes the constant to $$i K$$. i.e.

 $$ 
\psi(u) = \text{sn}(2u + iK )
 $$ 

and the condition $$(*2)$$ becomes whether following equality is true or not.

 $$ 
\frac{1}{\sqrt{2}} (\omega + \omega^{-1}) \stackrel{?}{=} \text{sn}( \frac43 K + i K)\tag{*4}
 $$ 

Notice $$ 3( \frac43 K + i K) = 4 K + 3 i K $$ is a pole of $$\text{sn}(u)$$. if one repeat
apply the addition formula for $$\text{sn}(u+v)$$
 
$$

\text{sn}(u+v) = \frac{\text{sn}(u)\text{cn}(v)\text{dn}(v)+\text{sn}(v)\text{cn}(u)\text{dn}(u)}{1-m\,\text{sn}(u)^2 \text{sn}(v)^2}
$$ 

One find in order for $$\text{sn}(3u)$$ to blow up, $$\text{sn}(u)$$ will be a root of
following polynomial equation:

 $$ 
3 m^2 s^8-4 m^2 s^6-4 m s^6+6 m s^4-1 = 0
 $$ 

Substitute $$m = \frac12$$ and $$s = \frac{1}{\sqrt{2}}(t+\frac{1}{t})$$ into this, the equation $$\omega$$ need to satisfy is given by:

 $$ 
(t^8 - 6 t^4 - 3)(3 t^8 + 6 t^4 - 1 ) = 0
 $$ 

One can check that $$\omega = \sqrt[4]{\frac{\sqrt{3}}{2-\sqrt{3}}}$$ is indeed a root of this polynomial. As a result, the original equality is valid.

