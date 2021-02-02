---
layout: post
title: sum related to trigonometric function 2
tags:
  - sum  
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  sum related to trigonometric function 2
  
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :

$$

\int_{0}^{\infty}\sin\left({1\over 4x^2}\right)\ln x\cdot{\mathrm dx\over x^2}=-\sqrt{\pi\over 2}\cdot\left({\pi-2\gamma \over 4}\right)

$$


<!–-break-–>

Consider these two similar integrals


$$
\int_{0}^{\infty}\sin\left({1\over 4x^2}\right)\ln x\cdot{\mathrm dx\over x^2}=-\sqrt{\pi\over 2}\cdot\left({\pi-2\gamma \over 4}\right)\tag1
$$



$$
\int_{0}^{\infty}\sin\left({1\over 4x^2}\right)\ln^2x\cdot{\mathrm dx\over x^2}=\sqrt{\pi\over 2}\cdot\left({\pi-2\gamma \over 4}\right)^2\tag2
$$


How does one prove $$(1)$$ and $$(2)$$?

# Answer

Recall

$$
 \int_0^\infty u^te^{-su}du=\frac{\Gamma(t+1)}{s^{t+1}}. 
$$

So
\begin{eqnarray*}
&&\int_{0}^{\infty}u^{t}\sin u\mathrm du\\
&=&\lim_{\epsilon\to0^+}\Im \int_{\epsilon}^{\infty}u^{t} e^{iu}\mathrm du=\Im \frac{\Gamma(t+1)}{(-i)^{t+1}}\\
&=&\Im \Gamma(t+1)(i)^{t+1}=\Gamma(t+1)\sin(\frac{(t+1)\pi}{2}).
\end{eqnarray*}
Let

$$
 I(a)=\int_0^{\infty}x^{-a}\sin(\frac1{4x^2})dx 
$$

and then

$$
I(a)=-2^{-2+a}\int_0^{\infty}u^{\frac{-3+a}2}\sin udu=-2^{a-2}\sin(\frac{(a-1)\pi}{4})\Gamma(\frac{a-1}{2}). 
$$

So

$$
\begin{eqnarray*}
I'(2)&=-2^{a-2}\ln2\sin(\frac{(a-1)\pi}{4})\Gamma(\frac{a-1}{2})-2^{a-4}\pi\cos(\frac{(a-1)\pi}{4})\Gamma(\frac{a-1}{2})-2^{a-3}\sin(\frac{(a-1)\pi}{4})\Gamma'(\frac{a-1}{2})\bigg|_{a=2}\\
&=-\ln2\cdot\frac1{\sqrt2}\sqrt{\pi}-\frac\pi 4\frac{1}{\sqrt2}\sqrt\pi-\frac{1}{2\sqrt2}\Gamma'(\frac12)
\end{eqnarray*}
$$

Noting

$$
 \frac{\Gamma'(z+1)}{\Gamma(z+1)}=-\gamma+\sum_{n=1}^\infty\left(\frac{1}{n}-\frac{1}{z+n}\right)
$$

one has

$$
 \Gamma'(\frac12)=\Gamma(\frac12)\left[-\gamma+\sum_{n=1}^\infty\left(\frac{1}{n}-\frac{1}{n-\frac12}\right)\right]=\sqrt{\pi}(-\gamma-2\ln2).
$$

Thus

$$
 I'(2)=-\sqrt{\pi\over 2}\left({\pi-2\gamma \over 4}\right). 
$$

You can treat $$I''(2)$$ in the same way and the calculation will be longer.