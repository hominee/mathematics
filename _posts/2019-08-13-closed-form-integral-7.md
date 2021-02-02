---
layout: post
title: Closed form integral 7
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
  - real-analysis
  
description:  
  Closed form integral 7
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of 

$$
\int_0^1 \frac{\operatorname{Li}_s(x-x^2)}{x-x^2}\ dx
$$

<!–-break-–>

# Answer

An expression as a generalized hypergeometric function can be directly obtained by expressing the ratio 
of two consecutive terms in the series which defines $$F(s)$$ as a rational fraction in $n$ allowing thus 
to express the series as a generalized hypergeometric series. 

Alternatively, starting from the integral, 

$$
\begin{equation*}
\begin{aligned}
   F(s)&=\int_0^{1/2}\frac{\mathrm{Li}_{s}(x-x^2)}{x-x^2}\,dx+\int_{1/2}^1\frac{\mathrm{Li}_{s}(x-x^2)}{x-x^2}\,dx\\
   &=2\int_0^{1/2}\frac{\mathrm{Li}_{s}(x-x^2)}{x-x^2}\,dx\\
   &=2\int_0^{1/4}\frac{\mathrm{Li}_{s}(t)}{t}\frac{dt}{\sqrt{1-4t}}\\
   &=2\int_0^{1}\frac{\mathrm{Li}_{s}(\frac{u}{4})}{u}\frac{du}{\sqrt{1-u}}
\end{aligned}
\end{equation*}
$$

(we changed $$x\to 1-x$$ n the second integral of the first expression, then $$t=x(1-x)$$ and 
finally $$t=u/4$$). Now, if $$s$$ is an integer, we use the  representation in terms of the hypergeometric 
function ([here](https://en.wikipedia.org/wiki/Polylogarithm#Series_representations))

$$
\begin{equation*}
 \mathrm{Li}_s(z)=z_{s+1} F_s\left( 1,1,\ldots,1;2,2,\ldots,2;z \right)
\end{equation*} 
$$

to obtain

$$
\begin{equation*}
 F(s)=\frac{1}{2}\int_0^{1}\left( 1-u \right)^{-1/2}{}_{s+1}F_s\left( 1,1,\ldots,1;2,2,\ldots,2;\frac{u}{4} \right)\,du
\end{equation*} 
$$

Then, from the tabulated integral ([DLMF](https://dlmf.nist.gov/16.5.E2)),

$$
\begin{equation*}
 _{p+1} F_{q+1} \left(a_{0},\dots,a_{p}\atop b_{0},\dots,b_{q};z\right)=%
\frac{\Gamma\left(b_{0}\right)}{\Gamma\left(a_{0}\right)\Gamma\left(b_{0}-a_{0%
}\right)}\int_{0}^{1}t^{a_{0}-1}(1-t)^{b_{0}-a_{0}-1}   {}_{p}F_{q} \left({a_{1}%
,\dots,a_{p}\atop b_{1},\dots,b_{q}};zt\right)\mathrm{d}t
\end{equation*} 
$$

valid for $$\Re b_0>\Re a_0>0$$ if $$p\le q$$ and, additionally, $$\left|\mathrm{ph}(1-z)\right|<\pi$$
 if $$p=q+1$$. Here $$a_0=1,b_0=3/2,z=1/4$$, thus
 
 $$
\begin{equation*}
 F(s)={}_{s+2}F_{s+1}\left( 1,1,\ldots,1;\frac{3}{2},2,2,\ldots,2;\frac{1}{4} \right)
\end{equation*} 
$$