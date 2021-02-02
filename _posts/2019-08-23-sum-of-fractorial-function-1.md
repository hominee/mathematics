---
layout: post
title: sum related to factorial function 1
tags:
  - sum
  - closed-form
  - real-analysis
  - gamma-function
  - factorial-function
  
description:  
  sum related to factorial function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :
 
 
 $$ 
 
\sum_{n=0}^\infty \frac{1}{(kn)!}
 
 $$ 

There seem to be rather nice values for low integer values for $$x$$, as follows:

 $$ 
\begin{array}{|c|c|}
\hline
x & \displaystyle\sum_{n=0}^\infty {1\over (xn)!} \\[1ex]
\hline
1 & e \\[2ex]
2 & \cosh(1) \\[2ex]
3 & \displaystyle{e^{3/2} + 2\cos\frac{\sqrt 3}{2} \over 3 \sqrt e} \\[2ex]
4 & \displaystyle\frac12(\cos1+\cosh1)\\
\hline
\end{array}
 $$ 


(These were verified with WolframAlpha.)

Is there any closed form for this, or some other function that it can be expressed in?

<!–-break-–>


# Answer

In 1903, the Swedish mathematician [Gösta Mittag-Leffler][1] introduced the following [special function][2]:

 $$ 

  E_\alpha(z)=\sum_{n=0}^{\infty}\frac{z^n}{\Gamma(\alpha n+1)},

 $$ 

where $$z$$ is a complex number, $$\Gamma$$ is the [gamma function][3] and $$\alpha \geq 0$$. The [Mittag-Leffler function][4] is a direct generalization of the [exponential function][5] to which it reduces for $$\alpha = 1$$. You can find more details about the function in this [survey article][6].

We can express your sum in terms of the Mittag-Leffler function as the following. For a positive integer $$k$$, we have


 $$ 

\sum_{n=0}^\infty \frac{1}{(kn)!} = E_k(1).

 $$ 


Note that for a positive integer $$n$$, we have $$\Gamma(n) = (n-1)!$$


  [1]: https://en.wikipedia.org/wiki/G%C3%B6sta_Mittag-Leffler
  [2]: http://mathworld.wolfram.com/SpecialFunction.html
  [3]: http://mathworld.wolfram.com/GammaFunction.html
  [4]: http://mathworld.wolfram.com/Mittag-LefflerFunction.html
  [5]: http://mathworld.wolfram.com/ExponentialFunction.html
  [6]: https://arxiv.org/abs/0909.0230