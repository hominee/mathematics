---
layout: post
title: integral related to hypergeometric function 3
tags:
  - integration   
  - definite-integrals
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  integral related to hypergeometric function 3
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :


 $$

\sum_{n=0}^{\infty}\frac{2^n(5n^5+5n^4+5n^3+5n^2-9n+9)}{(2n+1)(2n+2)(2n+3){2n\choose n}} = \frac{9 \pi ^2}{8}

 $$


<!–-break-–>


# Answer

Using Beta function, one can express:  

 $$ 
\sum_{n=0}^{\infty}\frac{2^n(5n^5+5n^4+5n^3+5n^2-9n+9)}{(2n+1)(2n+2)(2n+3){2n\choose n}}
 $$ 
  

 $$ 
=\frac{5n^5+5n^4+5n^3+5n^2-9n+9}{(n+1)^2}\cdot\frac{1}{2}\int_0^1(2t(1-t))^{n+1}dt
 $$ 
  

Therefore the original expression can be transformed into:  
 
 $$ 
\frac{1}{2}\int_0^1\sum_{n=0}^{\infty}\frac{(5n^5+5n^4+5n^3+5n^2-9n+9)(2t(1-t))^{n+1}}{(n+1)^2}dt
 $$ 
  

_____________
We know that  

 $$ 
\sum_{n=0}^{\infty}\frac{t^n}{n+1}=-\frac{\ln(1-t)}{t}\tag1
 $$ 
  
Integrating, we get  

 $$ 
\sum_{n=0}^{\infty}\frac{t^{n+1}}{(n+1)^2}=\text{Li}_2(t)\tag2
 $$ 
  
Differentiating, multiplying both sides by _t_ and using the above formulas to do some algebra, we obtain  

 $$ 
\sum_{n=0}^{\infty}n\frac{t^{n+1}}{(n+1)^2}=-\text{Li}_2(t)-\ln (1-t)\tag3
 $$ 
  
Repeating the process:  

 $$ 
\sum_{n=0}^{\infty}n^2\frac{t^{n+1}}{(n+1)^2}=\frac{t \text{Li}_2(t)-\text{Li}_2(t)-t+2 t \ln (1-t)-2 \ln (1-t)}{t-1}\tag4
 $$ 
  

 $$ 
\sum_{n=0}^{\infty}n^3\frac{t^{n+1}}{(n+1)^2}=\frac{-t^2 \text{Li}_2(t)+2 t \text{Li}_2(t)-\text{Li}_2(t)+3 t^2-3 t^2 \ln (1-t)-2 t+6 t \ln (1-t)-3 \ln (1-t)}{(t-1)^2}\tag5
 $$ 
  

 $$ 
\sum_{n=0}^{\infty}n^4\frac{t^{n+1}}{(n+1)^2}=\frac{t^3 \text{Li}_2(t)-3 t^2 \text{Li}_2(t)+3 t \text{Li}_2(t)-\text{Li}_2(t)-6 t^3+4 t^3 \ln (1-t)+7 t^2-12 t^2 \ln (1-t)-3 t+12 t \ln (1-t)-4 \ln (1-t)}{(t-1)^3}\tag6
 $$ 
  

 $$ 
\sum_{n=0}^{\infty}n^5\frac{t^{n+1}}{(n+1)^2}=\frac{-t^4 \text{Li}_2(t)+4 t^3 \text{Li}_2(t)-6 t^2 \text{Li}_2(t)+4 t \text{Li}_2(t)-\text{Li}_2(t)+10 t^4-5 t^4 \ln (1-t)-14 t^3+20 t^3 \ln (1-t)+14 t^2-30 t^2 \ln (1-t)-4 t+20 t \ln (1-t)-5 \ln (1-t)}{(t-1)^4}\tag7
 $$ 
  
Set _t_ $$\mapsto$$ $$2t(1-t)$$, substitute the above identities, and we simplify to get: 
 
$$
\begin{equation*}
\begin{aligned}
(4)&=\frac{1}{2}\int_0^1\frac{18 \left(2 t^2-2 t+1\right)^4 \text{Li}_2(-2 (t-1) t)+\left(2 t^2-2 t+1\right)^4 \left(-\ln \left(2 t^2-2 t+1\right)\right)+20 \left(24 t^7-96 t^6+156 t^5-132 t^4+68 t^3-28 t^2+9 t-1\right) t}{\left(2 t^2-2 t+1\right)^4}dt \\
&=\frac{1}{2}\underbrace{\int_0^118\text{Li}_2(-2 (t-1) t)dt}_{\large \color{blue}{\frac{9}{4}(-32+8\pi+\pi^2)}}-\frac{1}{2}\underbrace{\int_0^1\ln \left(2 t^2-2 t+1\right)dt}_{\large \color{red}{\frac{1}{2}(\pi-4)}}+\frac{1}{2}\underbrace{\int_0^1(30-\frac{90}{2t^2-2t+1}+\frac{130}{(2t^2-2t+1)^2}-\frac{100}{(2t^2-2t+1)^3}+\frac{30}{(2t^2-2t+1)^4})dt}_{\large \color{green}{-\frac{35}{2}(\pi-4)}} \\
&=\frac{1}{2}(\color{blue}{\frac{9}{4}(-32+8\pi+\pi^2)}-\color{red}{\frac{1}{2}(\pi-4)}\color{green}{-\frac{35}{2}(\pi-4)}) \\
&=\LARGE \frac{9\pi^2}{8}
\end{aligned}
\end{equation*} 
$$    

**Update**: the evaluation of $$\int_0^1\text{Li}_2(-2 (t-1) t)dt$$, and it can be done using integration by parts.  
  **Evaluating $$\int_0^1\text{Li}_2(-2 (t-1) t)dt$$**

  $$
\begin{equation*}
\begin{aligned}
& \int_0^1\text{Li}_2(-2t^2+2t)dt \\
& = \int_0^1\frac{-2t^2+t}{-t^2+t}\ln(1-2t+2t^2)dt \\
& = 2\int_0^1\ln(1-2t+2t^2)dt+\int_0^1\frac{-t}{-t^2+t}\ln(1-2t+2t^2)dt \\
& = -4+\pi-\frac{1}{2}\int_0^1\frac{\ln(1-2t+2t^2)}{-t^2+t}dt \\
& =-4+\pi-\frac{1}{2}(\int_0^1\frac{\ln(1-2t+2t^2)}{t}dt+\int_0^1\frac{\ln(1-2t+2t^2)}{1-t}dt) \\
& =-4+\pi-\int_0^1\frac{\ln(1-2t+2t^2)}{t}dt \\
& =\frac{1}{8}(-32+8\pi+\pi^2)
\end{aligned}
\end{equation*}
$$