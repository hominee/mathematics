---
layout: post
title: Problem related to calculus and definite integrals
tag:
 - calculus
 - integration
 - complex-analysis
 - definite-integrals

description: Problem related to calculus and definite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Integral $$\int_0^\infty\sin{(x^4)} dx$$

<!–-break-–>



# Answer 


Consider the contour integral $$\int_{\Gamma(R)} e^{-z^4}\, dz$$, where $$\Gamma(R)$$ is the first quadrant sector of the quarter circle (centered at the origin), subtended by the angle $$\pi/8$$, with counterclockwise orientation. Then $$\Gamma = \gamma_1 + \gamma_2 + \gamma_3$$, where $$\gamma_1$$ is the line segment from $$0$$ to $$R$$, $$\gamma_2$$ is the arc of the sector, and $$\Gamma_3$$ is the line segment from $$Re^{i\pi/8}$$ to $$0$$. Along $$\gamma_2$$, $$z = Re^{it}$$, $$0 \le t \le \pi/8$$, so 


$$

\|e^{-z^4}\| = \|e^{-R^4(\cos 4t+ i\sin 4t)}\| = e^{-R^4\cos 4t}.

$$


Since $$\cos 4t \ge 1 - 8t/\pi$$ for $$0 \le t \le \pi/8$$, $$\|e^{-z^4}\| \le e^{-R^4}e^{8R^4t/\pi}$$. Therefore


$$

\left\|\int_{\gamma_2} e^{-z^4}\, dz\right\| \le e^{-R^4}\int_0^{\pi/8} e^{8R^4t/\pi} R\, dt = Re^{-R^4}\cdot \frac{\pi(e^{R^4} -

1)}{8R^4} = \frac{\pi}{8R^3}(1 - e^{-R^4})

$$


The last expression tends to $$0$$ as $$R\to \infty$$. Since $$\int_{\Gamma(R)} e^{-z^4}\, dz = 0$$ by Cauchy's theorem, we have


$$

0 = \lim_{R\to \infty} \left(\int_{\gamma_1} e^{-z^4}\, dz + \int_{\gamma_3} e^{-z^4}\, dz\right).

$$

 
Along $$\gamma_3$$, $$z = re^{i\pi/8}$$, $$0 \le r \le R$$. Thus


$$

\int_{\gamma_3} e^{-z^4}\, dz = -\int_0^R e^{-r^4e^{i\pi/2}}\, e^{i\pi/8}\, dr = -e^{i\pi/8}\int_0^R e^{-ir^4}\, dr.

$$


Since 


$$

\int_{\gamma_1} e^{-z^4}\, dz + \int_{\gamma_3} e^{-z^4}\, dz = \int_0^R e^{-x^4}\, dx - e^{i\pi/8} \int_0^R e^{-ix^4}\, dx,

$$


we deduce that 



$$
\begin{align*}
0 &= \int_0^\infty e^{-x^4}\, dx - \int_0^\infty e^{-i(x^4 - \pi/8)}\, dx\\
0&= \Gamma(5/4) - \int_0^\infty [\cos(x^4 - \pi/8) + i \sin(x^4 - \pi/8)]\, dx\\
\Gamma(5/4)&= - \int_0^\infty (\cos(x^4)\cos(\pi/8) + \sin(x^4)\sin(\pi/8))\, dx\\& + \int_0^\infty (\sin(x^4)\cos(\pi/8) - \cos(x^4)\sin(\pi/8))\, dx
\end{align*}


$$

Taking the real and imaginary parts, we obtain a system of equations



$$
\begin{align*}

A\cos \pi/8 + B\sin \pi/8 &= \Gamma(5/4)\\
-A\sin \pi/8 + B\cos \pi/8 &= 0

\end{align*}


$$

Here $$A = \int_0^\infty \cos(x^4)\, dx$$ and $$B = \int_0^\infty \sin(x^4)\, dx$$. The solution is 



$$
\begin{align*}

A &= \cos(\pi/8)\Gamma(5/4)\\
B &= \sin(\pi/8)\Gamma(5/4)

\end{align*}


$$

That is,


$$

\int_0^\infty \sin x^4\, dx = \sin(\pi/8)\Gamma(5/4), \quad \int_0^\infty \cos x^4\, dx = \cos(\pi/8)\Gamma(5/4).

$$



