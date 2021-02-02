---
layout: post
title: sum related to Harmonic number
tags:
  - sum  
  - closed-form
  - Harmonic-number
  - Bernoulli-numbers
  - real-analysis
  
description:  
  sum related to Harmonic number
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :

$$

\sum_{n=1}^\infty\left(H_n-\,2H_{2n}+H_{4n}\right)^2

$$


<!–-break-–>

There is a known asymptotic expansion of [harmonic numbers](http://mathworld.wolfram.com/HarmonicNumber.html) $$H_n$$ for $$n\to\infty$$:


$$
\begin{align*} 
H_n&=\gamma+\ln n+\sum_{k=1}^\infty\left(-\frac{B_k}{k\cdot n^k}\right)\\
&=\gamma+\ln n+\frac{1}{2n}-\frac{1}{12n^2}+\frac{1}{120n^4}-\frac{1}{252n^6}\,+\,\dots,
\end{align*} 
\tag1
$$

where $$B_k$$ are [Bernoulli numbers](http://mathworld.wolfram.com/HarmonicNumber.html).
We can take a linear combination of harmonic numbers to cancel constant and logarithmic terms, compensate for $$O(n^{-1})$$ term, and get the following series that is possible to evaluate in a closed form (e.g. using generating function):

$$
\sum_{k=1}^\infty\left(H_n-\,2H_{2n}+H_{4n}-\frac1{8n}\right)=\frac18-\frac\pi{16}.\tag2
$$

Rather than compensating for $$O(n^{-1})$$ term, we can take a series with alternating signs, that is also possible to evaluate in a closed form:

$$
\sum_{n=1}^\infty\,(-1)^n\,\Big(H_n-\,2H_{2n}+H_{4n}\Big)=\frac{3\pi}{16}-\frac{\pi}{4\sqrt2}-\frac{\ln2}{8}.\tag3
$$

Generalizing, we can consider two families of series:

$$
\mathcal A_m=\sum_{n=1}^\infty\,(-1)^n\,\Big(H_n-\,2H_{2n}+H_{4n}\Big)^m,\tag4
$$


$$
\mathcal B_m=\sum_{n=1}^\infty\Big(H_n-\,2H_{2n}+H_{4n}\Big)^m,\tag5
$$

and try to evaluate them in a closed form.

---
the following conjectured result:
 
$$
\large\sum_{n=1}^\infty \Big(H_n-\,2H_{2n}+H_{4n}\Big)^2 
=\frac\pi8-\frac\pi{16} \,\ln2-\frac{\pi^2}{96}+\frac3{16}\,\ln^22-\frac{G}{4},
\tag{\diamond}
$$


where $$G$$ is the [Catalan constant](http://en.wikipedia.org/wiki/Catalan%27s_constant).

# Answer

So basically, I'll evaluate a bunch of integrals, trying to avoid polylogs as much as possible. 

First thing is to notice that $$\displaystyle H_n-2H_{2n}+H_{4n}=\int_0^1 \frac{x^{2n}-x^{4n}}{1+x}dx$$.
I noticed that $$H_n-2H_{2n}+H_{4n}=H_{4n}-H_{2n}-(H_{2n}-H_n)=H_{4n^{-}}-H_{(2n)^{-}}$$, where $$H_{n^{-}}=\sum_{k=1}^{n} \frac{(-1)^{k+1}}{k}$$ is called
a *skew harmonic number* (at least by **Khristo N. Boyadzhiev**. [link.](https://www.sav.sk/journals/uploads/0123134909Boyadz.pdf)) Knowing they have  a simple intergal representation I found the above. My answer is influenced by [Boyadzhiev's work.](http://arxiv.org/ftp/arxiv/papers/1203/1203.4618.pdf)
If I make any unexplainable substitution, it's most likely $$t=\frac{1-x}{1+x}$$.
Also, I'm not very good with Latex, so alignment should be awful. Hopefully there are no typos.

Below, easy enough to prove, is what I take for granted:
$$ -\ln\sin x=\ln2+\sum_{n=1}^{\infty} \frac{\cos(2nx)}{n} ,-\ln\cos x=\ln2+\sum_{n=1}^{\infty} \frac{(-1)^n\cos(2nx)}{n} \tag{1}$$


$$
 \int_0^{\frac{\pi}{2}} \cos x \cos(nx)dx=\begin{cases} \frac{\pi}{4} &n=1\\0 &n \,\,\text{odd}\\ \frac{(-1)^{1+n/2}}{n^2-1} &n \,\,\text{even} \end{cases} \tag{2}
$$



$$
 \int_0^1 \frac{\ln(1-x)}{a+x}dx=-\operatorname{Li_2}\left(\frac1{a+1}\right)\tag{3}
$$

Starting, 

$$
\sum_{n=0}^{\infty}(H_{n}-2H_{2n}+H_{4n})^2=\sum_{n=0}^{\infty}\int_0^1\int_0^1\frac{(x^{2n}-x^{4n})(u^{2n}-u^{4n})}{(1+x)(1+u)}dxdu
\\=\small\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1-x^2u^2)}-2\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1-x^2u^4)}+\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1-x^4u^4)}
\\=I_{22}-2I_{24}+I_{44}
$$




**Computing $$I_{22}$$.**

Substitute $$u=\frac{y}{x}$$ ,change the order of integration, evaluate the inner integral, and substitue $$t=\frac{1-x}{1+x}$$ to get


$$
\begin{align*} I_{22}=\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1-x^2u^2)}=\int_0^1\int_0^x\frac{dydx}{(1+x)(x+y)(1-y^2)}
\\=\int_0^1 \frac1{1-y^2}\int_1^y \frac{dx}{(1+x)(x+y)} dy=\int_0^1 \frac{\ln\left(\frac{(1+x)^2}{4x}\right)}{(1+x)(1-x^2)}\,dx
\\=\frac{-1}{4}\int_0^1 \frac{(1+t)}{t^2}\ln(1-t^2)dt=-\frac14\int_0^1\frac{\ln(1-t^2)}{t^2}dt-\frac14\int_0^1\frac{\ln(1-t^2)}{t}dt
\\=\frac14\sum_{n=0}^{\infty} \frac1{(n+1)(2n+1)}+\frac14\sum_{n=0}^{\infty} \frac1{(n+1)(2n+2)}=\frac{\ln2}{2}+\frac{\pi^2}{48}.\end{align*} 

$$




**Computing $$I_{44}$$.**

Start the same as with $$I_{22}$$ to get $$\displaystyle I_{44}=\int_0^1 \frac{\ln\left(\frac{(1+x)^2}{4x}\right)}{(1-x)(1-x^4)}\,dx=\frac{-1}{8}\int_0^1 \frac{\ln(1-t^2)}{t^2(1+t^2)}(1+t)^3dt$$.
We can calculate these integrals:


$$
\begin{align*} 
\int_0^1 \frac{\ln(1-x^2)}{1+x^2}dx=\int_0^1 \frac{\ln(1+x)}{1+x^2}dx+\int_0^1 \frac{\ln(1-x)}{1+x^2}dx \tag{4} 
\\=\int_0^1 \frac{\ln(1+x)}{1+x^2}dx +\int_0^1 \frac{\ln\left(\frac{2t}{1+t}\right)}{1+t^2}dt
\\=\frac{\pi}{4}\ln2+\sum_{n=0}^{\infty} (-1)^n\int_0^1\ln(t) t^{2n}dt=\frac{\pi}{4}\ln2-G.
 \end{align*} 

$$


$$

\begin{align*} \int_0^1 \frac{\ln(1-x^2)}{x^2(1+x^2)}dx=\int_0^1 \frac{\ln(1-x^2)}{x^2}dx-\int_0^1 \frac{\ln(1-x^2)}{1+x^2}dx \tag{5}
\\=-\sum_{n=0}^{\infty} \frac1{n+1}\int_0^1 x^{2n}dx-\frac{\pi}{4}\ln2+G=G-\frac{\pi}{4}\ln2-2\ln2.\end{align*} 

$$


$$

\begin{align*} \int_0^1 \frac{x\ln(1-x^2)}{1+x^2}dx=\frac12\int_0^1 \frac{\ln(1-x)}{1+x}dx \tag{6}
\\=-\frac12 \operatorname{Li_2}\left(\frac12\right)=\frac{\ln^2 2}{4}-\frac{\pi^2}{24}.\end{align*} 

$$


$$

\begin{align*} \int_0^1 \frac{\ln(1-x^2)}{x(1+x^2)}dx=\int_0^1 \frac{\ln(1-x^2)}{x}dx-\int_0^1 \frac{x\ln(1-x^2)}{1+x^2}dx \tag{7}
\\=-\sum_{n=0}^{\infty}\frac1{n+1}\int_0^1 x^{2n+1}dx-\frac{\ln^2 2}{4}+\frac{\pi^2}{24}=-\frac{\pi^2}{24}-\frac{\ln^2 2}{4}.\end{align*} 

$$

Altogether,

$$
I_{44}=\frac{-1}{8}\int_0^1 \frac{\ln(1-x^2)}{x^2(1+x^2)}(1+3x+3x^2+x^3)dx
\\=-\frac{\pi}{16}\ln2+\frac{\ln2}{4}+\frac{\ln^2 2}{16}+\frac{\pi^2}{48}+\frac{G}{4}.
$$


---

**Computing $$I_{24}$$.**

Substitute $$u=\frac{y}{x^2}$$, change the order of integration, let $$y\to y^2$$, evaluate the inner integral,and substitue $$t=\frac{1-x}{1+x}$$:

$$
\begin{align*} I_{24}=\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1-x^4u^2)}=\int_0^1\int_0^{x^2} \frac{dydx}{(1+x)(x^2+y)(1-y^2)}
\\=\int_0^1 \frac1{1-y^2}\int_{\sqrt{y}}^1\frac{dx}{(1+x)(x^2+y)}dy=2\int_0^1\frac{y}{1-y^4}\int_{y}^1\frac{dx}{(1+x)(x^2+y^2)}dy
\\=2\int_0^1\frac{\tan^{-1}\left(\frac{1-x}{1+x}\right)}{(1+x^2)(1-x^4)}dx-2\int_0^1\frac{x\ln\left(\frac{(1+x)\sqrt{1+x^2}}{2\sqrt{2}x}\right)}{(1+x^2)(1-x^4)}dx
=I_{241}-I_{242}. \end{align*}
$$


---

*Evaulation of $$I_{241}$$.* 

Substitute $$t=\frac{1-x}{1+x}$$ to get $$\displaystyle I_{241}=\frac14\int_0^1 \frac{\tan^{-1}(t)}{t(1+t^2)^2}(1+t)^4dt$$.

We can calculate these integrals.In the following, let $$x=\tan\theta$$:

$$

\begin{align*} \int_0^1 \frac{\tan^{-1}(x)}{(1+x^2)^2}dx=\int_0^{\frac{\pi}{4}}\theta\cos^2(\theta)d\theta=\frac{\pi^2}{64}+\frac{\pi}{16}-\frac18.\tag{8}\end{align*} 

$$


$$

\begin{align*} \int_0^1 \frac{x\tan^{-1}(x)}{(1+x^2)^2}dx=\int_0^{\frac{\pi}{4}}\theta\tan\theta\cos^2{\theta}d\theta=\frac12\int_0^{\frac{\pi}{4}}\theta\sin(2\theta)d\theta=\frac18.\tag{9}\end{align*} 

$$


$$

\begin{align*} \int_0^1 \frac{x^2\tan^{-1}(x)}{(1+x^2)^2}dx=\int_0^{\frac{\pi}{4}}\theta\sin^2(\theta)d\theta=\frac{\pi^2}{64}-\frac{\pi}{16}+\frac18.\tag{10}\end{align*} 

$$


$$

\begin{align*} \int_0^1 \frac{x^3\tan^{-1}(x)}{(1+x^2)^2}dx=\int_0^{\frac{\pi}{4}}\theta\sin^3(\theta)\sec{\theta}\,d\theta \tag{11}
\\=\int_0^{\frac{\pi}{4}}\theta\tan\theta \,d\theta-\int_0^{\frac{\pi}{4}}\theta\sin\theta\cos\theta \,d\theta=\frac{\pi}{8}\ln2-\frac18+\int_0^{\frac{\pi}{4}}\ln\cos\theta \,d\theta
\\=\frac{\pi}{8}\ln2-\frac18-\int_0^{\frac{\pi}{4}}\ln2 \,d\theta-\sum_{n=1}^{\infty} \frac{(-1)^n}{n}\int_0^{\frac{\pi}{4}}\cos(2n\theta)\,d\theta
\\=-\frac{\pi}{8}\ln2-\frac18+\frac12\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n^2}\sin(\frac{\pi n}{2})=\frac{G}{2}-\frac{\pi}{8}\ln2-\frac18.\end{align*} 
 $$



$$

\begin{align*} \int_0^1 \frac{\tan^{-1}(x)}{x(1+x^2)^2}dx=\int_0^{\frac{\pi}{4}}\theta\cos^3(\theta)\csc{\theta}\,d\theta \tag{12}
\\=\int_0^{\frac{\pi}{4}}\theta\cot\theta \,d\theta-\int_0^{\frac{\pi}{4}}\theta\sin\theta\cos\theta \,d\theta=-\frac18-\frac{\pi}{8}\ln2-\int_0^{\frac{\pi}{4}}\ln\sin\theta \,d\theta
\\=-\frac18-\frac{\pi}{8}\ln2+\int_0^{\frac{\pi}{4}}\ln2 \,d\theta+\sum_{n=1}^{\infty}\frac1{n}\int_0^{\frac{\pi}{4}}\cos(2n\theta)\,d\theta
\\=-\frac18+\frac{\pi}{8}\ln2+\frac12\sum_{n=1}^{\infty} \frac{\sin(\frac{\pi n}{2})}{n^2}=\frac{G}{2}+\frac{\pi}{8}\ln2-\frac18.\end{align*} 
 $$


Altogether,

$$
I_{241}=2\int_0^1\frac{\tan^{-1}\left(\frac{1-x}{1+x}\right)}{(1+x^2)(1-x^4)}dx= \frac14\int_0^1 \frac{\tan^{-1}(x)}{x(1+x^2)^2}(1+4x+6x^2+4x^3+x^4)dx
\\=\frac{\pi^2}{32}+\frac18+\frac{G}{4}
$$


---

*Evaulation of $$I_{242}$$.*

Substitute $$t=\frac{1-x}{1+x}$$ to get 

$$
 I_{242}=\frac14\int_0^1 \frac{\ln\left(\frac{\sqrt{1+t^2}}{1-t^2}\right)}{t(1+t^2)^2}(1-t^2)(1+t)^2dt
\\=\frac12\int_0^1 \frac{\ln\left(\frac{\sqrt{1+t^2}}{1-t^2}\right)}{(1+t^2)^2}(1-t^2)dt+\frac14\int_0^1 \frac{\ln\left(\frac{\sqrt{1+t^2}}{1-t^2}\right)}{t(1+t^2)}(1-t^2)dt
\\=\frac12\int_0^1 \frac{\ln\left(\frac{1+x^2}{1-x^2}\right)}{(1+x^2)^2}(1-x^2)dx-\frac14\int_0^1\frac{\ln(1+x^2)}{(1+x^2)^2}(1-x^2)dx\\+\frac18\int_0^1\frac{\ln(1+x^2)(1-x^2)}{x(1+x^2)}dx-\frac14\int_0^1\frac{\ln(1-x^2)(1-x^2)}{x(1+x^2)}dx

$$

Calculating these integrals: 

$$

\begin{align*} \int_0^1 \frac{\ln\left(\frac{1+x^2}{1-x^2}\right)}{(1+x^2)^2}(1-x^2)dx=-\frac12\int_0^1 \frac{\ln\left(\frac{1-x}{1+x}\right)}{\sqrt{x}(1+x)}\frac{1-x}{1+x}dx \tag{13}
\\=-\frac12\int_0^1\frac{t\ln t}{\sqrt{1-t^2}}dt=-\frac18\int_0^1\frac{\ln t}{\sqrt{1-t}}dt=-\frac18\int_0^1 t^{-1/2}\ln(1-t)dt
\\=\frac14\sum_{n=0}^{\infty} \frac1{(n+1)(2n+3)}=\frac12-\frac{\ln2}{2}.\end{align*} 
 $$



$$
\tag{14}
\begin{align*} 
\int_0^1 \frac{\ln(1+x^2)(1-x^2)}{x(1+x^2)}dx 
&=\frac{1}{2}\int_0^1 \frac{\ln(1+x)(1-x)}{x(1+x)}dx \\  
&=\frac{1}{2}\int_0^1\frac{\ln(1+x)}{x}dx-\int_0^1\frac{\ln(1+x)}{1+x}dx\\
&=\frac{1}{2}\sum_{n=0}^{\infty}\frac{(-1)^{n+1}}{n+1}\int_0^1 x^n dx-\frac{1}{2}\ln^2(1+x)\bigg{|}_0^1 \\
&=\frac{\pi^2}{24}-\frac{\ln^2 2}{2}.
\end{align*} 
 $$



$$

\begin{align*} \int_0^1\frac{\ln(1-x^2)(1-x^2)}{x(1+x^2)}dx=\frac12\int_0^1\frac{\ln(1-x)}{x}dx-\int_0^1\frac{\ln(1-x)}{1+x}dx \tag{15}
\\=-\frac{\pi^2}{12}-\left(\frac{\ln^2 2}{2}-\frac{\pi^2}{12}\right)=-\frac{\ln^2 2}{2}.\end{align*} 
 $$



$$
 
\int_0^1\frac{\ln(1+x^2)}{(1+x^2)^2}(1-x^2)dx=-2\int_0^{\frac{\pi}{4}}\cos^2(\theta)(1-\tan^2\theta)\ln\cos\theta\,d\theta \tag{16}
\\=-2\int_0^{\frac{\pi}{4}}\cos(2\theta)\ln\cos\theta\,d\theta=2\ln2\int_0^{\frac{\pi}{4}}\cos(2\theta)d\theta+\sum_{n=1}^{\infty} \frac{(-1)^n}{n}\int_0^{\frac{\pi}{2}}\cos\theta \cos(n\theta)d\theta
\\=\ln2-\frac{\pi}{4}+\sum_{n=1}^{\infty} \frac{(-1)^{2n}}{2n}\frac{(-1)^{n+1}}{(2n)^2-1}=\frac{\ln2}{2}-\frac{\pi}{4}+\frac12.
$$

Altogether, $$\displaystyle I_{242}=\frac{\pi^2}{192}+\frac{\pi}{16}+\frac{\ln^2 2}{16}-\frac{3\ln2}{8}+\frac18$$,

leading to $$\displaystyle I_{24}=I_{241}-I_{242}=\frac{5\pi^2}{192}-\frac{\pi}{16}-\frac{\ln^2 2}{16}+\frac{3\ln2}{8}+\frac{G}{4}$$,
and finally, confirming the conjecture,

$$
\sum_{n=0}^{\infty}(H_{n}-2H_{2n}+H_{4n})^2=I_{22}-2I_{24}+I_{44}=\frac{\pi}{8}-\frac{\pi}{16}\ln2-\frac{\pi^2}{96}+\frac{3\ln^2 2}{16}-\frac{G}{4}.
$$


---

I don't know about higher powers. I guess the case $$\mathcal A_2$$ can also be done. If we start the same as with $$\mathcal B_2$$, writing $$\mathcal A_2=J_{22}-2J_{24}+J_{44}$$
we can find that $$\displaystyle J_{22}=\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1+x^2u^2)}=2I_{44}-I_{22}=-\frac{\pi}{8}\ln2+\frac{G}{2}+\frac{\pi^2}{48}+\frac{\ln^2 2}{8}$$

$$J_{44}$$ can be reduced to $$\displaystyle =-\frac12\int_0^1 \frac{\ln(1-x^2)}{x(x^4+6x^2+1)}(1+x)^3 dx$$.
already this i can't evaulate fully, as polylogs are inescapable. Factorizing $$x^2+6x+1=(x+3+2\sqrt{2})(x+3-2\sqrt{2}).$$

I can get $$\displaystyle \int_0^1 \frac{\ln(1-x^2)}{x(x^4+6x^2+1)}dx=-\frac{\pi^2}{12}+\frac{4-3\sqrt{2}}{16}\operatorname{Li_2}\left(\frac{2-\sqrt{2}}{4}\right)+\frac{4+3\sqrt{2}}{16}\operatorname{Li_2}\left(\frac{2+\sqrt{2}}{4}\right)$$

but nothing more.

*Edit 1.*

After some more work and a fair amount of cancellation, we obtain 

$$
\int_0^1 \frac{\ln(1-x^2)}{x(x^4+6x^2+1)}(1+x)^3 dx=\frac{1+2\sqrt{2}}{4}\pi\ln2-\frac{\pi^2}{24}-\frac14\ln\left(\frac{2+\sqrt{2}}{4}\right)\ln\left(\frac{2-\sqrt{2}}{4}\right) \\
-\frac{\sqrt{2}+1}{2}\Im\operatorname{Li_2}\left(\frac{2+\sqrt{2}}{2}+\frac{i\sqrt{2}}{2}\right)-\frac{\sqrt{2}-1}{2}\Im\operatorname{Li_2}\left(\frac{2-\sqrt{2}}{2}+\frac{i\sqrt{2}}{2}\right)
$$


I obtained it by calculating $$\displaystyle \int_0^1 \frac{\ln(1+x)}{x+a}dx=\ln2\ln\left(\frac{a+1}{a-1}\right)+\operatorname{Li_2}\left(\frac2{1-a}\right)-\operatorname{Li_2}\left(\frac1{1-a}\right)$$, 
which together with $$(3)$$ can be used to give a closed form for $$\displaystyle \int_0^1\frac{\ln(1-x^2)}{x+a}dx$$, which in turn, through partial fractions, can be used to give a closed form for $$\displaystyle \int_0^1\frac{\ln(1-x^2)}{x^2+a^2}dx$$.
Fortunately, things didn't get too ugly as both $$3+2\sqrt{2}$$ and $$3-2\sqrt{2}$$ have nice square roots. I will fill in details as soon as I can.

Now we just need to evaluate $$J_{24}$$. Starting similarly as with $$I_{24}$$, 
we have:

$$
J_{24}=\int_0^1\int_0^1\frac{dxdu}{(1+x)(1+u)(1+x^4u^2)}
\\=2\int_0^1\frac{\tan^{-1}\left(\frac{1-x}{1+x}\right)}{(1+x^2)(1+x^4)}dx-2\int_0^1\frac{x\ln\left(\frac{(1+x)\sqrt{1+x^2}}{2\sqrt{2}x}\right)}{(1+x^2)(1+x^4)}dx
\\=J_{241}-J_{242}
$$


Through $$t=\frac{1-x}{1+x}$$, $$J_{241}$$ turns to $$\displaystyle \int_0^1 \frac{\tan^{-1}(x)}{(1+x^2)(x^4+6x^2+1)}(1+x)^4\,dx$$. I don't have any idea about that yet. 
