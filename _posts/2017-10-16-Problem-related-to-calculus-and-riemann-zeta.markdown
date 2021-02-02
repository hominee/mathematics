---
layout: post
title: Problem related to calculus and riemann zeta
tag:
 - calculus
 - sequences-and-series
 - analysis
 - fourier-series
 - riemann-zeta

description: Problem related to calculus and riemann zeta

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Computing $$\zeta(6)=\sum\limits_{k=1}^\infty \frac1{k^6}$$ with Fourier series.

<!–-break-–>


Let $$ f$$ be a function such that $$ f\in C_{2\pi}^{0}(\mathbb{R},\mathbb{R}) $$ (f is $$2\pi$$-periodic) such that $$ \forall x \in [0,\pi]$$: 

$$

f(x)=x(\pi-x)

$$


Computing the Fourier series of $$f$$ and using Parseval's identity, we have computed $$\zeta(2)$$ and $$\zeta(4)$$.

How can we compute $$ \zeta(6) $$ now?
Fourier series of $$ f $$:


$$

 S(f)= \frac{\pi^2}{6}-\sum_{n=1}^{\infty} \frac{\cos(2nx)}{n^2}

$$




$$

 x=0,  \zeta(2)=\pi^2/6

$$


.


# Answer 


One method is to consider the generating function of $$\zeta(2k)$$:


$$





$$
\begin{align*}

f(x)
&=\sum_{k=1}^\infty\zeta(2k)\,x^{2k}\\
&=\sum_{k=1}^\infty\sum_{n=1}^\infty\frac{x^{2k}}{n^{2k}}\\
&=\sum_{n=1}^\infty\frac{x^2/n^2}{1-x^2/n^2}\\
&=\sum_{n=1}^\infty\frac{x^2}{n^2-x^2}\\
&=-\frac{x}{2}\sum_{n=1}^\infty\left(\frac{1}{x-n}+\frac{1}{x+n}\right)\\
&=-\frac{x}{2}\left(\pi\cot(\pi x)-\frac1x\right)\\
&=\frac12(1-\pi x\cot(\pi x))\tag{1}

\end{align*}


$$


$$


In light of equation $$(1)$$, find the power series of


$$


x\cot(x)=\sum_{k=0}^\infty a_kx^{2k}


$$




$$


\cos(x)=\frac{\sin(x)}{x}\sum_{k=0}^\infty a_kx^{2k}


$$




$$





$$
\begin{align*}

\sum_{n=0}^\infty(-1)^n\!\frac{x^{2n}}{(2n)!}
&=\sum_{n=0}^\infty(-1)^n\!\frac{x^{2n}}{(2n+1)!}\;\;\sum_{k=0}^\infty a_kx^{2k}\\
&=\sum_{n=0}^\infty\left(\sum_{k=0}^n(-1)^k\!\frac{a_{n-k}}{(2k+1)!}\right)x^{2n}\tag{2}

\end{align*}


$$


$$


Comparing the coefficients of the powers of $$x$$ in $$(2)$$ yields


$$





$$
\begin{align*}

a_n
&=\frac{(-1)^n}{(2n)!}-\sum_{k=1}^n(-1)^k\!\frac{a_{n-k}}{(2k+1)!}\\
&=\frac{(-1)^n2n}{(2n+1)!}-\sum_{k=1}^{n-1}(-1)^k\!\frac{a_{n-k}}{(2k+1)!}\tag{3}

\end{align*}


$$


$$


Since $$a_n=-2\dfrac{\zeta(2n)}{\pi^{2n}}$$ for positive $$n$$, $$(3)$$ becomes


$$


\zeta(2n)=\frac{(-1)^{n-1}\pi^{2n}}{(2n+1)!}n+\sum_{k=1}^{n-1}\!\frac{(-1)^{k-1}\pi^{2k}}{(2k+1)!}\zeta(2n-2k)\tag{4}


$$


Equation $$(4)$$ gives $$\zeta(2n)$$ recursively for positive $$n$$:


$$





$$
\begin{align*}

\zeta(2)&=\frac{\pi^2}{3!}=\frac{\pi^2}{6}\\
\zeta(4)&=-\frac{\pi^4}{5!}2+\frac{\pi^2}{3!}\zeta(2)=\frac{\pi^4}{90}\\
\zeta(6)&=\frac{\pi^6}{7!}3-\frac{\pi^4}{5!}\zeta(2)+\frac{\pi^2}{3!}\zeta(4)=\frac{\pi^6}{945}\\
\zeta(8)&=-\frac{\pi^8}{9!}4+\frac{\pi^6}{7!}\zeta(2)-\frac{\pi^4}{5!}\zeta(4)+\frac{\pi^2}{3!}\zeta(6)=\frac{\pi^8}{9450}

\end{align*}


$$


$$



