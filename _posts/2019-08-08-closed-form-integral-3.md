---
layout: post
title: Closed form integral 3
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
  
description:  
  Closed form integral 3
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :

$$
\int_0^{\infty}\frac{\operatorname{Li}_s(-x)}{x^{\alpha+1}}\mathrm dx
= -\frac1{\alpha^s}\frac{\pi}{\sin(\pi \alpha)}
$$

<!–-break-–>

# Answer

 use the series expansion of $$\operatorname{Li}_s(-x)$$ which yields to

$$
\begin{equation*}
\begin{aligned}
\int_0^{\infty}\frac{\operatorname{Li}_s(-x)}{x^{\alpha+1}}\mathrm dx&=\int_0^{\infty}\frac1{x^{\alpha+1}}\left[\sum_{n=1}^{\infty}\frac{(-x)^n}{n^s}\right]\mathrm dx\\
&=\sum_{n=1}^{\infty}\frac{(-1)^n}{n^s}\int_0^{\infty}\frac{x^n}{x^{\alpha+1}}\mathrm dx\\
&=\sum_{n=1}^{\infty}\frac{(-1)^n}{n^s}\int_0^{\infty}x^{n-\alpha-1}\mathrm dx
\end{aligned}
\end{equation*}
$$

But one can easily see the problems concerning the convergence of the last integral. Furthermore I am not sure whether it is possible to interchange the order of summation and integration in this case or not. 

Another approach would be to use the an integral represantation of $$\operatorname{Li}_s(-x)$$ so that the given integral becomes

$$
\begin{equation*}
\begin{aligned}
\int_0^{\infty}\frac{\operatorname{Li}_s(-x)}{x^{\alpha+1}}\mathrm dx&=\int_0^{\infty}\frac1{x^{\alpha+1}}\left[\frac1{\Gamma(s)}\int_0^{\infty}\frac{t^{s-1}}{e^t/(-x)-1}\mathrm dt\right]\mathrm dx\\
&=-\frac1{\Gamma(s)}\int_0^{\infty}\int_0^{\infty}\frac{t^{s-1}}{x^{\alpha}(e^t+x)}\mathrm dx\mathrm dt\\
\end{aligned}
\end{equation*}
$$

for $$b>0$$, we have $$\int_0^\infty  \frac{1}{x^\alpha (b + x)}dx  = b^{ - \alpha } \int_0^\infty  \frac{x^{ - \alpha }}{1 + x}dx  = \frac{b^{ - \alpha }\pi }{\sin \alpha \pi }$$
so

$$\int_0^{\infty} \frac{\operatorname{Li}_s(-x)}{x^{\alpha+1}}dx = -\frac{1}{\Gamma(s)}
\int_0^{\infty} \int_0^{\infty} \frac{t^{s-1}}{x^{\alpha}(e^t+x)}dxdt = - \frac{\pi }{\Gamma (s)\sin \alpha \pi }
\int_0^\infty  t^{s - 1} e^{ - \alpha t}dt 
$$
