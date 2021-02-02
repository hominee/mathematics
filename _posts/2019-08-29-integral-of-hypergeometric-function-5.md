---
layout: post
title: integral related to hypergeometric function 5 
tags:
  - integration   
  - definite-integrals
  - closed-form
  - hypergeometric-function
  - real-analysis
  - eulers-constant
  
description:  
  integral related to hypergeometric function 5
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form for :

 
$$   
 
\int_{0}^{\infty}{\ln{x}\over \cosh^{2n}{x}}\mathrm dx 
 
$$   
 

<!–-break-–>


# Answer

Starting from

   $$   
 \zeta(s) = \left(1-\frac{2}{2^s}\right)^{-1}\sum_{n\geq 1}\frac{(-1)^{n+1}}{n^s} \tag{1}
   $$   

then applying the (inverse) Laplace transform and integration by parts, we get:

   $$   
 \int_{0}^{+\infty}\frac{x^s}{\cosh^2(x)}\,dx = \frac{2(2^s-2)\,\Gamma(s+1)}{4^s}\,\zeta(s)=\int_{0}^{1}\text{arctanh}(x)^s\,dx\tag{2} 
   $$   

Your result then follows from integration by parts and

   $$   
 \int_{0}^{+\infty}\frac{\log x}{\cosh^2(x)}\,dx = \left.\frac{d}{ds}\left(\frac{2(2^s-2)\Gamma(s+1)\zeta(s)}{4^s}\right)\right|_{s=0}=-\gamma+\log\frac{\pi}{4}.\tag{3}
   $$   
