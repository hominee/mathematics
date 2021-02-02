---
layout: post
title: Problem related to integration
tag:
 - integration

description: Problem related to integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to evaluate $$I=\int_0^{\pi/2}x^2\ln(\sin x)\ln(\cos x)\ \mathrm dx$$

<!–-break-–>


Find the value of
$$I=\displaystyle\int_0^{\pi/2}x^2\ln(\sin x)\ln(\cos x)\ \mathrm dx$$
We have the information that 
$$J=\displaystyle\int_0^{\pi/2}x\ln(\sin x)\ln(\cos x)\ \mathrm dx=\dfrac{(\pi\ln{2})^2}{8}-\dfrac{\pi^4}{192}$$
.

# Answer 


Tools Needed







$$
\begin{align*}
\frac1{k(j-k)^2}&=\frac1{j^2k}-\frac1{j^2(k-j)}+\frac1{j(k-j)^2}\tag{1}\\
\frac1{k(j+k)^2}&=\frac1{j^2k}-\frac1{j^2(k+j)}-\frac1{j(k+j)^2}\tag{2}\\
\log(\sin(x))&=-\log(2)-\sum_{k=1}^\infty\frac{\cos(2kx)}{k}\tag{3}\\
\log(\cos(x))&=-\log(2)-\sum_{k=1}^\infty(-1)^k\frac{\cos(2kx)}{k}\tag{4}\\
\cos(2jx)\cos(2kx)&=\frac12\Big[\cos(2(j-k)x)+\cos(2(j+k)x)\Big]\tag{5}\\
\end{align*}


$$







$$


\int_0^{\pi/2}x^2\cos(2kx)\,\mathrm{d}x=\left\{
\begin{array}{}
(-1)^k\frac\pi{4k^2}&\text{if }k\ne0\\
\frac{\pi^3}{24}&\text{if }k=0
\end{array}\right.\tag{6}\\


$$



Tool Use








$$
\begin{align*}
&\int_0^{\pi/2}x^2\log(\sin(x))\log(\cos(x))\,\mathrm{d}x\\[12pt]
&=\int_0^{\pi/2}x^2\left(\log(2)+\sum_{k=1}^\infty\frac{\cos(2kx)}{k}\right)\left(\log(2)+\sum_{k=1}^\infty(-1)^k\frac{\cos(2kx)}{k}\right)\,\mathrm{d}x\\[12pt]
&=\log(2)^2\int_0^{\pi/2}x^2\,\mathrm{d}x
+\log(2)\sum_{k=1}^\infty\frac1k\int_0^{\pi/2}x^2\cos(4kx)\,\mathrm{d}x\\
&+\sum_{j=1}^\infty\sum_{k=1}^\infty\frac{(-1)^k}{2jk}\int_0^{\pi/2}x^2\Big[\cos(2(j-k)x)+\cos(2(j+k)x)\Big]\,\mathrm{d}x\\[12pt]
&=\frac{\pi^3}{24}\log(2)^2+\log(2)\frac\pi{16}\zeta(3)\\
&+\frac\pi8\sum_{j=1}^\infty\sum_{k=1}^\infty\frac{(-1)^j}{jk}\left[\mathrm{iif}\left(j=k,\frac{\pi^2}{6},\frac1{(j-k)^2}\right)+\frac1{(j+k)^2}\right]\\[12pt]
&=\frac{\pi^3}{24}\log(2)^2+\log(2)\frac\pi{16}\zeta(3)\\
&+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\sum_{k=1}^{j-1}\frac1{k(j-k)^2}
+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j^2}\frac{\pi^2}{6}
+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\sum_{k=j+1}^\infty\frac1{k(j-k)^2}\\
&+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\sum_{k=1}^\infty\frac1{k(j+k)^2}\\[12pt]
&=\frac{\pi^3}{24}\log(2)^2+\log(2)\frac\pi{16}\zeta(3)\\
&+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\left(\frac2{j^2}H_{j-1}+\frac1jH_{j-1}^{(2)}\right)
-\frac{\pi^5}{576}
+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\left(-\frac1{j^2}H_j+\frac1j\frac{\pi^2}{6}\right)\\
&+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\left(\frac1{j^2}H_j-\frac1j\frac{\pi^2}{6}+\frac1jH_j^{(2)}\right)\\[12pt]
&=\frac{\pi^3}{24}\log(2)^2+\log(2)\frac\pi{16}\zeta(3)\\
&+\frac\pi8\sum_{j=1}^\infty\frac{(-1)^j}{j}\left(\frac2{j^2}H_j+\frac2jH_j^{(2)}-\frac3{j^3}\right)
-\frac{\pi^5}{576}\\[12pt]
&=\frac{\pi^3}{24}\log(2)^2+\log(2)\frac\pi{16}\zeta(3)+\frac{11\pi^5}{5760}
+\frac\pi4\sum(-1)^j\left(\frac1{j^3}H_j+\frac1{j^2}H_j^{(2)}\right)\\[12pt]
&=\frac{\pi^3}{24}\log(2)^2+\log(2)\frac\pi{16}\zeta(3)-\frac{\pi^5}{960}
-\frac\pi{16}\sum_{j=1}^\infty\frac1{j^3}H_{2j}\tag{7}
\end{align*}


$$





Numerically, $$(7)$$ matches the integral. we are  working on the last harmonic sum. Both numerical integration and $$(7)$$ yield $$0.0778219793722938643380944$$.
Mathematica Help
Thanks to Artes' answer on Mathematica, we have verified that these agree to 100 places.

