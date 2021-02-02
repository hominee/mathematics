---
layout: post
title: integral related to exponential function 1 
tags:
  - integration   
  - definite-integrals
  - closed-form
  - real-analysis
  
description:  
  integral related to exponential function 1

hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form for :

$$
   
\int_{0}^{\infty}{\ln(e^x-1)\over e^x+1}\mathrm dx

$$
   
 

<!–-break-–>


# Answer

Let $$I$$ be given by the integral


$$
I=\int_0^\infty \frac{\log(e^x-1)}{e^x+1}\,dx \tag 1
$$


Enforcing the substitution $$x\to -\log(x)$$ in $$(1)$$ we find


$$
\begin{align*}
I&=\int_0^1 \frac{\log(1-x)-\log(x)}{1+x}\,dx\\\\
&=\int_0^1 \frac{\log(1-x)}{1+x}\,dx-\int_0^1 \frac{\log(x)}{1+x}\,dx\tag2
\end{align*}
$$


We enforce the substitution $$x\to 2x-1$$ in the first integral on the right-hand side of $$(2)$$ to reveal


$$
\begin{align*}
\int_0^1 \frac{\log(1-x)}{1+x}\,dx&=\int_{1/2}^1 \frac{\log(2)+\log(1-x)}{x}\,dx\\\\
&=\log^2(2)-\text{Li}_2(1)+\text{Li}_2(1/2)\\\\
&=\log^2(2)-\frac{\pi^2}{6}+\frac{\pi^2}{12}-\frac12\log^2(2)\\\\
&=\frac12\log^2(2)-\frac{\pi^2}{12}\tag 3
\end{align*}
$$


We integrate by parts the second integral on the right-hand side of $$(2)$$ with $$u=\log(x)$$ and $$v=\log(1+x)$$ to reveal


$$
\int_0^1 \frac{\log(x)}{1+x}\,dx=-\int_0^1 \frac{\log(1+x)}{x}\,dx\tag 4
$$


Then letting $$x\to -1$$ in $$(4)$$, we find 


$$
\begin{align*}
\int_0^1 \frac{\log(x)}{1+x}\,dx&=-\int_0^{-1} \frac{\log(1-x)}{x}\,dx\\\\
&=\text{Li}_2(-1)\\\\
&=-\frac{\pi^2}{12}\tag 5
\end{align*}
$$


Finally, substituting $$(3)$$ and $$(5)$$ into $$(2)$$ yields the coveted result


$$
\bbox[5px,border:2px solid #C0A000]{I=\frac12\log^2(2)}
$$

