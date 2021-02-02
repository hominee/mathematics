---
layout: post
title: integral related to floor function 5
tags:
  - integration   
  - definite-integrals
  - closed-form
  - floor-integral
  - real-analysis
  
description:  
  integral related to floor function 5
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Value of :

$$
\int_{0}^{1} \left(-1\right)^{\large ^{\left\lfloor\frac{1}{x}\right\rfloor}}  \mathrm{d}x
$$


<!–-break-–>


# Answer

write 

$$
\begin{equation*}
\begin{aligned}
\int_{0}^{1} \left(-1\right)^{\large ^{\left\lfloor\frac{1}{x}\right\rfloor}}  \mathrm{d}x &= \sum_{k=1}^{\infty}\int_{\frac{1}{k+1}}^{\frac{1}{k}}  \left(-1\right)^{\large ^{\left\lfloor\frac{1}{x}\right\rfloor}}  \mathrm{d}x  \\
&= \sum_{k=1}^{\infty} \int_{k}^{k+1} \left(-1\right)^{\large ^{\left\lfloor u\right\rfloor}} \, \frac{\mathrm{d} u}{u^{2}} \\
&= \sum_{k=1}^{\infty} \int_{k}^{k+1} \left(-1\right)^{{k}} \, \frac{\mathrm{d} u}{u^{2}} \\
&= \sum_{k=1}^{\infty}\frac{\left(-1\right)^{k}}{k (k+1)} \\
&=  \sum_{k=1}^{\infty}\frac{\left(-1\right)^k}{k}+\sum_{k=1}^{\infty}\frac{\left(-1\right)^{k+1}}{k+1}\\
&=-\log 2-\log 2+1
\end{aligned}
\end{equation*}
$$

where we have used the standard identity

$$
\log(1+x)=-\sum_{k=1}^{\infty}\frac{\left(-1\right)^k}{k}x^k, \quad |x|<1,
$$ 

when  $$x \to 1^-$$ (via [Abel's theorem][1]).

Finally,

$$
\int_{0}^{1} \left(-1\right)^{\large ^{\left\lfloor\frac{1}{x}\right\rfloor}}  \mathrm{d}x  
= 1-2 \log 2.
$$


  [1]: https://en.wikipedia.org/wiki/Abel's_theorem