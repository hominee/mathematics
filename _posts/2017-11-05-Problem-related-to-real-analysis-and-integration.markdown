---
layout: post
title: Problem related to real analysis and integration
tag:
 - real-analysis
 - calculus
 - integration

description: Problem related to real analysis and integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

prove $$\int_0^\infty \frac{\log^2(x)}{x^2+1}\mathrm dx=\frac{\pi^3}{8}$$ with real methods

<!–-break-–>


Context: we looked up "complex residue" on google images, and saw this integral.
 I, being unfamiliar with the use of contour integration, decided to try proving the result without complex analysis.

we are  attempting to prove that 


$$

J=\int_0^\infty\frac{\log^2(x)}{x^2+1}\mathrm dx=\frac{\pi^3}8

$$


With real methods because we do not know complex analysis.

we have started with the substitution $$x=\tan u$$:


$$

J=\int_0^{\pi/2}\log^2(\tan x)\mathrm dx

$$




$$

J=\int_0^{\pi/2}\log^2(\cos x)\mathrm dx-2\int_{0}^{\pi/2}\log(\cos x)\log(\sin x)\mathrm dx+\int_0^{\pi/2}\log^2(\sin x)\mathrm dx

$$


But frankly, this is basically worse.




**Update**: Wait we think we actually found a viable method


$$

F(\alpha)=\int_0^\infty \frac{x^{\alpha}}{x^2+1}\mathrm dx

$$


As we have shown in other posts of mine,


$$

\int_0^\infty\frac{x^{2b-1}}{(1+x^2)^{a+b}}\mathrm dx=\frac12\mathrm{B}(a,b)=\frac{\Gamma(a)\Gamma(b)}{2\Gamma(a+b)}

$$


so 


$$

F(\alpha)=\frac12\Gamma\left(\frac{1+\alpha}2\right)\Gamma\left(\frac{1-\alpha}2\right)

$$


And from 


$$

\Gamma(1-s)\Gamma(s)=\frac\pi{\sin \pi s}

$$


we see that


$$

F(\alpha)=\frac\pi{2\cos\frac{\pi \alpha}{2}}

$$


So 

$$

J=F''(0)=\frac{\pi^3}8

$$


Okay while we have just found a proof, we would like to see which ways you did it.


# Answer 


Pretty straightforward this integral can be related to the Dirichlet Beta Function $$\beta(s)$$ and its integral representation which is given by



$$

\beta(s)~=~\frac1{\Gamma(s)}\int_0^\infty \frac{t^{s-1}}{e^{t}+e^{-t}}\mathrm dt

$$



Therefore, enforce the substitution $$x=e^{-t}$$ within your integral $$J$$ to obtain

$$
\begin{align*}
J=\int_0^\infty\frac{\log^2(x)}{1+x^2}\mathrm dx &= \int_{-\infty}^\infty\frac{t^2}{1+e^{-2t}}e^{-t}\mathrm dt\\
&=\int_0^\infty\frac{t^2}{1+e^{-2t}}e^{-t}\mathrm dt+\underbrace{\int_{-\infty}^0\frac{t^2}{1+e^{-2t}}e^{-t}\mathrm dt}_{t~\mapsto~ -t}\\
&=\int_0^\infty\frac{t^2}{e^t+e^{-t}}\mathrm dt+\int_0^\infty\frac{t^2}{1+e^{2t}}e^t\mathrm dt\\
&=2\int_0^\infty\frac{t^2}{e^t+e^{-t}}\mathrm dt\\
&=2\Gamma(3)\beta(3)
\end{align*}
$$


$$

\therefore~J~=~2\int_0^\infty\frac{t^2}{e^t+e^{-t}}\mathrm dt~=~\frac{\pi^3}8

$$



The result follows from the known value $$\beta(3)=\frac{\pi^3}{32}$$ for which a proofcan be found here for instance. The validity of the integral representation can be shown by utilizing the geometric series of the denominator combined with the change of summation and integration, which is allowed in this case, and followed by applying the Defintion of the Dirichlet Beta Function and the Gamma Function.

