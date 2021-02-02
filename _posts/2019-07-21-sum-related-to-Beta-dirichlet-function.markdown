---
layout: post
title: sum related to Beta dirichlet function
tags:
  - sum  
  - closed-form
  - Beta-dirichlet-function
  - real-analysis
  
description:  
  sum related to Beta dirichlet function
  
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :

$$

\sum_{n=1}^{\infty}(-1)^{n-1}\left({\beta(n)\over n}-\ln{n+1\over n}\right)=\ln\sqrt{2\over \pi}\cdot{2\over \Gamma^2\left({3\over 4}\right)}

$$

 
<!–-break-–>


# Answer

Let us consider the two sums separately:

$$

S_1 = \sum_{n=1}^\infty (-1)^{n-1}\frac{\beta(n)}{n} \\
S_2 = \sum_{n=1}^\infty (-1)^{n-1}\ln\frac{n+1}{n}

$$


For $$S_1$$, let us first consider the related sum, for which $$S_1$$ is the limiting value $$S(1)$$:

$$
S(x) = \sum_{n=1}^\infty (-1)^{n-1}\frac{\beta(n)x^n}{n} \\
S'(x) = \sum_{n=1}^\infty (-1)^{n-1}\beta(n)x^{n-1} = \sum_{n=1}^\infty (-1)^{n-1}x^{n-1}\sum_{k=0}^\infty \frac{(-1)^k}{(2k+1)^n} \\
= \sum_{k=0}^\infty \frac{(-1)^k}{2k+1} \sum_{n=1}^\infty \left( \frac{-x}{2k+1} \right)^{n-1} = \sum_{k=0}^\infty \frac{1}{2k+1+x} = \frac{1}{2} \Phi \left(-1, 1, \frac{1+x}{2} \right)
$$

Where $$ \Phi $$ is the Lerch Transcendent, 
and $$ \mid x \mid <1 $$. Now, upon integration, we can recover $$S_1$$:

$$
S_1 - S(0) =\int_0^1 S'(x) dx = \int_0^1 \frac{1}{2} \Phi \left(-1, 1, \frac{1+x}{2} \right)dx = \int_\frac{1}{2}^1 \Phi (-1, 1, x)dx \\
= \lim_{s\to0}\int_\frac{1}{2}^1 \Phi (-1, 1+s, x)dx = \lim_{s\to0} \left[ \frac{-1}{s}\Phi (-1, s, x) \right|_\frac{1}{2}^1 \\
= \lim_{s\to0} \frac{\Phi \left(-1, s, \frac{1}{2}\right) - \Phi(-1, s, 1)}{s} = \lim_{s\to0} \frac{2^s \beta(s) - \eta(s)}{s} \\
=^H \lim_{s\to0} \ \ln(2) 2^s \beta(s) + 2^s \beta'(s) - \eta'(s) = \frac{1}{2} \ln(2) + \ln \frac{\Gamma^2(\frac{1}{4})}{2 \pi \sqrt{2}} - \frac{1}{2} \ln \frac{\pi}{2} = \ln \frac{\sqrt{2 \pi}}{\Gamma^2(\frac{3}{4})}
$$

And as $$S(0) = 0$$, this is all $$S_1$$. For $$S_2$$:

$$
S_2 = \sum_{n=1}^\infty (-1)^{n-1}\ln\frac{n+1}{n} = \ln \prod_{n=1}^\infty \left( \frac{n+1}{n} \right)^{(-1)^{n-1}} \\
= \lim_{N \to \infty} \ln \prod_{n=1}^N \frac{n^2}{(n - \frac{1}{2})(n + \frac{1}{2})} = \lim_{N \to \infty} \ln\frac{\pi \Gamma^2(N+1)}{2\Gamma(N + \frac{1}{2})\Gamma(N + \frac{3}{2})} = \ln \frac{\pi}{2}
$$

The sum therefore equals:

$$

S_1-S_2=\ln \frac{2\sqrt2}{\sqrt{\pi} \ \Gamma^2(\frac{3}{4})}

$$

as predicted.