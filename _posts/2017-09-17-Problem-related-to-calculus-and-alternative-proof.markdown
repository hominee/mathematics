---
layout: post
title: Problem related to calculus and alternative proof
tag:
 - calculus
 - real-analysis
 - sequences-and-series
 - alternative-proof

description: Problem related to calculus and alternative proof

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

An alternative proof for sum of alternating series evaluates to $$\frac{\pi}{4}\sec\left(\frac{a\pi}{4}\right)$$

<!–-break-–>


How does one prove the given series? 

$$

\sum_{n=0}^\infty\left(\frac{(-1)^n}{4n-a+2}+\frac{(-1)^n}{4n+a+2}\right)=\frac{\pi}{4}\sec\left(\frac{a\pi}{4}\right)

$$


This series came up in xpaul's calculation during the process of answering my homework problem. we worked for a while on this today but was unsuccessful. 


$$




$$
\begin{align*}\sum_{n=0}^\infty\left(\frac{(-1)^n}{4n-a+2}+\frac{(-1)^n}{4n+a+2}\right)&=4\sum_{n=0}^\infty(-1)^n\frac{2n+1}{(4n+2)^2-a^2}\\&=\sum_{n=0}^\infty(-1)^n\frac{2n+1}{(2n+1)^2-\left(\frac{a}{2}\right)^2}\end{align*}


$$

$$


Comparing with Taylor series for secant, hyperbolic secant, or any other well known series forms but we could not get any of them to work,  perhaps someone else can? we would like a nice proof and avoiding residue method in order to complete my homework's answer. Thanks in advance.

# Answer 


we answered this before in Closed form of $$\int_{0}^{\infty} \frac{\tanh(x)\,\tanh(2x)}{x^2}\;dx$$. However the solution was too long as Venus mentioned. Inspired from Jack D'aurizio's answer, we have a simple solution for this. It is easy to check that

$$
\begin{eqnarray*}
&&\sum_{n=0}^\infty\left(\frac{(-1)^n}{4n-a+2}+\frac{(-1)^n}{4n+a+2}\right)\\
&=& \int_{0}^{1}\frac{x}{1+x^4}\left(x^a+x^{-a}\right)\,dx=\int_{0}^{\infty}\frac{x^{a+1}}{1+x^4}\,dx\\
&=&\frac{1}{a+2}\int_0^\infty\frac{1}{1+x^{\frac{a+2}{4}}}dx.
\end{eqnarray*}
$$

Now using the following well-known integral


$$

 \int_0^\infty\frac{1}{1+x^n}dx=\frac{\pi}{n\sin(\pi/n)}, \text{ for }n>1, 

$$


(for example, see Prove $$\int_0^{\infty}\! \frac{\mathbb{d}x}{1+x^n}=\frac{\pi}{n \sin\frac{\pi}{n}}$$ using real analysis techniques only) it is easy to get the answer.

