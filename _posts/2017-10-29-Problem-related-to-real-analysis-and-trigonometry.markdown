---
layout: post
title: Problem related to real analysis and trigonometry
tag:
 - real-analysis
 - integration
 - trigonometry

description: Problem related to real analysis and trigonometry

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Evaluating $$\int_0^\infty \sin x^2\, dx$$ with real methods?

<!–-break-–>


we have seen the Fresnel integral


$$

\int_0^\infty \sin x^2\, dx = \sqrt{\frac{\pi}{8}}

$$


evaluated by contour integration and other complex analysis methods, and we have found these methods to be the standard way to evaluate this integral.
  we was wondering, however, does anyone know a real analysis method to evaluate this integral?
.


# Answer 


Let $$u=x^2$$, then


$$


   \int_0^\infty \sin(u) \frac{\mathrm{d} u}{2 \sqrt{u}}


$$


The real analysis way of evaluating this integral is to consider a parametric family:


$$




$$
\begin{eqnarray*}

    I(\epsilon) &=& \int_0^\infty \frac{\sin(u)}{2 \sqrt{u}} \mathrm{e}^{-\epsilon u} \mathrm{d} u = \frac{1}{2} \sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)!}\int_0^\infty u^{2n+\frac{1}{2}} \mathrm{e}^{-\epsilon u} \mathrm{d} u \\ &=& \frac{1}{2} \sum_{n=0}^\infty \frac{(-1)^n}{(2n+1)!} \Gamma\left(2n+\frac{3}{2}\right) \epsilon^{-\frac{3}{2}-2n} \\
  &=& \frac{1}{2 \epsilon^{3/2}} \sum_{n=0}^\infty \left(-\frac{1}{\epsilon^2}\right)^n\frac{\Gamma\left(2n+\frac{3}{2}\right)}{\Gamma\left(2n+2\right)} \\
  &\stackrel{\Gamma-\text{duplication}}{=}&\frac{1}{2 \epsilon^{3/2}} \sum_{n=0}^\infty \left(-\frac{1}{\epsilon^2}\right)^n\frac{\Gamma\left(n+\frac{3}{4}\right)\Gamma\left(n+\frac{5}{4}\right)}{\sqrt{2} n! \Gamma\left(n+\frac{3}{2}\right)} \\
   &=& \frac{1}{(2 \epsilon)^{3/2}} \frac{\Gamma\left(\frac{3}{4}\right)\Gamma\left(\frac{5}{4}\right)}{\Gamma\left(\frac{3}{2}\right)} {}_2F_1\left(\frac{3}{4}, \frac{5}{4}; \frac{3}{2}; -\frac{1}{\epsilon^2}\right) \\
  &\stackrel{\text{Euler integral}}{=}& \frac{1}{(2 \epsilon)^{3/2}} \frac{\Gamma\left(\frac{3}{4}\right)\Gamma\left(\frac{5}{4}\right)}{\Gamma\left(\frac{3}{2}\right)} \frac{1}{\operatorname{B}\left(\frac{5}{4}, \frac{3}{2}-\frac{5}{4}\right)} \int_0^1 x^{\frac{5}{4}-1} (1-x)^{\frac{3}{2}-\frac{5}{4} -1} \left(1+\frac{x}{\epsilon^2}\right)^{-3/4} \mathrm{d} x \\
  &=& \frac{1}{2^{3/2}} \frac{\Gamma\left(\frac{3}{4}\right)\Gamma\left(\frac{5}{4}\right)}{\Gamma\left(\frac{3}{2}\right)} \frac{\Gamma\left(\frac{3}{2}\right)}{\Gamma\left(\frac{5}{4}\right) \Gamma\left(\frac{1}{4}\right)} \int_0^1 x^{\frac{5}{4}-1} (1-x)^{\frac{1}{4} -1} \left(\epsilon^2+x\right)^{-3/4} \mathrm{d} x

\end{eqnarray*}


$$


$$


Now we are ready to compute $$\lim_{\epsilon \to 0} I(\epsilon)$$:


$$




$$
\begin{eqnarray*}

  \lim_{\epsilon \to 0} I(\epsilon) &=& \frac{1}{2^{3/2}} \frac{\Gamma\left(\frac{3}{4}\right)}{\Gamma\left(\frac{1}{4}\right)} \int_0^1 x^{\frac{1}{2}-1} \left(1-x\right)^{\frac{1}{4}-1} \mathrm{d} x = \frac{1}{2^{3/2}} \frac{\Gamma\left(\frac{3}{4}\right)}{\Gamma\left(\frac{1}{4}\right)} \frac{\Gamma\left(\frac{1}{2}\right) \Gamma\left(\frac{1}{4}\right)}{\Gamma\left(\frac{3}{4}\right)} \\ &=& \frac{1}{2^{3/2}} \Gamma\left(\frac{1}{2}\right) = \frac{1}{2} \sqrt{\frac{\pi}{2}}

\end{eqnarray*}


$$


$$



