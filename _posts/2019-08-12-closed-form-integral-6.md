---
layout: post
title: Closed form integral 6
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
  - real-analysis
  
description:  
  Closed form integral 6
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of 

$$
\int_0^\infty \frac{\operatorname{Li}_3(x)}{1+x^2}\ dx
$$

<!–-break-–>

# Answer

Using the generalized integral expression of the polylogrithmic function which can be found in the book ***(Almost) Impossible Integrals, Sums and series*** page 4.

$$
\int_0^1\frac{x\ln^n(u)}{1-xu}\ du=(-1)^n n!\operatorname{Li}_{n+1}(x)
$$ 
and by setting $$n=2$$ we get

$$
\operatorname{Li}_{3}(x)=\frac12\int_0^1\frac{x\ln^2 u}{1-xu}\ du
$$

we can write 

$$
\begin{align}
\Re\int_0^\infty\frac{\operatorname{Li}_{3}(x)}{1+x^2}\ dx 
&=\int_0^1\ln^2u\left(\int_0^\infty\frac{x}{(1-ux)(1+x^2)}\ dx\right)\ du\\
&=\int_0^1\ln^2u\left(-\frac12\left(\frac{\pi u}{1+u^2}+\frac{2\ln(-u)}{1+u^2}\right)\right)\ du, \quad \color{red}{\ln(-u)=\ln u+i\pi}\\
&=-\frac{\pi}{4}\underbrace{\int_0^1\frac{u\ln^2u}{1+u^2}\ du}_{u^2\mapsto\ u}-\frac12\underbrace{\int_0^1\frac{\ln^3u}{1+u^2}\ du}_{-6\beta(4)}\\
&=-\frac{\pi}{32}\int_0^1\frac{\ln^2u}{1+u}\ du+3\beta(4) \tag{#} \\
&=-\frac{\pi}{32}\left(\frac32\zeta(3)\right)+3*\frac1{768}\left(\psi^{(3)}\left(\frac14\right)-8\pi^4\right)\\
&=\frac1{256}\left(\psi^{(3)}\left(\frac14\right)-8\pi^4-12\pi\zeta(3)\right)
\end{align}

$$

note that the value of $$\beta(4)$$ can be found [here][1].


----


**Bonus:**

In the post body, I reached

$$
\int_0^1 \frac{\operatorname{Li}_3(x)}{1+x^2}\ dx=\frac12\Re\int_0^\infty\frac{\operatorname{Li}_3(x)}{1+x^2}\ dx+\frac12\beta(4)-\zeta(2)G
$$

and we proved in $$(\#)$$

$$
\Re\int_0^\infty\frac{\operatorname{Li}_{3}(x)}{1+x^2}\ dx=-\frac{\pi}{32}\int_0^1\frac{\ln^2u}{1+u}\ du+3\beta(4)
$$

therefore

$$
\int_0^1\frac{\operatorname{Li}_{3}(x)}{1+x^2}\ dx=-\frac{\pi}{64}\int_0^1\frac{\ln^2x}{1+x}\ dx+2\beta(4)-\zeta(2)G
$$

substituting thr value of $$\int_0^1\frac{\ln^2x}{1+x}\ dx$$ and $$\beta(4)$$ we get

$$
\int_0^1 \frac{\operatorname{Li}_3(x)}{1+x^2}\ dx=\frac1{384}\left(\psi^{(3)}\left(\frac14\right)-8\pi^4-9\pi\zeta(3)-64\pi^2G\right)
$$

  [1]: https://en.wikipedia.org/wiki/Dirichlet_beta_function?fbclid=IwAR2JKUjyn8sG4wMdUfeT3JyJLpw7C-aanbnwRYbIZ0k9QYwA3Hz1_0OsQhU
  