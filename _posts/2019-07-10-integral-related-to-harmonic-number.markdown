---
layout: post
title: sum related to harmonic number
tags:
  - sum 
  - closed-form
  - harmonic number
  - real-analysis
  
description:  
  sum related to harmonic number
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :


$$


\sum_{n=1}^{\infty}\left[H_n^2-\left(\log n+\gamma+\frac{1}{2n}\right)^2\right]


$$




<!–-break-–>



# Answer

Just some considerations for now.

[here][1] that


$$
 \sum_{n=1}^{N}H_n^2 = (N+1) H_N^2-(2N+1)H_N+2N  \tag1 
$$


and we have:


$$

 \mathcal{L}^{-1}\left(\frac{\log x+\gamma}{x}\right)(s)=-\log(s)\tag{2} 

$$




$$

 \mathcal{L}^{-1}\left(\frac{\left(\log x+\gamma\right)^2}{x}\right)(s)=-\zeta(2)+\log^2(s)\tag{3} 

$$


hence the partial sums of the given series can be rearranged as follows:



$$

\begin{eqnarray*}\sum_{n=1}^{N}\left[H_n^2-\left(\log n+\gamma+\frac{1}{2n}\right)^2\right]&=&(\color{blue}{1})-\frac{H_N^{(2)}}{4}-\sum_{n=1}^{N}\frac{\log n+\gamma}{n}-\sum_{n=1}^{N}n\frac{(\log n+\gamma)^2}{n}\\&=&(\color{blue}{1})-\frac{H_N^{(2)}}{4}+\int_{0}^{+\infty}\frac{\log(s)(1-e^{-Ns})}{e^s-1}\,ds\\&-&\int_{0}^{+\infty}\frac{e^{-N s} \left(e^{(1+N) s}+N-e^s (1+N)\right)\left(\zeta(2)-\log^2 s\right)}{\left(-1+e^s\right)^2}\,ds\end{eqnarray*}

$$



If we find a way to distribute $$(\color{blue}{1})$$ over the last two integrals, in a way ensuring they are convergent integrals as $$N\to +\infty$$, we are done. At first sight the closed form of the LHS appears to be related with $$\zeta(2)$$, $$\zeta'(0)=-\frac{1}{2}\log(2\pi)$$ and


$$

 \zeta''(0)=\frac{\gamma^2}{2}-\frac{\pi ^2}{24}-\frac{1}{2}\log^2(2\pi)+\gamma_1

$$


with $$\gamma_1$$ being a [Stieltjes constant][2]. An alternative, brute-force way is just to compute the asymptotic expansions of


$$

 \sum_{n=1}^{N}\log^2(n),\qquad \sum_{n=1}^{N}\frac{\log(n)}{n} 

$$


with the sufficient degree of accuracy (I guess that to stop at the $$O\left(\frac{1}{N^3}\right)$$ term is enough), that is just a tedious exercise about summation by parts. 


  [1]: https://math.stackexchange.com/a/933714/44121
  [2]: https://en.wikipedia.org/wiki/Stieltjes_constants