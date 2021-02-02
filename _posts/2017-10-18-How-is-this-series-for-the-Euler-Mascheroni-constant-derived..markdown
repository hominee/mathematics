---
layout: post
title: How is this series for the Euler-Mascheroni constant derived.
tag:
 - sequences-and-series
 - limits

description: How is this series for the Euler-Mascheroni constant derived.

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How is this series for the Euler-Mascheroni constant derived?.

<!–-break-–>


We are familiar with the classic sum for Euler's constant $$\gamma$$:


$$

 \gamma=\lim_{n\to \infty}\left(\sum_{k=1}^{n}\frac{1}{k}-\ln(n)\right) .


$$


But, how is this one derived?:


$$

 \gamma=\lim_{n\to \infty}\left(\frac12\sum_{k=1}^{\infty}\frac{(-1)^{k+1}}{k(2k)!}n^{2k}-\ln(n)\right) .


$$


we thought perhaps it may have something to do with the Bernoulli numbers or even Zeta because there are terms which appear in their identities (such as the formula for $$\zeta(2n)$$), but we are  not sure.

Thanks for any input.
 
.


# Answer 


Consider $$\sin^2\left(\frac{n}{2} \right)$$:


$$


  \sin^2\left(\frac{n}{2} \right) = \frac{1-\cos(n)}{2} = \sum_{k=1}^\infty \frac{(-1)^{k+1}}{2 \cdot (2k)!} n^{2k}


$$


Now, since $$\frac{n^{2k}}{2 k} = \int\limits_0^n t^{2k-1} \mathrm{d} t$$, we get:


$$


   \sum_{k=1}^\infty \frac{(-1)^{k+1}}{(2k)!} \frac{n^{2k}}{2 k} = \int_0^n \frac{1-\cos(t)}{t} \mathrm{d} t


$$


The latter integral gives, by the definition of the cosine integral:


$$


 \int_0^n \frac{1-\cos(t)}{t} \mathrm{d} t = \gamma + \log(n) - \operatorname{Ci}(n)


$$


In order to get a sense of why Euler-Mascheroni constant $$\gamma$$ appears here, consider another definition of cosine integral (in which it is manifest that $$\lim_{x \to \infty} \operatorname{Ci}(x) = 0$$):


$$


   \operatorname{Ci}(n) = -\int_{n}^\infty \frac{\cos(t)}{t} \mathrm{d} t


$$


Both definitions fulfill $$\operatorname{Ci}^\prime(x) = \frac{\cos(x)}{x}$$. In order to establish that the integration constant is indeed the Euler-Mascheroni constant, we consider $$n=1$$:


$$

 


$$
\begin{eqnarray*}

   \gamma &=& \int_0^1 \frac{1 - \cos(t)}{t} \mathrm{d} t - \int_1^\infty \frac{\cos(t)}{t} \mathrm{d} t = \Re\left( \int_0^\infty \frac{[0<\|t\|<1]-\mathrm{e}^{i t}}{t} \mathrm{d} t \right) \\
   &\stackrel{t \to i t}{=}& \Re\left( \int_0^\infty \frac{[0<\|t\|<1]-\mathrm{e}^{-t}}{t} \mathrm{d} t \right) \stackrel{\text{by parts}}{=} 
  \Re\left( -\int_0^\infty \mathrm{e}^{-t} \ln(t) \mathrm{d} t \right) = \gamma

\end{eqnarray*}


$$


$$

 
The last equality follows from the definition of the constant.

