---
layout: post
title: sum related to hypergeometric function 1
tags:
  - sum  
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  sum related to hypergeometric function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :
 
 
$$
 
\sum_{n=0}^{\infty}\frac{2^nn[n(\pi^3+1)+\pi^2](n^2+n-1)}{(2n+1)(2n+3){2n \choose n}}=1+\pi+\pi^2+\pi^3+\pi^4
 
$$
 


<!–-break-–>


# Answer

Generally the following sums may help:

$$
\sum_{n=0}^\infty\frac{x^n}{\binom{2n}{n}}=4 \left(\frac{1}{4-x}+\frac{\sqrt{x} \arcsin\left(\frac{\sqrt{x}}{2}\right)}{(4-x)^{3/2}}\right)
$$


$$
\sum_{n=0}^\infty\frac{nx^n}{\binom{2n}{n}}=\frac{\partial}{\partial x}\sum_{n=0}^\infty\frac{x^{n+1}}{\binom{2n}{n}}-\sum_{n=0}^\infty\frac{x^{n}}{\binom{2n}{n}}
$$


$$

\sum_{n=0}^\infty\frac{x^n}{\binom{2n}{n}(2n+1)}=\frac{4 \arcsin \left(\frac{\sqrt{x}}{2}\right)}{\sqrt{(4-x) x}}

$$


$$

\sum_{n=0}^\infty\frac{x^n}{\binom{2n}{n}(2n+3)}=-\frac{4 \left(2 \sqrt{(4-x) x}+(x-8) \sin ^{-1}\left(\frac{\sqrt{x}}{2}\right)\right)}{\sqrt{4-x} x^{3/2}}
$$


Derivation of the third line from the first is as follows:

$$

\sum_{n=0}^\infty\frac{x^n}{\binom{2n}{n}}=f(x)

$$


$$

C+\sum_{n=0}^\infty\frac{x^{n}}{\binom{2n}{n}(2n+3)}=\frac{1}{x^3}\int\sum_{n=0}^\infty\frac{x^{n+2}}{\binom{2n}{n}}\mathrm{d}x=\frac{1}{x^3}\int f(x)x^2\mathrm{d}x

$$

Where $$C$$ should be matched to the value at $$x=0$$+ there are some convergence criteria that should be checked. Also 

$$

\frac{n[n(y^3+1)+y^2](n^2+n-1)}{(2n+1)(2n+3)}=\frac{1}{2}\frac{n[n(y^3+1)+y^2](n^2+n-1)}{(2n+1)}-\frac{1}{2}\frac{n[n(y^3+1)+y^2](n^2+n-1)}{(2n+3)}

$$

And then:

$$

\frac{1}{2}\frac{n[n(y^3+1)+y^2](n^2+n-1)}{(2n+1)}=\frac{n^3 \left(8 y^3+8\right)+n^2 \left(-4 y^3+8 y^2-4\right)+n \left(-2 y^3-4 y^2-2\right)+3 y^3-2 y^2+3}{32}+\frac{-9y^3+6y^2-9}{2n+1}

$$


Applying these, and a few more similarly obtained formulas,  may help. There might be a better approach, with less calculation. (and there may be some mistakes). Finally plug in $$x=2$$ and $$y=\pi$$