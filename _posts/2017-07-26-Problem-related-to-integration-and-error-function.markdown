---
layout: post
title: Problem related to integration and error function
tag:
 - integration
 - improper-integrals
 - closed-form
 - hypergeometric-function
 - error-function

description: Problem related to integration and error function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Integral $$\int_0^\infty\exp\left(-\sqrt2\,x^2\right)\,\operatorname{erfi}(x)\,\log(x)\,x^3\,dx$$

<!–-break-–>


Consider the following integral:

 $$ 
\mathcal{A}=\int_0^\infty\exp\left(-\sqrt2\,x^2\right)\,\operatorname{erfi}(x)\,\log(x)\,x^3\,dx,\tag1
 $$ 

where $$\operatorname{erfi}(x)$$ denotes the imaginary error function:

 
$$

\begin{align*}\operatorname{erfi}(x)&=\frac2{\sqrt\pi}\int_0^x\exp
\left(z^2\right)dz\tag2\\&={_1F_1}\left(\frac12;\frac32;x^2\right)\cdot\frac{2\,x}{\sqrt\pi}.\end{align*}
\tag3
 $$ 

To evaluate it, I tried to replace the power $$3$$ with a parameter $$\alpha$$ and remove the logarithmic factor, and I got this:

 $$ 
\int_0^\infty\exp\left(-\sqrt2\,x^2\right)\,\operatorname{erfi}(x)\,x^\alpha\,dx=\frac{_2F_1\left(\frac12,\frac\alpha2+1;\frac32;\frac1{\sqrt{2}}\right)\,\Gamma\left(\frac\alpha2+1\right)}{2^{\alpha/4}\,\sqrt{2\pi}}.\tag4
 $$ 

Now taking a derivative with respect $$x<1$$ to the parameter $$\alpha$$ and substituting $$\alpha=3$$ should give me the desired result:

 $$ 
\mathcal{A}=\frac{\sqrt{7+5\sqrt2}}{48\sqrt2}\left(\left(3-\sqrt2\right)\cdot(16-15\log2-6\gamma)+9\sqrt{10-7\sqrt2}\cdot\mathcal{D}\right),\tag5
 $$ 

where 

 $$ 
\mathcal{D}=\left|\partial_\beta\Bigg(_2 F_1 \left(\frac12,\beta;\tfrac32;\frac1{\sqrt2}\right)\Bigg)\right|_{\beta=5/2}\tag6
 $$


The problem is I do not know how to evaluate the $$\mathcal{D}$$ term — how to take a derivative of the hypergeometric function with respect to the parameter $$\beta$$.

# Answer 


There is an explicit expression for the value of this integral that does not rely on derivatives of hypergeometric indices.  The idea is to simply use the definition of erfi and reverse the order of integration.  The integral we want is then

 $$ 
\mathcal{A}=\frac{2}{\sqrt{\pi}}\int_0^1 dt \, \int_0^{\infty} dx \, e^{-(\sqrt{2}-t^2) x^2} \, x^4 \, \log{x}
 $$ 

Really, all you need to know is that

 $$ 
\int_0^{\infty} dx \, e^{-x^2} \log{x} =  \frac12 \left [\frac{d}{d\beta}\Gamma\left (\frac{\beta+1}{2}\right ) \right ]_{\beta=0} = -\frac{\sqrt{\pi}}{4} (\gamma+\log{4})
 $$ 

Then

 
$$

\begin{align*}\int_0^{\infty} dx \, e^{-\alpha x^2} \, x^4 \, \log{x} &= \frac{d^2}{d \alpha^2} \int_0^{\infty} dx \, e^{-\alpha x^2} \, \log{x}  \\&= -\frac{\sqrt{\pi } (3 \log (\alpha)+3 \gamma -8+3 \log (4))}{16 \alpha^{5/2}}\end{align*}

$$
 

So what we have here is the messy but very doable integral

 $$ 
(8 - 3 \gamma - 6 \log{2}) \frac{\sqrt{\pi}}{16} \int_0^1 dt \, \left (\sqrt{2}-t^2 \right )^{-5/2} - \frac{3 \sqrt{\pi}}{16} \int_0^1 dt \, \left (\sqrt{2}-t^2 \right )^{-5/2} \log{\left (\sqrt{2}-t^2 \right )} 
 $$ 

With these integrals, we make the substitution $$t = 2^{1/4} \sin{\theta}$$, etc.  We end up having to evaluate the following integrals

 $$ 
\int d\theta \, \sec^4{\theta} = \frac13 \tan^3{\theta} + \tan{\theta}+C
 $$ 


 
$$

\begin{align*}\int d\theta \, \sec^4{\theta}\,  \log{(\cos{\theta})} &= \left [\frac13 \tan^3{\theta} + \tan{\theta} \right ] \log{(\cos{\theta})} \\&+ \frac13 \left [\frac13 \tan^3{\theta} + 2 \tan{\theta}  - 2 \theta \right]+C \end{align*}

$$
 

over $$t \in [0,\arcsin{2^{-1/4}}]$$.  I leave out the details of the arithmetic; the final result one gets upon evaluating the above integrals at the endpoints of the $$t$$ interval is

 $$ 
\mathcal{A}=\frac{2 (3+ \sqrt{2})-[  \gamma +2 \log (2)+ \log{\left(\sqrt{2}-1\right)}]\left(4+ \sqrt{2}\right)}{16 \left(\sqrt{2}-1\right)^{1/2}}+\frac14 \arcsin\left(2^{-1/4}\right)
 $$ 

which is about $$0.538106$$, matching a numerical evaluation of the original integral.

