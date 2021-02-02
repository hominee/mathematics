---
layout: post
title: integral related to floor function 1
tags:
  - integration   
  - definite-integrals
  - closed-form
  - Riemann-integral
  - floor-integral
  - real-analysis
  
description:  
  integral related to floor function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :

$$

\int_0^1 \left(\left\lfloor\frac{\alpha}{x}\right\rfloor-\alpha\left\lfloor\frac{1}{x}\right\rfloor\right)\mathrm dx=\alpha \ln\alpha
$$


<!–-break-–>


# Answer

The ***improper*** integral can be evaluated as the limit of an integral over $$[1/n,1] $$ as $$n \to \infty,$$

Making the change of variables $$u = 1/x,$$ we get 

$$
\alpha\int_{1/n}^1 \left\lfloor\frac{1}{x}\right\rfloor dx = \alpha\int_{1}^{n } \frac{\left\lfloor u\right\rfloor}{u^2} \, du  \\ = \alpha \sum_{k=1}^{n-1}\int_{k}^{k+1 } \frac{\left\lfloor u\right\rfloor}{u^2} \, du \\ = \alpha \sum_{k=1}^{n-1}\int_{k}^{k+1 } \frac{k}{u^2} \, du  \\ = \alpha \sum_{k=1}^{n-1} k\left(\frac{1}{k} - \frac{1}{k+1} \right) \\ = \alpha \sum_{k=2}^{n} \frac{1}{k},\tag{1}
$$

and, making the change of variables $$u = \alpha/x,$$ we get

$$
\int_{1/n}^1 \left\lfloor\frac{\alpha}{x}\right\rfloor dx= \alpha \int_{\alpha}^{n \alpha} \frac{\left\lfloor u\right\rfloor}{u^2} \, du \\ = \alpha \int_{\alpha}^{n} \frac{\left\lfloor u\right\rfloor}{u^2} \, du  - \alpha \int_{n \alpha}^{n} \frac{\left\lfloor u\right\rfloor}{u^2} \, du \\ = \alpha \int_{1}^{n} \frac{\left\lfloor u\right\rfloor}{u^2} \, du  - \alpha \int_{n \alpha}^{n } \frac{\left\lfloor u\right\rfloor}{u^2} \, du\tag{2}
$$

Subtracting (1) from (2) we eliminate the divergent harmonic sum and obtain

$$
\int_{1/n}^1 \left(\left\lfloor\frac{\alpha}{x}\right\rfloor - \alpha \left\lfloor\frac{1}{x}\right\rfloor \right) dx = - \alpha \int_{n \alpha}^{n} \frac{\left\lfloor u\right\rfloor}{u^2} \, du \\ = - \alpha \int_{1}^{n} \frac{\left\lfloor u\right\rfloor}{u^2} \, du + \alpha \int_{1}^{\lfloor n \alpha \rfloor} \frac{\left\lfloor u\right\rfloor}{u^2} \, du + \alpha \int_{\lfloor n \alpha \rfloor}^{n \alpha} \frac{\left\lfloor u\right\rfloor}{u^2} \, du \\ = -\alpha \sum_{k=2}^{n} \frac{1}{k} + \alpha \sum_{k=2}^{\lfloor n \alpha \rfloor}\frac{1}{k} + \alpha \frac{n \alpha - \lfloor n \alpha \rfloor}{n \alpha} \\ = -\alpha \left(\sum_{k=1}^{n} \frac{1}{k} - \log n \right)  + \alpha \left( \sum_{k=1}^{\lfloor n \alpha \rfloor}\frac{1}{k} - \log\lfloor n \alpha \rfloor \right) - \alpha \log n + \alpha \log \lfloor n \alpha \rfloor  + \alpha \frac{n \alpha - \lfloor n \alpha \rfloor}{n \alpha}
$$

From here, it should be relatively straightforward to take the limit as $$ n \to \infty$$ to obtain $$\alpha \log \alpha $$.
