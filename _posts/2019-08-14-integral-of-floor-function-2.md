---
layout: post
title: integral related to floor function 2
tags:
  - integration   
  - definite-integrals
  - closed-form
  - floor-integral
  - real-analysis
  
description:  
  integral related to floor function 2
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Prove that : 


 $$ 

\int_0^1{\left\lfloor{1\over x}\right\rfloor}^{-1}\!dx={1\over2^2}+{1\over3^2}+{1\over4^2}+\cdots.

 $$ 


<!–-break-–>

# Answer

observe that: if $$x\in\big(\frac{1}{k+1},\frac{1}{k}\big]$$, then $$\frac{1}{x}\in[k,k+1)$$, thus $$\left\lfloor{1\over x}\right\rfloor=k$$ and hence

 $$ 

\left\lfloor{1\over x}\right\rfloor^{-1}=\frac{1}{k}, \quad \text{whenever}\,\, x\in\Big(\frac{1}{k+1},\frac{1}{k}\Big].

 $$ 

Therefore

 $$ 

\int_{1/n}^1{\left\lfloor{1\over x}\right\rfloor}^{-1}dx=\sum_{k=1}^{n-1}
\int_{1/(k+1)}^{1/k}{\left\lfloor{1\over x}\right\rfloor}^{-1}dx=\sum_{k=1}^{n-1}
\int_{1/(k+1)}^{1/k}\frac{1}{k}dx=\sum_{k=1}^{n-1}\frac{1}{k}\cdot\frac{1}{k(k+1)},

 $$ 

and thus

 $$ 

\int_0^1
{\left\lfloor{1\over x}\right\rfloor}^{-1}dx=\lim_{n\to\infty}
\int_{1/n}^1{\left\lfloor{1\over x}\right\rfloor}^{-1}dx=
\sum_{n=1}^\infty \frac{1}{n^2(n+1)}.

 $$ 

Meanwhile

 $$ 

\sum_{n=1}^\infty \frac{1}{n(n+1)}=\sum_{n=1}^\infty\left(\frac{1}{n}-\frac{1}{n+1}\right)=1
\quad\text{and}\quad \frac{1}{n^2}-\frac{1}{n(n+1)}=\frac{1}{n^2(n+1)}.

 $$ 

Hence, finally

$$
\begin{equation*} 
\begin{aligned}
\frac{1}{2^2}+\frac{1}{3^2}+\cdots+\frac{1}{n^2}+\cdots &=\sum_{n=1}^{\infty}\frac{1}{n^2}-1 \\
&=\sum_{n=1}^{\infty}\frac{1}{n^2}-\sum_{n=1}^\infty \frac{1}{n(n+1)}\\
&=\sum_{n=1}^\infty \frac{1}{n^2(n+1)} \\
&=\int_0^1 {\left\lfloor{1\over x}\right\rfloor}^{-1}dx.
\end{aligned}  
\end{equation*}
$$