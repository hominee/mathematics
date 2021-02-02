---
layout: post
title: Problem related to calculus and closed form
tag:
 - calculus
 - real-analysis
 - integration
 - definite-integrals
 - closed-form

description: Problem related to calculus and closed form

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Compute $$\int_0^{\pi/4}\frac{(1-x^2)\ln(1+x^2)+(1+x^2)-(1-x^2)\ln(1-x^2)}{(1-x^4)(1+x^2)} x\exp(\frac{x^2-1}{x^2+1}) dx$$

<!–-break-–>



Compute the following integral
  \begin{equation}
\int_0^{\Large\frac{\pi}{4}}\left[\frac{(1-x^2)\ln(1+x^2)+(1+x^2)-(1-x^2)\ln(1-x^2)}{(1-x^4)(1+x^2)}\right] x\, \exp\left[\frac{x^2-1}{x^2+1}\right]\, dx
\end{equation}

we was given two integral questions by my teacher. we can answer this one although it took a lot of time to compute it. we want to share this problem to the other users here and we would love to see how Mathematics SE users compute this monster.

# Answer 


Rewrite



$$
\begin{align*}
&\int\left[\frac{(1-x^2)\ln(1+x^2)+(1+x^2)-(1-x^2)\ln(1-x^2)}{(1-x^4)(1+x^2)}\right] x\ \exp\left[\frac{x^2-1}{x^2+1}\right]\ dx\\
&=-\int\left[\frac{(1-x^2)\ln\left(\dfrac{1-x^2}{1+x^2}\right)-(1+x^2)}{(1-x^2)(1+x^2)(1+x^2)}\right] x\ \exp\left[-\frac{1-x^2}{1+x^2}\right]\ dx\\
&=-\frac14\int\left[\frac{(1-x^2)\ln\left(\dfrac{1-x^2}{1+x^2}\right)-(1+x^2)}{(1-x^2)}\right] \frac{2x}{1+x^2}\, \exp\left[-\frac{1-x^2}{1+x^2}\right]\ \frac{2\ dx}{1+x^2}\\
&=-\frac14\int\left[\ln\left(\frac{1-x^2}{1+x^2}\right)-\frac{1+x^2}{1-x^2}\right] \frac{2x}{1+x^2}\, \exp\left[-\frac{1-x^2}{1+x^2}\right]\ \frac{2\ dx}{1+x^2}.\tag1
\end{align*}
$$


Now, consider Weierstrass substitution:


$$


x=\tan\frac{t}{2}\;,\;\sin t=\frac{2x}{1+x^2}\;,\;\cos t=\frac{1-x^2}{1+x^2}\;,\;\text{ and }\;dt=\frac{2\ dx}{1+x^2}.


$$


The integral in $$(1)$$ turns out to be


$$


-\frac14\int\left[\ln\left(\cos t\right)-\frac{1}{\cos t}\right] \sin t\, \exp\left[-\cos t\right]\ dt.\tag2


$$


Let $$y=\cos t\;\Rightarrow\;dy=-\sin t\ dt$$, then $$(2)$$ becomes


$$


\frac14\int\left[\ln y-\frac{1}{y}\right] e^{-y}\ dy=\frac14\left[\int e^{-y}\ln y\ dy-\int\frac{e^{-y}}{y}\ dy\right].\tag3


$$


The second integral in the RHS $$(3)$$ can be evaluated by using IBP. Taking $$u=e^{-y}\;\Rightarrow\;du=-e^{-y}\ dy$$ and $$dv=\dfrac1y\ dy\;\Rightarrow\;v=\ln y$$, then


$$


\int\frac{e^{-y}}{y}\ dy=e^{-y}\ln y+\int e^{-y}\ln y\ dy.\tag4


$$


Substituting $$(4)$$ to $$(3)$$, we obtain


$$


\frac14\left[\int e^{-y}\ln y\ dy-e^{-y}\ln y-\int e^{-y}\ln y\ dy\right]=-\frac14e^{-y}\ln y+C.


$$


Thus



$$
\begin{align*}
&\int\left[\frac{(1-x^2)\ln(1+x^2)+(1+x^2)-(1-x^2)\ln(1-x^2)}{(1-x^4)(1+x^2)}\right] x\ \exp\left[\frac{x^2-1}{x^2+1}\right]\ dx\\
&=\color{blue}{-\frac14\exp\left[-\frac{1-x^2}{1+x^2}\right]\ln \left|\frac{1-x^2}{1+x^2}\right|+C}
\end{align*}


$$

and



$$
\begin{align*}
&\int_0^{\Large\frac\pi4}\left[\frac{(1-x^2)\ln(1+x^2)+(1+x^2)-(1-x^2)\ln(1-x^2)}{(1-x^4)(1+x^2)}\right] x\ \exp\left[\frac{x^2-1}{x^2+1}\right]\ dx\\
&=\color{blue}{-\frac14\exp\left[\frac{\pi^2-16}{\pi^2+16}\right]\ln \left|\frac{16-\pi^2}{16+\pi^2}\right|}.
\end{align*}


$$

