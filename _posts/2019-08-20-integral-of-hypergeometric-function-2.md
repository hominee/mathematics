---
layout: post
title: integral related to hypergeometric function 2
tags:
  - integration   
  - definite-integrals
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  integral related to hypergeometric function 2
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :

$$
\frac{2^{n+2}(n-1)}{\binom{2n}{n}(n+1)} \frac{n-1}{n+1}= (\pi -2 )(\pi-4)   
$$

<!–-break-–>


# Answer

By using the [Euler beta function][1], one has

$$
\frac{2^{n+2}(n-1)}{\binom{2n}{n}(n+1)}=\frac{4(n-1)(2n+1)}{n+1}\int_0^1(2x(1-x))^ndx,\quad n \geq 0. \tag1
$$

Then, one may obtain

$$ 
\begin{equation*}
\begin{aligned}
&\sum_0^\infty\frac{2^{n+2}(n-1)}{\binom{2n}{n}(n+1)}
\\\\&=\sum_0^\infty\frac{4(n-1)(2n+1)}{n+1}\int_0^1(2x(1-x))^ndx\\\\
&=\int_0^1\sum_0^\infty\frac{4(n-1)(2n+1)}{n+1}(2x(1-x))^ndx \:dx\\\\
&=\int_0^1\left(\frac{-40x^2+40x-12}{(1-2 x+2 x^2)^2}-\frac{4 \log(1-2 x+2 x^2)}{(1-x) x}\right)dx\\\\
&=\underbrace{\int_0^1\frac{-40x^2+40x-12}{(1-2 x+2 x^2)^2}\,dx}_{\large \color{blue}{8-6\pi}}+\underbrace{4\int_0^1-\frac{\log(1-2 x+2 x^2)}{(1-x) x}\,dx}_{\large \color{red}{\pi^2}}
\\\\&=\color{blue}{8-6\pi}+\color{red}{\pi^2}
\\\\&=(\pi-2)(\pi-4)
\end{aligned}
\end{equation*}
 $$ 
 
Addintionally for Some details, observe that

 $$ 

\sum_{n=0}^\infty(2n-3)y^n=\frac{5 y-3}{(1-y)^2},\quad |y|<1, \tag{A}

 $$ 


 $$ 

\sum_{n=0}^\infty\frac1{n+1}y^n=-\frac{\log(1-y)}y,\quad |y|<1, \tag{B}

 $$
 
One has

 $$ 

\frac{4(n-1)(2n+1)}{n+1}=4(2 n-3)+\frac8{1+n}  \tag{C}

 $$ 
 
 then, using $$(\text{A})$$, $$(\text{B})$$ and $$(\text{C})$$ with $$ y:=2x(1-x)$$ gives

 $$ 

\sum_0^\infty\frac{4(n-1)(2n+1)}{n+1}(2x(1-x))^n=\frac{-40x^2+40x-12}{(1-2 x+2 x^2)^2}-\frac{4 \log(1-2 x+2 x^2)}{(1-x) x}

 $$
 
 One may classically integrate the fraction by parts. One may then rewrite the  $$\log$$-term as

 $$ 
-\frac{4 \log(1-2 x+2 x^2)}{(1-x) x}=\frac{16}{1-u^2}\log \left(1-\frac{1-u^2}2\right) \tag{D}
 $$ 
 
 with $$ u:=2x-1$$, expanding in power series of $$(1-u^2)$$, integrating termwise to recognize a classic binomial series giving $$\pi^2$$.

  [1]: https://en.wikipedia.org/wiki/Beta_function