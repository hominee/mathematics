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

\sum_{n=1}^\infty \frac{H_n }{n^3 2^n}

$$




<!–-break-–>


# Answer

Continuing [Raymond Manzoni's answer](https://math.stackexchange.com/a/605602/123277) (both of them deserve the credit because of inspiring my answer) we have

$$

\sum_{n=1}^\infty \frac{H_nx^n}{n^2}=\zeta(3)+\frac{1}{2}\ln x\ln^2(1-x)+\ln(1-x)\operatorname{Li}_2(1-x)+\operatorname{Li}_3(x)-\operatorname{Li}_3(1-x).

$$

Dividing equation above by $$x$$ and then integrating yields

$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_nx^n}{n^3}=&\zeta(3)\ln x+\frac12\color{red}{\int\frac{\ln x\ln^2(1-x)}{x}\ dx}+\color{blue}{\int\frac{\ln(1-x)\operatorname{Li}_2(1-x)}x\ dx}\\&+\operatorname{Li}_4(x)-\color{green}{\int\frac{\operatorname{Li}_3(1-x)}x\ dx}.\tag1
\end{align*} 
 $$
Using IBP to evaluate the green integral by setting $$u=\operatorname{Li}_3(1-x)$$ and $$dv=\frac1x\ dx$$, we obtain
$$
\begin{align*}
\color{green}{\int\frac{\operatorname{Li}_3(1-x)}x\ dx}&=\operatorname{Li}_3(1-x)\ln x+\int\frac{\ln x\operatorname{Li}_2(1-x)}{1-x}\ dx\qquad x\mapsto1-x\\
&=\operatorname{Li}_3(1-x)\ln x-\color{blue}{\int\frac{\ln (1-x)\operatorname{Li}_2(x)}{x}\ dx}.\tag2
\end{align*} 
 $$
Using Euler's reflection formula for dilogarithm

$$

\operatorname{Li}_2(x)+\operatorname{Li}_2(1-x)=\frac{\pi^2}6-\ln x\ln(1-x),

$$

then combining the blue integral in $$(1)$$ and $$(2)$$ yields

$$

\frac{\pi^2}6\int\frac{\ln (1-x)}{x}\ dx-\color{red}{\int\frac{\ln x\ln^2(1-x)}{x}\ dx}=-\frac{\pi^2}6\operatorname{Li}_2(x)-\color{red}{\int\frac{\ln x\ln^2(1-x)}{x}\ dx}.

$$

Setting $$x\mapsto1-x$$ and using the identity $$H_{n+1}-H_n=\frac1{n+1}$$, the red integral becomes
$$
\begin{align*}
\color{red}{\int\frac{\ln x\ln^2(1-x)}{x}\ dx}&=-\int\frac{\ln (1-x)\ln^2 x}{1-x}\ dx\\
&=\int\sum_{n=1}^\infty H_n x^n\ln^2x\ dx\\
&=\sum_{n=1}^\infty H_n \int x^n\ln^2x\ dx\\
&=\sum_{n=1}^\infty H_n \frac{\partial^2}{\partial n^2}\left[\int x^n\ dx\right]\\
&=\sum_{n=1}^\infty H_n \frac{\partial^2}{\partial n^2}\left[\frac {x^{n+1}}{n+1}\right]\\
&=\sum_{n=1}^\infty H_n \left[\frac{x^{n+1}\ln^2x}{n+1}-2\frac{x^{n+1}\ln x}{(n+1)^2}+2\frac{x^{n+1}}{(n+1)^3}\right]\\
&=\ln^2x\sum_{n=1}^\infty\frac{H_n x^{n+1}}{n+1}-2\ln x\sum_{n=1}^\infty\frac{H_n x^{n+1}}{(n+1)^2}+2\sum_{n=1}^\infty\frac{H_n x^{n+1}}{(n+1)^3}\\
&=\frac12\ln^2x\ln^2(1-x)-2\ln x\left[\sum_{n=1}^\infty\frac{H_{n+1} x^{n+1}}{(n+1)^2}-\sum_{n=1}^\infty\frac{x^{n+1}}{(n+1)^3}\right]\\&+2\left[\sum_{n=1}^\infty\frac{H_{n+1} x^{n+1}}{(n+1)^3}-\sum_{n=1}^\infty\frac{x^{n+1}}{(n+1)^4}\right]\\
&=\frac12\ln^2x\ln^2(1-x)-2\ln x\left[\sum_{n=1}^\infty\frac{H_{n} x^{n}}{n^2}-\sum_{n=1}^\infty\frac{x^{n}}{n^3}\right]\\&+2\left[\sum_{n=1}^\infty\frac{H_{n} x^{n}}{n^3}-\sum_{n=1}^\infty\frac{x^{n}}{n^4}\right]\\
&=\frac12\ln^2x\ln^2(1-x)-2\ln x\left[\sum_{n=1}^\infty\frac{H_{n} x^{n}}{n^2}-\operatorname{Li}_3(x)\right]\\&+2\left[\sum_{n=1}^\infty\frac{H_{n} x^{n}}{n^3}-\operatorname{Li}_4(x)\right].
\end{align*} 
 $$
Putting all together, we have
$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_nx^n}{n^3}=&\frac12\zeta(3)\ln x-\frac18\ln^2x\ln^2(1-x)+\frac12\ln x\left[\sum_{n=1}^\infty\frac{H_{n} x^{n}}{n^2}-\operatorname{Li}_3(x)\right]\\&+\operatorname{Li}_4(x)-\frac{\pi^2}{12}\operatorname{Li}_2(x)-\frac12\operatorname{Li}_3(1-x)\ln x+C.\tag3
\end{align*} 
 $$
Setting $$x=1$$ to obtain the constant of integration, 
$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_n}{n^3}&=\operatorname{Li}_4(1)-\frac{\pi^2}{12}\operatorname{Li}_2(1)+C\\
\frac{\pi^4}{72}&=\frac{\pi^4}{90}-\frac{\pi^4}{72}+C\\
C&=\frac{\pi^4}{60}.
\end{align*} 
 $$
Thus
$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_nx^n}{n^3}=&\frac12\zeta(3)\ln x-\frac18\ln^2x\ln^2(1-x)+\frac12\ln x\left[\sum_{n=1}^\infty\frac{H_{n} x^{n}}{n^2}-\operatorname{Li}_3(x)\right]\\&+\operatorname{Li}_4(x)-\frac{\pi^2}{12}\operatorname{Li}_2(x)-\frac12\operatorname{Li}_3(1-x)\ln x+\frac{\pi^4}{60}.\tag4
\end{align*} 
 $$
Finally, setting $$x=\frac12$$, we obtain
$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_n}{2^nn^3}=\color{purple}{\frac{\pi^4}{720}+\frac{\ln^42}{24}-\frac{\ln2}8\zeta(3)+\operatorname{Li}_4\left(\frac12\right)},
\end{align*} 
 $$
which matches Cleo's answer.

----------

**References :**

$$[1]\ $$ [Harmonic number](http://mathworld.wolfram.com/HarmonicNumber.html)

$$[2]\ $$ [Polylogarithm](https://en.wikipedia.org/wiki/Polylogarithm)