---
layout: post
title: Problem related to calculus and definite integrals
tag:
 - calculus
 - real-analysis
 - integration
 - definite-integrals

description: Problem related to calculus and definite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Compute $$\int_0^\pi\frac{\cos nx}{a^2-2ab\cos x+b^2}\, dx$$

<!–-break-–>



How to compute the following integral
  \begin{equation}
\int_0^\pi\frac{\cos nx}{a^2-2ab\cos x+b^2}\, dx
\end{equation}

we have been given two integral questions by my teacher. we cannot answer this one. we have also searched the similar question here but it looks like nothing is similar so we think this is not a duplicate. we could compute the integral if 
\begin{equation}
\int_0^\pi\frac{dx}{a^2-2ab\cos x+b^2}
\end{equation}
The $$\cos nx$$ part makes the integral is really difficult. we want to use the result to compute this integral (the real question given by my teacher)
\begin{equation}
\int_0^\pi\frac{x^2\cos nx}{a^2-2ab\cos x+b^2}\, dx
\end{equation}
My question is how to compute the first integral (in the grey-shaded part) preferably with elementary ways (high school methods)? 
.

# Answer 


Let $$I_n(a,b)$$ be the desired integral. 

**Note** that $$I_n(a,b)=I_n(b,a)$$, and $$I_n(a,b)=I_n(-a,-b)$$. So, we may suppose that 
$$|b|< a$$ 

**Note** that


$$

\eqalign{
\frac{a^2-b^2}{a^2-2ab\cos x+b^2}&=\frac{a}{a-e^{ix}b}+\frac{be^{-ix}}{a-e^{-ix}b}\cr
&=\sum_{n=0}^\infty \left(\frac{b}{a}\right)^ne^{inx}+\frac{be^{-ix}}{a}\sum_{n=0}^\infty
\left(\frac{b}{a}\right)^ne^{-inx}\cr
&=1+\sum_{n=1}^\infty \left(\frac{b}{a}\right)^ne^{inx}+ \sum_{n=1}^{\infty}
\left(\frac{b}{a}\right)^{n}e^{-inx}\cr
&=1+2\sum_{n=1}^\infty \left(\frac{b}{a}\right)^n\cos(n x)
}


$$


It follows, using the uniform convergence of the series on $$[0,\pi]$$, that


$$


\int_0^\pi\frac{(a^2-b^2)\cos(mx)}{a^2-2ab\cos x+b^2}dx
=\int_0^\pi\cos(mx)dx+2\sum_{n=1}^\infty \left(\frac{b}{a}\right)^n\int_0^\pi\cos(n x)\cos(mx)dx


$$


But $$\int_0^\pi\cos(n x)\cos(mx)dx=0$$ if $$n\ne m$$, and 
$$\int_0^\pi\cos^2(n x)dx=\pi/2$$ if $$n\ne0$$. So


$$

\eqalign{I_m(a,b)=
\int_0^\pi\frac{\cos(mx)}{a^2-2ab\cos x+b^2}dx
&=\left\{\matrix{\frac{\pi}{a^2-b^2}&\hbox{if}&m=0\cr
\frac{\pi}{a^2-b^2}\left(\frac{b}{a}\right)^m&\hbox{if}&m\ne0
}
\right.}


$$


which is the desired formula for 
$$|b|<a$$.

