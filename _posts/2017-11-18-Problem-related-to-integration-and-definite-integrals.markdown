---
layout: post
title: Problem related to integration and definite integrals
tag:
 - integration
 - definite-integrals

description: Problem related to integration and definite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Evaluate $$ \int_{-\pi/2}^{\pi/2} \frac{\cos(x)}{1+e^x} dx$$ 

<!–-break-–>



# Answer 


As $$\displaystyle\int_a^bf(x)dx=\int_a^bf(a+b-x)dx$$
if $$\displaystyle f(x)=\frac{\cos x}{1+e^x}, f\left[\frac\pi2+\left(-\frac\pi2\right)-x\right]=\frac{\cos(-x)}{1+e^{-x}}=\frac{e^x\cos x}{1+e^x}$$


$$

I=\int_{-\frac\pi2}^{\frac\pi2}\frac{\cos x}{1+e^x}dx=\int_{-\frac\pi2}^{\frac\pi2}\frac{e^x\cos x}{1+e^x}dx

$$




$$

\implies I+I=\int_{-\frac\pi2}^{\frac\pi2}\cos x\ dx

$$



