---
layout: post
title: Closed form integral 2
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
  - Riemann-zeta
description:  
  Closed form integral 2
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :

$$
\int_{0}^{\Large\frac\pi2}
{\ln^{2}\left(\vphantom{\large A}\cos\left(x\right)\right)
\ln^{2}\left(\vphantom{\large A}\sin\left(x\right)\right)
\over
\cos\left(x\right)\sin\left(x\right)}\,{\rm d}x
={1 \over 4}\,
\bigg[2\,\zeta\left(5\right) - \zeta\left(2\right)\zeta\left(3\right) \bigg]
$$

<!–-break-–> 

# Answer

Related problems: [(I)](https://math.stackexchange.com/questions/294226/some-integrals-with-log/294323#294323), [(II)](https://math.stackexchange.com/questions/397347/find-the-value-of-int-0-infty-fracx3ex-1-lnex-1-dx/397754#397754), [(III)](https://math.stackexchange.com/questions/330057/how-to-evaluate-i-displaystyle-int-0-pi-2x2-ln-sin-x-ln-cos-xdx/332041#332041), [(IV)](https://math.stackexchange.com/questions/275643/proving-an-alternating-euler-sum-sum-k-1-infty-frac-1k1-h-kk/276590#276590), [(V)](https://math.stackexchange.com/questions/873333/how-find-this-integral-i-int-0-frac-pi2-ln1-tan4x2-frac2/873425#873425), [(6)](https://math.stackexchange.com/questions/397347/find-the-value-of-int-0-infty-fracx3ex-1-lnex-1-dx/397754#397754). Use the change of variables $$\ln(\cos(x))=t$$ to transform the integral to

$$ 
I = \int_{0}^{\frac{\pi }{2}} \frac{\ln ^{2}\cos x{\ln ^{2}}\sin x}{\cos x\sin x} \text{d}x 
= \frac{1}{4}\,\int _{-\infty }^{0} \! \frac {t^{2} \left( \ln  \left( 1-{
\rm{e}^{2\,t}} \right)\right) ^{2}}{1-\rm{e}^{2t}} dt.
$$

Follow it by another change of variables $$ 1-e^{2t}=z $$ gives

$$\frac{1}{4}\,\int _{-\infty }^{0}\!{\frac {t^{2} \left( \ln  \left( 1-{
{\rm e}^{2\,t}} \right)  \right) ^{2}}{1-  {\rm{e}^{2t}}
 }}{dt}= \frac{1}{32}\,\int _{0}^{1}\!{\frac { \left( \ln  \left( 1-z \right) 
 \right) ^{2} \left( \ln  \left( z \right)  \right) ^{2}}{z \left( 1-
z\right) }}{dz}$$ 

$$= \frac{1}{32}\,\int _{0}^{1}\!{\frac { \left( \ln  \left( 1-z \right) 
 \right) ^{2} \left( \ln  \left( z \right)  \right) ^{2}}{z }}{dz}+\frac{1}{32}\,\int _{0}^{1}\!{\frac { \left( \ln\left( 1-z \right) 
 \right) ^{2} \left( \ln  \left( z \right)  \right) ^{2}}{ \left( 1-
z\right) }}{dz} $$

$$ \implies I = \frac{1}{16}\,\int _{0}^{1}\!{\frac { \left( \ln  \left( 1-z \right) 
 \right) ^{2} \left( \ln  \left( z \right)  \right) ^{2}}{z }}{dz}\longrightarrow (1). $$

**Getting the exact result:** Integral (1) can be evaluated as

$$ \frac{1}{16}\,\int _{0}^{1}\!{\frac { \left( \ln  \left( 1-z \right) 
 \right)^{2} \left( \ln  \left( z \right)  \right)^{2}}{z }}{dz}=\frac{1}{16} \lim_{w\to 0}\lim_{s\to 0^+}\frac{d^2}{dw^2}\frac{d^2}{ds^2}\int_{0}^{1} (1-z)^{w}z^{s-1}dz $$

$$ = \frac{1}{16}\lim_{w\to 0}\lim_{s\to 0^+}\frac{d^2}{dw^2}\frac{d^2}{ds^2}\beta(s,w+1)=\frac{1}{16}\lim_{w\to 0}\lim_{s\to 0^+}\frac{d^2}{dw^2}\frac{d^2}{ds^2}\frac{\Gamma(s)\Gamma(w+1)}{\Gamma(s+w+1)}$$

$$ I=\frac{1}{4}\left( 2\zeta \left( 5 \right)-\zeta \left( 2 \right)\zeta \left( 3 \right) \right) \longrightarrow (*), $$

where [$$\beta(u,v)$$ is the beta function](http://en.wikipedia.org/wiki/Beta_function). 

**Other forms for the solution 1:** Using integration by parts with $$u=\ln^2(1-z)$$, integral $$(1)$$ can be written as

$$ \frac{1}{16}\,\int _{0}^{1}\!{\frac { \left( \ln  \left( 1-z \right) 
 \right)^{2} \left( \ln  \left( z \right)\right)^{2}}{z }}{dz}=\frac{1}{24}\,\int _{0}^{1}\!{\frac{ \ln\left( 1-z \right)\left( \ln  \left( z \right) \right)^{3}}{1-z}}{dz} $$

$$ = -\sum_{n=0}^{\infty}(\psi(n+1)+\gamma)\int_{0}^{1}z^n\ln^3(z)dz = \frac{1}{4}\sum_{n=0}^{\infty}\frac{\psi(n+1)+\gamma}{(n+1)^4}. $$

$$ I= \frac{1}{4}\sum_{n=1}^{\infty}\frac{\psi(n)}{n^4}+\frac{\gamma}{4}\zeta(4)\sim 0.02413779000 \longrightarrow (**). $$

You can use the identity $$ H_{n-1}=\psi(n)+\gamma $$, where $$H_n$$ are [the harmonic numbers](http://en.wikipedia.org/wiki/Harmonic_number), to write the result as

$$ I=\frac{1}{4}\sum_{n=1}^{\infty}\frac{H_{n-1}}{n^4} \longrightarrow (***). $$

**Other forms for the solution 2:** We can have the following form for the solution

$$ I=\frac{1}{16}\sum_{n=1}^{\infty}\frac{H^2_{n}}{n^3}+\frac{1}{16}\sum_{n=1}^{\infty}\frac{\psi'(n+1)}{n^3}-\frac{1}{16}\zeta(2)\zeta(3)\longrightarrow (****). $$

**Note 1:** we used the power series expansion of the function $$ \frac{\ln(1-z)}{1-z}, $$

$$\frac{\ln(1-z)}{1-z}= -\sum _{n=0}^{\infty } \left( \psi \left( n+1 \right) + \gamma \right){x}^{n}=-\sum _{n=0}^{\infty } H_{n}{x}^{n}. $$

**Note 2:** Try to tackle integral $$(1)$$ using the technique used in solving [your previous question](https://math.stackexchange.com/questions/265981/how-to-evaluate-int-01-frac-ln-2-left-1-x-right-ln-2-l). 