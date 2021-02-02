---
layout: post
title: Bounding the Gamma Function
tag:
 - special-functions
 - gamma-function

description: Bounding the Gamma Function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Bounding the Gamma Function

<!–-break-–>


we are  trying to verify a bound for the gamma function

 $$ 
 \Gamma(z) = \int_0^\infty e^{-t}t^{z - 1}\;dt. 
 $$ 

we n particular, for real $$m \geq 1$$, we 'd like to show that

 $$ 
 \Gamma(m + 1) \leq 2\left(\frac{3m}{5}\right)^m. 
 $$ 

Knowing that the bound should be attainable, my first instinct is to split the integral as

 $$ 
 \Gamma(m + 1) = \int_0^{3m/5} e^{-t}t^{m}\;dt + \int_{3m/5}^\infty e^{-t}t^m\;dt
\leq (1 - e^{-3m/5})\left(\frac{3m}{5}\right)^m + \int_{3m/5}^\infty e^{-t}t^m\;dt. 
 $$ 

Using integration by parts,

 $$ 
 \int_{3m/5}^\infty e^{-t}t^m\;dt = e^{-3m/5}\left(\frac{3m}{5}\right)^m + m\int_{3m/5}^\infty e^{-t}t^{m-1}\;dt.
 $$ 

So the problem has been reduced to showing

 $$ 
 m\int_{3m/5}^\infty e^{-t}t^{m-1}\;dt \leq \left(\frac{3m}{5}\right)^m. 
 $$ 

But this doesn't seem to have made the problem any easier.

# Answer 


Suppose $$m = n + \alpha$$ where $$0 \le \alpha < 1$$, so that $$\alpha$$ is the fractional part of $$m$$. Taking logarithms, the inequality becomes

 $$ 
 \sum_{k=1}^n \log (k + \alpha) + \log \Gamma (1+\alpha) <
\log 2 + (n+\alpha) \log (n+\alpha) + (n+\alpha) \log \frac{3}{5} 
 $$ 

Now using Riemann sums, we have

 $$ 
 \sum_{k=1}^n \log (k + \alpha) < \int_1^{n+1} \log(x+\alpha) dx
 $$ 

which is

 $$ 
 (n+1+\alpha) \log (n+1+\alpha) - n - 1 - (1+\alpha) \log(1+\alpha) + 1.
 $$ 

This means we need to show that

 $$ 
 (n+1+\alpha) \log (n+1+\alpha) - n - (1+\alpha) \log(1+\alpha) + \log \Gamma (1+\alpha) < \log 2 + (n+\alpha) \log (n+\alpha) + (n+\alpha) \log \frac{3}{5} 
 $$ 

Rearranging terms, this is

 $$ 
 (n+1+\alpha) \log (n+1+\alpha) -  (n+\alpha) \log (n+\alpha) <
\log 2 - \log \Gamma (1+\alpha) + (n+\alpha) \log \frac{3}{5} + n + (1+\alpha) \log(1+\alpha)
 $$ 

Now for the LHS we have

 $$ 
 \log (n+1+\alpha) + \log \left( 1 + \frac{1}{n+\alpha}\right)^{n+\alpha} <
\log (n+1+\alpha) + 1
 $$ 

because $$ \log \left( 1 + \frac{1}{x}\right)^x < 1$$ by a trivial calculation.
On the RHS we have

 $$ 
 n \log\frac{3e}{5} + \log 2 - \log \Gamma (1+\alpha) + \alpha \log \frac{3}{5}  + (1+\alpha) \log(1+\alpha) > \log (n+1+\alpha) + 1
 $$ 

for all $$n > n_0$$ for some $$n_0$$ because the coefficient $$\log\frac{3e}{5}$$ on $$n$$ is positive and the remaining terms are bounded by a constant. This concludes the proof. Note that the proof also goes through with a factor of $$\frac{2}{5}$$, just barely, and requiring $$n_0 = 22.$$ The original post has $$n_0 = 1.$$
we are  not sure of all the details but we  hope it's a start.

