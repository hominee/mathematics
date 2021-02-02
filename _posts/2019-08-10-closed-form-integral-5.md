---
layout: post
title: Closed form integral 5
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
  - real-analysis
  
description:  
  Closed form integral 5
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of 

$$
\sum_{n=0}^\infty\frac{\operatorname{Li}_{1/2}\left(-2^{-2^{-n}}\right)}{\sqrt{2^n}}
$$

<!–-break-–>

Let

$$
S=\sum_{n=0}^\infty\frac{\operatorname{Li}_{1/2}\left(-2^{-2^{-n}}\right)}{\sqrt{2^n}}
$$

where $$\operatorname{Li}_a(z)$$ is the [polylogarithm](http://mathworld.wolfram.com/Polylogarithm.html). 
For $$a=1/2$$ it can be represented as

$$
\begin{equation*}
\begin{aligned}
\operatorname{Li}_{1/2}(z)&=\sum_{k=1}^\infty\frac{z^k}{\sqrt k} \\
&=\int_0^\infty\frac z{\sqrt{\pi\,x}\ \left(e^x-z\right)}\,dx.
\end{aligned}
\end{equation*}
$$
 
So how to find a closed-form expression for $$S$$?

# Answer

1. Let us denote

$$
a_n=\frac{\operatorname{Li}_{1/2}\left(-2^{-2^{-n}}\right)}{2^{n/2}},
\qquad 
b_n=\frac{\operatorname{Li}_{1/2}\left(2^{-2^{-n}}\right)}{2^{n/2}}.
$$

These quantities satisfy the recurrence relation

$$
a_n+b_n=b_{n-1},\tag{2}
$$

which follows from the [identity](http://functions.wolfram.com/ZetaFunctionsandPolylogarithms/PolyLog/17/02/01/02/0001/)

$$
\sqrt{2}\,\operatorname{Li}_{1/2}\left(z^2\right)=
\operatorname{Li}_{1/2}\left(z\right)+\operatorname{Li}_{1/2}\left(-z\right).
$$

 2. The relation (2) implies that
 
$$
b_N+\sum_{n=0}^Na_n=b_{-1},
$$

and therefore our series telescopes:

$$
S=\sum_{n=0}^{\infty}a_n=b_{-1}-b_{\infty}.\tag{3}
$$

 3. The polylogarithm asymptotics
 
$$
\operatorname{Li}_{1/2}(x)\sim\frac{\sqrt{\pi}}{\sqrt{1-x}}\quad \text{as}\;\;
x\rightarrow 1^-,
$$

implies that $$\displaystyle b_{\infty}=\sqrt{\frac{\pi}{\ln 2}}$$. Being combined with (3), this finally gives the above answer (which is further confirmed numerically).

so the result is 

$$
\boxed{\; S=\sqrt{2}\,\operatorname{Li}_{1/2}\left(\frac14\right)-\sqrt{\displaystyle\frac{\pi}{\ln 2}}\;} \tag{1}
$$