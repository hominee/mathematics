---
layout: post
title: Identification of a function
tags:
  - polylogarithm
  - calculus
  - functions
  - sequences and series
description: >
  Identification of a function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

I recently came across the following function

$$\sum_{k=1}^\infty(\log(k))^n\frac{z^k}{k}$$

I found it while dealing with the polylogarithm function, $$Li_n (z)$$ (Notice that if instead of $$(\log(k))^n$$ we had $$k^n$$ then the above expression would become $$Li_{1-n}(z)$$. Still these functions are quite different.) 

I was wondering if this function is known, and if there are good numerical approximations to estimate it?

<!–-break-–>

# Answer

Your sum can be expressed in term of derivatives of a polylogarithm with respect to order. 
For all $$|z|< 1 $$, we have:

$$
\begin{equation*}
\begin{aligned}
 (-1)^n\frac{ \partial^n}{\partial s^n} \left.\operatorname{Li}_s(z)\right|_{s=1} 
 &= (-1)^n \frac{\partial^n}{\partial s^n} \left.\left(\sum_{k=1}^\infty \frac{z^k}{k^s}\right)\right|_{s=1} \\ 
 &= (-1)^n \sum_{k=1}^\infty z^k \frac{\partial^n}{\partial s^n}\left.\left(\frac{1}{k^s}\right)\right|_{s=1} \\ 
 &= (-1)^n \sum_{k=1}^\infty z^k\left.\left(\frac{(-1)^n\log^n(k)}{k^s}\right)\right|_{s=1} \\ 
 &= \sum_{k=1}^\infty \frac{z^k \log^n(k)}{k}.
\end{aligned}
\end{equation*}
$$