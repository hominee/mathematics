---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - integration
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

tough integral involving $$\sin(x^2)$$ and $$\sinh^2 (x)$$

<!–-break-–>


we ran across this integral we get no where with.
 Can someone suggest a method of attack?.



$$

\int_0^{\infty}\frac{\sin(\pi x^2)}{\sinh^2 (\pi x)}\mathrm dx=\frac{2-\sqrt{2}}{4}

$$


we tried series, imaginary parts, and so forth, but have made no progress.
  
Thanks very much.
 


# Answer 


Although this question is two years old, the integral was mentioned in chat recently, we evaluated it, and then found this question. Since there is no complete solution, although Hans Lundmark's suggestion is excellent and similar in nature, we are  posting what we have done.
Contours
Since the integrand is even,







$$
\begin{align*}

\int_0^\infty\frac{\sin(\pi x^2)}{\sinh^2(\pi x)}\,\mathrm{d}x
&=\frac12\int_{-\infty}^\infty\frac{\sin(\pi x^2)}{\sinh^2(\pi x)}\,\mathrm{d}x

\end{align*}


$$





Define


$$


f(z)=\frac{\cos\left(\pi z^2\right)}{\sinh(2\pi z)\sinh^2(\pi z)}


$$




**Note** that because


$$


f(x\pm i)
=\frac{-\cos\left(\pi x^2\right)\cosh(2\pi x)\pm i\sin\left(\pi x^2\right)\sinh(2\pi x)}{\sinh(2\pi x)\sinh^2(\pi x)}\\


$$


we have








$$
\begin{align*}

\int_\gamma f(z)\,\mathrm{d}z
&=\int_{-\infty}^\infty\big[f(x-i)-f(x+i)\big]\,\mathrm{d}x\\
&=-2i\int_{-\infty}^\infty\frac{\sin(\pi x^2)}{\sinh^2(\pi x)}\,\mathrm{d}x\\
&=2\pi i\times\begin{array}{}\text{the sum of the residues}\\\text{inside the contour}\end{array}

\end{align*}


$$





where $$\gamma$$ is the contour
$$\hspace{3.2cm}$$
Therefore,


$$


\int_0^\infty\frac{\sin(\pi x^2)}{\sinh^2(\pi x)}\,\mathrm{d}x
=-\frac\pi2\times\begin{array}{}\text{the sum of the residues}\\\text{inside the contour}\end{array}


$$


Residues
near $$0$$ :






$$
\begin{align*}

f(z)
&=\frac{\cos\left(\pi z^2\right)}{\sinh(2\pi z)\sinh^2(\pi z)}\\
&=\frac{1-\frac12\pi^2z^4+O(z^8)}{2\pi z\left(1+\frac23\pi^2z^2+O(z^4)\right)\pi^2 z^2\left(1+\frac13\pi^2z^2+O(z^4)\right)}\\
&=\frac{1-\pi^2z^2}{2\pi^3z^3}+O(z)\\[10pt]
&\implies\text{residue}=-\frac1{2\pi}

\end{align*}


$$





at $$\pm i/2$$, use L'Hosptal :








$$
\begin{align*}

\text{residue}
&=\lim_{z\to\pm i/2}\frac{(z\mp i/2)\cos\left(\pi z^2\right)}{\sinh(2\pi z)\sinh^2(\pi z)}\\
&=\frac1{2\pi\cosh(\pm\pi i)}\frac{\cos(-\pi/4)}{\sinh^2(\pm\pi i/2)}\\
&=\frac1{2\pi\cos(\pm\pi)}\frac{\sqrt2/2}{-\sin^2(\pm\pi/2)}\\[4pt]
&=\frac{\sqrt2}{4\pi}

\end{align*}


$$





near $$\pm i$$ :







$$
\begin{align*}

f(z\pm i)
&=\frac{-\cos\left(\pi z^2\right)\cosh(2\pi z)\pm i\sin\left(\pi z^2\right)\sinh(2\pi z)}{\sinh(2\pi z)\sinh^2(\pi z)}\\
&=\frac{-\left(1-\frac12\pi^2z^4+O(z^8)\right)\left(1+2\pi^2z^2+O(z^4)\right)+O(z^3)}{2\pi z\left(1+\frac23\pi^2z^2+O(z^4)\right)\pi^2 z^2\left(1+\frac13\pi^2z^2+O(z^4)\right)}\\
&=-\frac{1+\pi^2z^2}{2\pi^3z^3}+O(1)\\[10pt]
&\implies\text{residue}=-\frac1{2\pi}

\end{align*}


$$





Result
Thus,








$$
\begin{align*}

\int_0^\infty\frac{\sin(\pi x^2)}{\sinh^2(\pi x)}\,\mathrm{d}x
&=-\frac\pi2\left(-\frac1{2\pi}-\frac1{2\pi}+\frac{\sqrt2}{4\pi}+\frac{\sqrt2}{4\pi}\right)\\[6pt]
&=\frac{2-\sqrt2}{4}

\end{align*}


$$






