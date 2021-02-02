---
layout: post
title: sum related to zeta function 1
tags:
  - sum
  - closed-form
  - real-analysis
  - zeta-function
  
description:  
  sum related to zeta function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :

 
$$
 
 \sum_{n=1}^{\infty}{\zeta(2n+1)\over (2n+1)2^{4n}} 
 
$$


<!–-break-–>
 

We was able to determine $$(1)$$ to have this closed form 


$$
\ln(2)-\gamma=\sum_{n=1}^{\infty}{\zeta(2n+1)\over (2n+1)2^{2n}}\tag1
$$


then we when on and try to evaluate $$(2)$$ and we only half of the closed form


$$
2\ln(2)-\gamma-2X=\sum_{n=1}^{\infty}{\zeta(2n+1)\over (2n+1)2^{4n}}\tag2
$$


Where
 
$$
X=\sum_{n=0}^{\infty}{\eta(2n+1)\over(2n+1)2^{2n+1}}\tag3
$$


where $$\eta$$ is the [Dirichlet eta function][1] and $$\gamma$$ is [Euler-Masheroni constant][2]

**How do we evaluate the closed form of $$(3)?$$**


  [1]: https://en.wikipedia.org/wiki/Dirichlet_eta_function
  [2]: https://en.wikipedia.org/wiki/Euler%E2%80%93Mascheroni_constant


# Answer

We have the following Lemma (a sketch of a proof can be found below)


$$

s(x)=\sum_{n\geq 1}(-x)^n \zeta(n+1)=-\gamma-\psi(1+x)\quad \color{red}{(I)}

$$


where $$\psi(z)=\frac{d\log(\Gamma(z))}{dz}$$ is the digamma function and $$\gamma$$ is Euler's constant


Integrating yields


$$

S(x)=\int dx s(x)=\sum_{n\geq1}\frac{\zeta(n+1)}{n+1}(-x)^{n+1}=-\gamma x-\log(\Gamma(1+x))

$$


Taking the odd part

$$

S(x)-S(-x)=2\sum_{n\geq1}\frac{\zeta(2n+1)}{2n+1}x^{2n+1}=-2\gamma x-\log(\Gamma(1+x))+\log(\Gamma(1-x))

$$


Now let us put $$x=\frac{1}{4}$$ we get

$$

\sum_{n\geq1}\frac{\zeta(2n+1)}{2n+1}\frac1{4^{2n}}=-\gamma+2\log\left(\frac{\Gamma(3/4)}{\Gamma(5/4)}\right)

$$



which is the sum of OP's interest

---

We now proof $$\color{red}{(I)}$$:

Use the definition of the $$\zeta$$-function as a series and exchange the order of summation. Doing the first sum yields $$S(x)=\sum_{k\geq1}\frac{1}{x+k}-\frac{1}k$$ [expressing this in terms of Digamma functions][1] yields $$\color{red}{(I)}$$. 


  [1]: https://en.wikipedia.org/wiki/Digamma_function