---
layout: post
title: integral related to digamma function
tags:
  - integral 
  - closed-form
  - digamma-function
  - harmonic-numbers
  - real-analysis
  
description:  
  integral related to digamma function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$

\sum_{n=1}^\infty\frac{(-1)^n\,H_{n/5}}n

$$



<!–-break-–>

Let $$H_q$$ denote harmonic numbers (generalized to a non-integer index $$q$$):

$$
H_q=\sum_{k=1}^\infty\left(\frac1k-\frac1{k+q}\right)=\int_0^1\frac{1-x^q}{1-x}dx=\gamma+\psi(q+1),\tag1
$$

where $$\psi(z)=\Gamma'(z)/\Gamma(z)$$ is the [digamma function](http://mathworld.wolfram.com/DigammaFunction.html).

My goal is to evaluate the following series:

$$
\mathcal S_m=\sum_{n=1}^\infty\frac{(-1)^n\,H_{n/m}}n.\tag2
$$

Using the integral representation from $$(1)$$ we can get equivalent integral forms:

$$
\mathcal S_m=\int_0^1\frac{\ln(1+\sqrt[m]x)-\ln2}{1-x}\,dx=m\int_0^1\frac{\ln(1+z)-\ln2}{1-z^m}\,z^{m-1}dz.\tag3
$$

Here are some simple cases:

$$

\begin{align*}
\mathcal S_1=\frac{\ln^22}2-\frac{\pi^2}{12} \hspace{7.7em}\color{maroon}{\mathcal S_2=\ln^22-\frac{\pi^2}{12}}\\
\color{blue}{\mathcal S_3=\frac{3\ln^22}2-\frac{\pi^2}9+\frac12\,\operatorname{Li}_2\!\left(\tfrac14\right)} 
\hspace{2em}\color{green}{\mathcal S_4=\frac{7\ln^22}4-\frac{5\pi^2}{48}}
\end{align*} 
\tag4
$$

For $$\mathcal S_5$$ the integral can be found using _Mathematica_ (there is even a closed-form antiderivative, so it should be possible in principle to prove it by differentiation), but the result takes tens of thousands characters to write down (you can see it [here](http://goo.gl/QocWP0)), and _Mathematica_ cannot do much simplification on it ([here](http://goo.gl/4r1gsc) is a simplified result).


# Answer


 1. Formula (3) can be rewritten as 

$$
\mathcal{S}_m=-m\int_0^1\frac{\ln\frac{1+z}{2}}{z^m-1}z^{m-1}dz=-m\sum_{k=0}^{m-1}\alpha_{km}\int_0^1\frac{\ln\frac{1+z}{2}}{z-e^{2\pi i k/m}}dz,
$$

where

$$
\alpha_{km}=\lim_{\quad z\to\; \exp{\frac{2\pi i k}m}}\frac{z^{m-1}\left(z-e^{2\pi i k/m}\right)}{z^m-1}=\frac{e^{2\pi i k(m-1)/m}}{\prod_{n\ne k}\left(e^{2\pi i k/m}-e^{2\pi i n/m}\right)}=\frac1m.
$$

Note in particular that the last expression is independent of $$k$$. 

 2. The remaining integrals can be computed in terms of polylogarithms:

$$
I\left(\zeta\right)=\int_0^1\frac{\ln\frac{1+z}{2}}{z-\zeta}dz=
\operatorname{Li}_2\left(\frac{2}{1+\zeta}\right)-
\operatorname{Li}_2\left(\frac{1}{1+\zeta}\right)+
\ln2\ln\frac{\zeta}{1+\zeta}.\tag{1}
$$

We have in particular

$$
I\left(1\right)=\frac{\pi^2}{12}-\frac{\ln^22}{2},\qquad
I\left(-1\right)=-\frac{\ln^22}{2}. 
$$


This implies that

$$
\mathcal{S}_m=-\sum_{k=0}^{m-1}I\left(e^{2\pi i k/m}\right), \tag{2}
$$

with $$I\left(\zeta\right)$$ defined by (1). It is clear that under the sum the elementary pieces of $$I(\zeta)$$ simplify. It might happen that something nice happens also with the dilogarithmic ones.


----------
**Update 1** (how to simplify one of the two sums of dilogarithms to an elementary expression):

 - [This formula](http://functions.wolfram.com/ZetaFunctionsandPolylogarithms/PolyLog2/03/01/0002/) for $$\operatorname{Li}_2\left(e^{2\pi i \mathbb{Q}}\right)$$ implies that

$$
\sum_{k=0}^{m-1}\operatorname{Li}_2\left(e^{2\pi i k/m}\right)=\frac{\pi^{2}}{6m},\qquad
\sum_{k=0}^{m-1}\operatorname{Li}_2\left(-e^{2\pi i k/m}\right)=\begin{cases}\quad \frac{\pi^{2}}{6m},\quad & m\text{ even}, \\ -\frac{\pi^{2}}{12m},\quad & m \text{ odd}.
\end{cases}

$$

 - We also have the identity $$\operatorname{Li}_2\left(z\right)=-\operatorname{Li}_2\left(\frac{z}{z-1}\right)-\frac12\ln^2\left(1-z\right)$$, which can be rewritten as

$$
\operatorname{Li}_2\left(\frac{1}{\zeta+1}\right)=-\operatorname{Li}_2\left(-\zeta^{-1}\right)-\frac12\ln^2\frac{\zeta}{\zeta+1}.
$$


 - Combining both results, we obtain for odd $$m$$

$$
\sum_{k=0}^{m-1}\operatorname{Li}_2\left(\frac{1}{1+e^{2\pi i k/m}}\right)=
\frac{\pi^2}{12m}-\frac12\sum_{k=0}^{m-1}\ln^2\left(1+e^{-2\pi i k /m}\right),
$$

and for even $$m$$

$$
\sum_{k=0 \mid k\neq \frac{m}{2}}^{m-1}\operatorname{Li}_2\left(\frac{1}{1+e^{2\pi i k/m}}\right)=
\frac{\pi^2(m-1)}{6m}-\frac12\sum_{k=0\mid k\neq \frac{m}{2}}^{m-1}\ln^2\left(1+e^{-2\pi i k /m}\right).
$$



----------
**Update 2** (simplification of the remaining sum for even $$m$$):

We can use again the identity $$\operatorname{Li}_2\left(z\right)=-\operatorname{Li}_2\left(\frac{z}{z-1}\right)-\frac12\ln^2\left(1-z\right)$$ to show that

$$
\operatorname{Li}_2\left(\frac{2}{1+\zeta}\right)+\operatorname{Li}_2\left(\frac{2}{1-\zeta}\right)=-\frac12\ln^2\frac{\zeta-1}{\zeta+1}.
$$

For even $$m$$, if $$\zeta$$ is an $$m$$th root of unity, then so is $$-\zeta$$, which simplifies the second sum to an elementary expression:

$$
\sum_{k=0 \mid k\neq \frac{m}{2}}^{m-1}\operatorname{Li}_2\left(\frac{2}{1+e^{2\pi i k/m}}\right)=\frac{\pi^2}{12}-\frac{\ln^2 2}{2}-\frac12\sum_{k=1}^{\frac{m}{2}-1}\ln^2\frac{e^{2\pi i k/m}-1}{e^{2\pi i k/m}+1}.
$$

Altogether, this leads to evaluation

$$
\begin{align*}
\mathcal{S}_{2n}&=\frac{\ln 2\ln 8n^2}{2}-\frac{\pi^2}{12n}+\frac12
\sum_{k=1}^{n-1}\ln^2\frac{e^{\pi i k/n}-1}{e^{\pi i k/n}+1}-\frac12\sum_{k=0\mid k\neq n}^{2n-1}\ln^2\left(1+e^{-\pi i k /n}\right)=\\
&=\ln 2\ln 2n-\frac{\pi^2\left(n^2+1\right)}{24n}-\sum_{k=1}^{n-1}\ln\left(2\sin\frac{\pi k}{2n}\right)\ln\left(2\cos\frac{\pi k}{2n}\right).
\tag{\spadesuit}
\end{align*}
$$

----------
**Update 3** (partial simplification for odd $$m$$)

Let us denote $$m=2n+1$$. We will use the identity

$$
\operatorname{Li}_2\left(\frac{2}{1+\zeta}\right)=\operatorname{Li}_2\left(\frac{\zeta+1}{\zeta-1}\right)+\frac12 \ln^2 \frac{\zeta-1}{\zeta+1}
-\ln\left(-\frac{2}{1+\zeta}\right)\ln\frac{\zeta-1}{\zeta+1}-\frac{\pi^2}{6}. \tag{3}
$$

Now the key three facts are that 

 - If $$\zeta$$ is $$\zeta^m=1$$, then so is $$\zeta^{-1}$$. 

 - Under replacement $$\zeta\leftrightarrow \zeta^{-1}$$, the dilogarithm argument on the right of (3) changes its sign.

 - There is an identity $$\operatorname{Li}_2\left( z\right)+ \operatorname{Li}_2\left( - z\right)=\frac{1}{2}\operatorname{Li}_2\left( z^2\right)$$.

Put altogether, this leads to
 
$$
\begin{align*}\sum_{k=0}^{m-1}\operatorname{Li}_2\left(\frac{2}{1+e^{\frac{2\pi i k}{m}}}\right)=&\frac12\sum_{k=1}^n\operatorname{Li}_2\left(-\cot^2\frac{\pi k}{2n+1}\right)+\frac{4n^2+3n+2}{2n+1}\cdot\frac{\pi^2}{12}+\\ &+\sum_{k=1}^n\ln\left(\tan\frac{\pi k}{2n+1}\right)
\ln\left(\frac12\sin\frac{2\pi k}{2n+1}\right).
\end{align*}
$$

Combining this with the previous results of Update 1, we finally arrive at

$$
\begin{align*}
\nonumber\mathcal{S}_{2n+1} 
&= -\frac{1}{2}\sum_{k=1}^n \operatorname{Li}_2\left(-\cot^2\frac{\pi k}{2n+1}\right)-\sum_{k=1}^n\ln^2\sin\frac{\pi k}{2n+1}+\\
&+\left(n+\frac12\right)\ln^2 2-\frac{\left(2n^2+n+1\right)\pi^2}{12\left(2n+1\right)}.  \tag \clubsuit
\end{align*} 
 $$

*Remark*. For $$n=2$$ (i.e. $$m=5$$) this sum contains two dilogarithms

$$
\operatorname{Li}_2\left(-1\pm\frac{2}{\sqrt5}\right)$$. One should be able to reduce them to just one $$\operatorname{Li}_2\left(\frac15\right)
$$ 

using a suitable identity.