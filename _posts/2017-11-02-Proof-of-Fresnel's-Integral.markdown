---
layout: post
title: Proof of Fresnel's Integral
tag:
 - calculus
 - complex-analysis
 - hyperbolic-functions
 - elementary-functions
 - fresnel-integrals

description: Proof of Fresnel's Integral

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proof of Fresnel's Integral

<!–-break-–>


So, my teacher wants us to prove the Fresnel's integral:


$$

\int_0^\infty\cos(x^2)dx=\sqrt{\frac{\pi}{8}}

$$


The problem is that we cannot use complex analysis to prove that and we should do that using the Euler identity:


$$

\int_0^\infty\cos(x^2)dx=\frac{1}{2}\int_0^\infty e^{iw^2}dw+\frac{1}{2}\int_0^\infty e^{-iw^2}dw

$$

 
But we have that integral of $$e^{-iw^2}$$ and we cannot solve that :(
we are  an engineering student, so basically, we only have the "basic" calculus, just simple/double/triple integrals, some notions about series, ODE's and PDE's, but nothing as deep as in the regular Math degree, so probably there's no need to use hard stuff to figure this out.


# Answer 


Hint: note that 

$$

I=\int_{0}^{\infty}\cos\left(x^{2}\right)dx\stackrel{x^{2}=u}{=}\frac{1}{2}\int_{0}^{\infty}u^{-1/2}\cos\left(u\right)du
 

$$

 

$$

=\frac{1}{2\sqrt{\pi}}\int_{0}^{\infty}\cos\left(u\right)\int_{0}^{\infty}v^{-1/2}e^{-uv}dvdu
 

$$

 and now using the Fubini theorem we can exchange the integrals and get 

$$

I=\frac{1}{2\sqrt{\pi}}\int_{0}^{\infty}v^{-1/2}\int_{0}^{\infty}\cos\left(u\right)e^{-uv}dudv=\textrm{Re}\left(\frac{1}{2\sqrt{\pi}}\int_{0}^{\infty}v^{-1/2}\int_{0}^{\infty}e^{u\left(i-v\right)}dudv\right)
 

$$

 

$$

\textrm{Re}\left(\frac{1}{2\sqrt{\pi}}\int_{0}^{\infty}\frac{v^{-1/2}}{v-i}dv\right)=\frac{1}{2\sqrt{\pi}}\int_{0}^{\infty}\frac{v^{1/2}}{v^{2}+1}dv\stackrel{z=\sqrt{v}}{=}\frac{1}{\sqrt{\pi}}\int_{0}^{\infty}\frac{z^{2}}{z^{4}+1}dz
 

$$

 and the last integral is simple to evaluate using partial fractions. 

**Note** that 

$$

\int_{0}^{\infty}\frac{z^{2}}{z^{4}+1}dz=\frac{1}{2\sqrt{2}}\left(\int_{0}^{\infty}\frac{z}{z^{2}-\sqrt{2}z+1}-\frac{z}{z^{2}+\sqrt{2}z+1}dz\right)
 

$$

 

$$

=\frac{1}{2\sqrt{2}}\left(\lim_{a\rightarrow\infty}\frac{1}{2}\int_{0}^{a}\frac{2z-\sqrt{2}+\sqrt{2}}{z^{2}-\sqrt{2}z+1}-\frac{2z+\sqrt{2}-\sqrt{2}}{z^{2}+\sqrt{2}z+1}dz\right)
 

$$

 

$$

=\frac{1}{2\sqrt{2}}\left(\lim_{a\rightarrow\infty}\frac{1}{2}\int_{0}^{a}\frac{2z-\sqrt{2}}{z^{2}-\sqrt{2}z+1}-\frac{2z+\sqrt{2}-\sqrt{2}}{z^{2}+\sqrt{2}z+1}dz+\int_{0}^{a}\frac{\sqrt{2}}{z^{2}-\sqrt{2}z+1}dz\right)

$$

 and we think you can conclude by yourself from here.

