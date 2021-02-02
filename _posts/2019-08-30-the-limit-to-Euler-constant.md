---
layout: post
title: limit to eulers constant
tags:
  - limit 
  - eulers-constant
  - real-analysis
  - zeta-functions
  
description:  
  limit to eulers constant
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that:

$$
\gamma=\lim\limits_{n \to \infty}\left(\sum\limits_{k=1}^{n}{\zeta(2k)\over k}\right)-\ln(2n) 
$$
 
<!–-break-–>

Where $$\gamma$$ is [Euler-Mascheroni Constant][1]

[1]: https://en.m.wikipedia.org/wiki/Euler%E2%80%93Mascheroni_constant

# Answer

Note that
$$
\sum_{k\geq1}\frac{\zeta\left(2k\right)-1}{k}
=\sum_{k\geq1}\frac{1}{k}\sum_{m\geq2}\frac{1}{m^{2k}}$$ 

$$
=\sum_{m\geq2}\sum_{k\geq1}\frac{1}{km^{2k}}=-\sum_{m\geq2}\log\left(1-\frac{1}{m^{2}}\right)
$$ 

$$=-\log\left(\prod_{m\geq2}\left(1-\frac{1}{m^{2}}\right)\right)$$ 

and it is well known that

 $$\prod_{m\geq2}\left(1-\frac{1}{m^{2}}\right)=\frac{1}{2}$$

 since 
 
 $$
 \prod_{m=2}^{N}\left(1-\frac{1}{m^{2}}\right)=\prod_{m=2}^{N}\frac{m^{2}-1}{m^{2}}=\prod_{m=2}^{N}\frac{m-1}{m}\prod_{m=2}^{N}\frac{m+1}{m}=\frac{1}{N}\frac{N+1}{2}
 $$ 
 
 so 
 
 $$
 \sum_{k\geq1}\frac{\zeta\left(2k\right)-1}{k}=\color{red}{\log\left(2\right)}.
 $$ 
 
 The result obviously implies your limit since

 $$
 \lim_{n\rightarrow\infty}\left(\sum_{k=1}^{n}\frac{\zeta\left(2k\right)}{k}-\log\left(2n\right)\right)
 =\lim_{n\rightarrow\infty}\left(\sum_{k=1}^{n}\frac{\zeta\left(2k\right)}{k}-\sum_{k=1}^{n}\frac{1}{k}+\sum_{k=1}^{n}\frac{1}{k}-\log\left(2n\right)\right)
 $$

 $$
 \lim_{n\rightarrow\infty}\left(\sum_{k=1}^{n}\frac{\zeta\left(2k\right)-1}{k}+\sum_{k=1}^{n}\frac{1}{k}-\log\left(n\right)-\log\left(2\right)\right)
 =\lim_{n\rightarrow\infty}\left(\sum_{k=1}^{n}\frac{1}{k}-\log\left(n\right)\right)
 =\color{blue}{\gamma}.
 $$