---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - real-analysis
 - integration
 - definite-integrals
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Prove that $$\int_0^\infty \frac{e^{\cos(ax)}\cos\left(\sin (ax)+bx\right)}{c^2+x^2}dx =\frac{\pi}{2c}\exp\left(e^{-ac}-bc\right)$$

<!–-break-–>


In my course, we have to prove formula below


$$

I=\int_0^\infty \frac{e^{\cos(ax)}\cos\left(\sin (ax)+bx\right)}{c^2+x^2}dx =\frac{\pi}{2c}\exp\left(e^{-ac}-bc\right)

$$


for $$a,b,c>0.$$
we know that this integral can be easily solved with complex analysis using


$$

f(z)=\frac{1}{2} \ \mathbb{R} \left(\int_{-\infty}^\infty \frac{\exp\left(e^{iaz}+ibz\right)}{c^2+z^2}dz\right)

$$


but right now we are  in a course dealing with real analysis. we tried to use parametrization integral method


$$

I'(a)=-\int_0^\infty \frac{xe^{\cos(ax)}\sin(\sin(ax)+(a+b)x)}{c^2+x^2}dx 

$$


but it doesn't look easier to handle. we tried to differentiate it again, but we just got a horrible form. An idea came to mind to differentiate with respect to parameter $$b$$ and set a differential equation


$$

I''(b)+x^2I(b)=0

$$


plugging this ODE to W \| A, we got


$$

I(b)=c_1\cos(bx^2)+c_2\sin(bx^2)

$$


It's definitely wrong! After seeing Samrat's answer, we tried to plug in again to W\|A and we got


$$

I(b)=c_1 D_{-1/2}((i+1)b)+c_2 D_{-1/2}((i-1)b)

$$


where $$D_n(z)$$ is the parabolic cylinder function but we have no idea what does that mean.
Any idea? Thanks in advance.

# Answer 




$$

\begin{aligned}
\int_0^{\infty} \frac{e^{\cos(ax)}\cos(\sin(ax)+bx)}{x^2+c^2}\,dx &=\Re\left(\int_0^{\infty} \frac{e^{e^{iax}}e^{ibx}}{x^2+c^2}\right) \\
&=\Re\left(\sum_{k=0}^{\infty} \frac{1}{k!}\int_0^{\infty} \frac{e^{i(ak+b)x}}{x^2+c^2}\,dx\right)\\
&=\sum_{k=0}^{\infty} \frac{1}{k!}\int_0^{\infty}\frac{\cos((ak+b)x)}{x^2+c^2}\,dx \\
&=\frac{\pi}{2c}\sum_{k=0}^{\infty} \frac{1}{k!}e^{-c(ak+b)}\\
&=\frac{\pi}{2c}e^{-bc}\sum_{k=0}^{\infty} \frac{e^{-kac}}{k!}\\
&=\frac{\pi}{2c}e^{-bc}e^{e^{-ac}}=\boxed{\dfrac{\pi}{2c}\exp\left(e^{-ac}-bc\right)} \\
\end{aligned}

$$



we used the following result:


$$

\int_0^{\infty} \frac{\cos(mx)}{x^2+a^2}=\frac{\pi}{2a}e^{-am}

$$



