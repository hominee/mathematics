---
layout: post
title: Problem related to calculus and integration
tag:
 - calculus
 - real-analysis
 - integration
 - definite-integrals
 - improper-integrals

description: Problem related to calculus and integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 


I found a nice formula of the following integral here


 $$ 
\int_0^\infty \frac{x^{\alpha}dx}{1+2x\cos\beta +x^{2}}=\frac{\pi\sin (\alpha\beta)}{\sin (\alpha\pi)\sin \beta }
 $$ 


It states there that it can be proved by using contours method which I do not understand. It seems that the RHS is Euler's reflection formula for the gamma function but I am not so sure.

<!–-break-–>

# Answer 


If you don't mind, I would like to present an alternative approach that makes use of the fact that

 $$ 
\int^\infty_0\frac{x^{p-1}}{1+x}dx=\frac{\pi}{\sin{p\pi}}
 $$ 

Simply factorise the denominator and decompose the integrand into partial fractions.
$$
\begin{align*}
\int^\infty_0\frac{x^a}{x^2+2(\cos{b})x+1}dx
&=\int^\infty_0\frac{x^a}{(x+e^{ib})(x+e^{-ib})}dx\\
&=\frac{1}{-e^{ib}+e^{-ib}}\int^\infty_0\frac{x^a}{e^{ib}+x}dx+\frac{1}{-e^{-ib}+e^{ib}}\int^\infty_0\frac{x^a}{e^{-ib}+x}dx\\
&=\frac{1}{-2i\sin{b}}\int^\infty_0\frac{(e^{ib}u)^a}{1+u}du+\frac{1}{2i\sin{b}}\int^\infty_0\frac{(e^{-ib}u)^a}{1+u}du\\
&=\frac{e^{iab}}{-2i\sin{b}}\frac{\pi}{\sin(\pi a+\pi)}+\frac{e^{-iab}}{2i\sin{b}}\frac{\pi}{\sin(\pi a+\pi)}\\
&=\frac{\pi}{\sin \pi a\sin{b}}\left(\frac{e^{iab}-e^{-iab}}{2i}\right)\\
&=\frac{\pi\sin{ab}}{\sin{\pi a}\sin{b}}
\end{align*}
$$
