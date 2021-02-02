---
layout: post
title: integral related to floor function 4
tags:
  - integration   
  - definite-integrals
  - closed-form
  - floor-integral
  - real-analysis
  
description:  
  integral related to floor function 4
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Value of :

$$
\int_{0}^{1}\left( \left\lfloor{\frac{2}{x}} \right\rfloor-2 \left\lfloor{\frac{1}{x}} \right\rfloor \right)dx
$$


<!–-break-–>


# Answer

The function $$\lfloor \frac{2}{x} \rfloor$$ is unbounded near $$x = 0$$ so if you try to split your integral, 
at best you can hope to interpret $$I_1 = \int_0^1 \lfloor \frac{2}{x} \rfloor \, dx$$ as an improper integral. 
Unfortunately, this integral actually diverges (it behaves like $$\int_0^1 \frac{1}{x} \, dx$$) and so is $$I_2$$ 
(this also follows from the calculations below)

Let's see how the integrand (which I will denote by $$f(x)$$) behaves. Divide the interval $$\left( 0, 1 \right]$$ 
into intervals

$$
\cdots, \left( \frac{2}{k+1}, \frac{2}{k} \right],\cdots,\left( \frac{2}{4}, \frac{2}{3} \right], \left( \frac{2}{3}, 1 \right]. 
$$

 1. If $$x \in \left( \frac{2}{k+1}, \frac{2}{k} \right]$$ then $$\frac{2}{x} \in [k,k+1)$$ so $$\lfloor \frac{2}{x} 
 \rfloor = k$$. 
 2. If $$x \in \left( \frac{2}{k+1}, \frac{2}{k} \right]$$ then $$\frac{1}{x} \in [\frac{k}{2},\frac{k+1}{2})$$. 
 Now, if $$k$$ is even then $$2\lfloor \frac{1}{x} \rfloor = 2 \frac{k}{2} = k$$ while if $$k$$ is odd then $$2 \lfloor 
 \frac{1}{x} \rfloor = 2\frac{k-1}{2} = k - 1$$.
 3. Hence, we have for all $$x \in (0,1]$$
 
$$
 f(x) = \lfloor \frac{2}{x} \rfloor - 2 \lfloor \frac{1}{x} \rfloor = \begin{cases} 1 & x \in \left( \frac{1}{l+1}, \frac{2}{2l + 1} \right], l \geq 1, \\
0 & \textrm{otherwise}. \end{cases} 
$$

Hence,

$$
\begin{equation*}
\begin{aligned}
\int_0^1 f(x) \, dx &= \lim_{n \to \infty} \int_{\frac{2}{2n+1}}^1 f(x) \, dx \\
&= \lim_{n \to \infty} \left( \sum_{l=1}^n \left( \frac{2}{2l+1} - \frac{1}{l+1} \right) \right) \\
&= 2 \cdot \sum_{l=1}^{\infty} \left( \frac{1}{2l+1} - \frac{1}{2l+2} \right) \\
&= 2 \sum_{n=3}^{\infty} \frac{(-1)^{n+1}}{n} = 2 \left( \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} - \left( 1 - \frac{1}{2} \right) \right) \\
&= 2 \left( \ln(2) - \frac{1}{2} \right) \\
&= \ln \left( \frac{4}{e} \right) 
\end{aligned}
\end{equation*}
$$

where I used the Taylor series of $$\ln(1 + x)$$ which converges at $$x = 2$$ to $$\ln(2)$$ to evaluate the infinite sum. 
