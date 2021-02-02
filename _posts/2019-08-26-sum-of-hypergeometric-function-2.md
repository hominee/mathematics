---
layout: post
title: sum related to hypergeometric function 2
tags:
  - sum  
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  sum related to hypergeometric function 2
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Prove that:


$$

\sum_{n=0}^{\infty}{2^n(n^2-n\pi+1)(n^2+n-1)\over (2n+1)(2n+3){2n\choose n}}=1

$$

 


<!–-break-–


# Answer

This answer  is divided  into  several steps.

**Overview:** 

At first  we show

$$

\sum_{n=1}^\infty\frac{(2x)^{2n}}{n\binom{2n}{n}}=\frac{2x}{\sqrt{1-x^2}}\arcsin(x)\qquad\qquad  |x|<1\tag{1}

$$

With   a    *small  trick* we derive the generating function

$$

\sum_{n=0}^\infty\frac{(2x)^{2n}}{(2n+1)\binom{2n}{n}}
=\frac{1}{x\sqrt{1-x^2}}\arcsin(x)

$$

just as intermediate step to derive the following series as basis for further calculations:

$$
\begin{align*}
A(x):=\frac{1}{2}\sum_{n=0}^\infty\frac{(2x)^{n}}{(2n+3)(2n+1)\binom{2n}{n}}
=\frac{1}{x}-\frac{1}{x}\sqrt{\frac{2}{x}-1}\cdot\arcsin\left(\sqrt{\frac{x}{2}}\right)
\end{align*}
$$

Since  we have to additionally respect the factor $$(n^2-n\pi+1)(n^2+n-1)$$ in the numerator of OPs series we apply the differential operator $$D_x$$ and calculate from $$A(x)$$

$$
\begin{align*}
(xD_x)^kA(x)&=\frac{1}{2}\sum_{n=0}^\infty\frac{n^k(2x)^{n}}{(2n+3)(2n+1)\binom{2n}{n}}\qquad\qquad k=1,\ldots,4
\end{align*}
$$

These are  the *building blocks* to finally calculate OPs series.


$$  $$


**Generating function with reciprocal central binomial coefficient:**

The central binomial coefficient can be represented with the *[Betafunction](https://en.wikipedia.org/wiki/Beta\_function)* as

$$
\begin{align*}
\frac{1}{\binom{2n}{n}}&=\frac{\left(n!\right)^2}{(2n)!}=\frac{n\Gamma(n)\Gamma(n+1)}{\Gamma(2n+1)}\\
&=n\beta(n+1,n)\\
&=n\int_0^1t^n(1-t)^{n-1}
\end{align*}
$$

We obtain

$$
\begin{align*}
\sum_{n=1}^\infty\frac{(2x)^{2n}}{n\binom{2n}{n}}&=\sum_{n=1}^\infty(2x)^{2n}\int_0^1t^n(1-t)^{n-1}dt\\
&=\frac{1}{1-t}\int_0^1\sum_{n=1}^\infty(4x^2t)^n(1-t)^{n}dt\\
&=\frac{1}{1-t}\int_0^1\frac{4x^2t}{1-4x^2t(1-t)}dt
\end{align*}
$$

Substituting $$x(2t-1)=s$$ gives

$$
\begin{align*}
x(2t-1)&=s\qquad &x^2(4t^2-4t+1)&=s^2\\
2xdt&=ds\qquad &4x^2t^2-4x^2t&=s^2-x^2
\end{align*}
$$

We get

$$
\begin{align*}
\sum_{n=1}^\infty\frac{(2x)^{2n}}{n\binom{2n}{n}}&=\int_{-x}^x\frac{s+x}{s^2+(1-x^2)}ds\\
&=\left.\frac{1}{2}\log(s^2-x^2+1)\right|_{-x}^{x}+\left.\frac{x}{1-x^2}\arctan\left(\frac{s}{\sqrt{1-x^2}}\right)\right|_{-x}^x\\
&=\frac{2x}{\sqrt{1-x^2}}\arctan\left(\frac{x}{\sqrt{1-x^2}}\right)\\
&=\frac{2x}{\sqrt{1-x^2}}\arcsin\left(\frac{\frac{x}{\sqrt{1-x^2}}}{\sqrt{\frac{x^2}{1-x^2}+1}}\right)\\
&=\frac{2x}{\sqrt{1-x^2}}\arcsin\left(x\right)\\
\end{align*}
$$

and (1) follows.


$$
 
$$


**Generating function of $$A(x)$$:**

We derive a generating function for

$$
\begin{align*}
A(x)=\frac{1}{2}\sum_{n=0}^\infty\frac{(2x)^{n}}{(2n+3)(2n+1)\binom{2n}{n}}\tag{2}
\end{align*}
$$

We do it in three steps. At first we show

$$
\begin{align*}
\sum_{n=0}^\infty\frac{(2x)^{n}}{(2n+1)\binom{2n}{n}}=\frac{1}{x\sqrt{1-x^2}}\arcsin(x)\tag{3}
\end{align*}
$$

Since 

$$
\begin{align*}
\frac{1}{2n+1}\binom{2n}{n}^{-1}&=\frac{1}{2n+1}\cdot\frac{(n!)^2}{(2n)!}\cdot\frac{2(n+1)^2}{2(n+1)^2}\\
&=\frac{2}{n+1}\cdot\frac{((n+1)!)^2}{(2n+2)!}\\
&=\frac{2}{n+1}\binom{2n+2}{n+1}^{-1}\tag{4}
\end{align*}
$$

we get from (1)

$$
\begin{align*}
\sum_{n=0}^\infty\frac{(2x)^{2n}}{(2n+1)\binom{2n}{n}}
&=2\sum_{n=0}^\infty\frac{(2x)^{2n}}{(n+1)\binom{2n+2}{n+1}}\\
&=2\sum_{n=1}^\infty\frac{(2x)^{2n-2}}{n\binom{2n}{n}}\\
&=\frac{1}{x\sqrt{1-x^2}}\arcsin(x)\\
&=1+\frac{2}{3}x^2+\frac{8}{15}x^4+\frac{16}{35}x^6+\frac{128}{315}x^8+\cdots
\end{align*}
$$

Substituting $$n$$ with $$n+1$$ in (4) gives

$$
\begin{align*}
\frac{1}{2n+3}\binom{2n+2}{n+1}^{-1}=\frac{2}{n+2}\binom{2n+4}{n+2}^{-1}
\end{align*}
$$

We get from (2)

$$
\begin{align*}
\sum_{n=0}^\infty\frac{(2x)^{2n}}{(2n+3)\binom{2n+2}{n+1}}
&=2\sum_{n=0}^\infty\frac{(2x)^{2n}}{(n+2)\binom{2n+4}{n+2}}\tag{5}\\
&=2\sum_{n=2}^\infty\frac{(2x)^{2n-4}}{n\binom{2n}{n}}\\
&=\frac{1}{4x^3\sqrt{1-x^2}}\arcsin(x)-\frac{1}{4x^2}\\
&=\frac{1}{6}+\frac{2}{15}x^2+\frac{4}{35}x^4+\frac{32}{315}x^6+\frac{64}{693}x^8+\cdots
\end{align*}
$$

On the other hand we get from (4)

$$
\begin{align*}
\frac{1}{2n+3}\binom{2n+2}{n+1}^{-1}=\frac{1}{2n+3}\cdot\frac{n+1}{2n+1}\cdot \frac{1}{2}\binom{2n}{n}^{-1}
\end{align*}
$$

and from this identity we obtain from (5)

$$
\begin{align*}
\sum_{n=0}^\infty\frac{(2x)^{2n}}{(2n+3)\binom{2n+2}{n+1}}
&=\frac{1}{2}\sum_{n=0}^\infty\frac{(n+1)(2x)^{2n}}{(2n+3)(2n+1)\binom{2n}{n}}\tag{6}\\
&=\frac{1}{4x^3\sqrt{1-x^2}}\arcsin(x)-\frac{1}{4x^2}
\end{align*}
$$

We want to get rid of $$n+1$$ in the numerator in (6) in order    to obtain the series $$A(x)$$. We  substitute

$$
\begin{align*}
x\rightarrow \sqrt{\frac{u}{2}}
\end{align*}
$$

and then we integrate the series.

We obtain from (6) by this substitution

$$
\begin{align*}
\sum_{n=0}^\infty\frac{2^{n-1}(n+1)}{(2n+3)(2n+1)\binom{2n}{n}}u^n
&=\frac{1}{4\left(\frac{u}{2}\right)^{\frac{3}{2}}\sqrt{1-\frac{u}{2}}}\arctan\left(\sqrt{\frac{u}{2}}\right)-\frac{1}{2u}\tag{7}\\
&=\frac{1}{u\sqrt{u(2-u)}}\arcsin\left(\sqrt{\frac{u}{2}}\right)-\frac{1}{2u}\\
&=\frac{1}{6}+\frac{1}{15}u+\frac{1}{35}u^2+\frac{4}{315}u^3+\frac{4}{693}u^4+\frac{8}{3003}u^5+\cdots
\end{align*}
$$

Integrating the RHS of (7) with the help of Wolfram Alpha gives $$A(u)$$.

$$
\begin{align*}
A(u)&=\sum_{n=0}^\infty\frac{2^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}u^n\\
&=\frac{1}{u}-\frac{1}{u}\sqrt{\frac{2}{u}-1}\cdot\arcsin\left(\sqrt{\frac{u}{2}}\right)\tag{8}\\
&=\frac{1}{6}+\frac{1}{30}u+\frac{1}{105}u^2+\frac{1}{315}u^3+\frac{4}{3465}u^4+\frac{4}{9009}u^5+\cdots\\
\end{align*}
$$

and the claim (2) follows.


$$
 
$$


**Building blocks: $$(uD_u)^kA(u)$$**

The next step is to successively apply the operator $$uD_u$$ on $$A(u)$$ with $$D_u$$ the differential operator. We obtain with some help of Wolfram Alpha

$$
\begin{align*}\
(uD_u)A(u)&=\sum_{n=0}^\infty\frac{n2^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}u^n\\
&=-\frac{3}{2u}+\frac{3-u}{u^2\sqrt{\frac{2}{u}-1}}\cdot\arcsin\left(\sqrt{\frac{u}{2}}\right)\tag{9}\\
&=\frac{1}{30}u+\frac{2}{105}u^2+\frac{1}{105}u^3+\frac{16}{3465}u^4+\frac{20}{9009}u^5+\cdots\\
\\
(uD_u)^2A(u)&=\sum_{n=0}^\infty\frac{n^22^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}u^n\\
&=\frac{4u-9}{2u(u-2)}+\frac{u^2-7u+9}{u^2(u-2)\sqrt{\frac{2}{u}-1}}\cdot\arcsin\left(\sqrt{\frac{u}{2}}\right)\tag{10}\\
&=\frac{1}{30}u+\frac{4}{105}u^2+\frac{1}{35}u^3+\frac{64}{3465}u^4+\frac{100}{9009}u^5+\cdots\\
\\
(uD_u)^3A(u)&=\sum_{n=0}^\infty\frac{n^32^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}u^n\\
&=-\frac{5u^2-25u+27}{2u(u-2)^2}-\frac{u^3-13u^2+34u-27}{u^2(u-2)^2\sqrt{\frac{2}{u}-1}}\cdot\arcsin\left(\sqrt{\frac{u}{2}}\right)\tag{11}\\
&=\frac{1}{30}u+\frac{8}{105}u^2+\frac{3}{35}u^3+\frac{256}{3465}u^4+\frac{500}{9009}u^5+\cdots\\
\\
(uD_u)^4A(u)&=\sum_{n=0}^\infty\frac{n^42^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}u^n\\
&=\frac{6u^3-53u^2+115u-81}{2u(u-2)^3}\\
&\qquad+\frac{u^4-23u^3+89u^2-142u+81}{u^2(u-2)^3\sqrt{\frac{2}{u}-1}}\cdot\arcsin\left(\sqrt{\frac{u}{2}}\right)\tag{12}\\
&=\frac{1}{30}u+\frac{16}{105}u^2+\frac{9}{35}u^3+\frac{1024}{3465}u^4+\frac{2500}{9009}u^5+\cdots\\
\end{align*}
$$


**Building blocks at $$u=1$$**

We have now all the building blocks we need and derive from (8) to (12) some nice identities by setting $$u=1$$ and noting that $$\arcsin\left(\frac{1}{\sqrt{2}}\right)=\frac{\pi}{4}$$.

$$
\begin{align*}
A(1)&=\sum_{n=0}^\infty\frac{2^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}} \\
=1-\frac{1}{4}\pi \left.(uD_u)A(u)\right|_{u=1} \\
&=\sum_{n=0}^\infty\frac{n2^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}=-\frac{3}{2}+\frac{1}{2}\pi\\
\left.(uD_u)^2A(u)\right|_{u=1}&=\sum_{n=0}^\infty\frac{n^22^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}=\frac{5}{2}-\frac{3}{4}\pi\\
\left.(uD_u)^3A(u)\right|_{u=1}&=\sum_{n=0}^\infty\frac{n^32^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}=-\frac{7}{2}+\frac{5}{4}\pi\\
\left.(uD_u)^4A(u)\right|_{u=1}&=\sum_{n=0}^\infty\frac{n^42^{n-1}}{(2n+3)(2n+1)\binom{2n}{n}}=\frac{13}{2}-\frac{3}{2}\pi
\end{align*}
$$


**OPs series:**

Since

$$

(n^2-n\pi+1)(n^2+n-1)=n^4+(1-\pi)n^3-\pi n^2+(1+\pi)n-1

$$

We obtain by putting all together in OPs series

$$
\begin{align*}
\sum_{n=0}^{\infty}&{2^n(n^2-n\pi+1)(n^2+n-1)\over (2n+1)(2n+3){2n\choose n}}\\
&=\sum_{n=0}^{\infty}{2^n(n^4+(1-\pi)n^3-\pi n^2+(1+\pi)n-1)\over (2n+1)(2n+3){2n\choose n}}\\
&=2\left.(uD_u)^4A(u)\right|_{u=1}+2(1-\pi)\left.(uD_u)^3A(u)\right|_{u=1}\\
&\qquad-2\pi\left.(uD_u)^2A(u)\right|_{u=1}+2(1+\pi)\left.(uD_u)A(u)\right|_{u=1}-2A(1)\\
&=2\left(\frac{13}{2}-\frac{3}{2}\pi\right)+2(1-\pi)\left(-\frac{7}{2}+\frac{5}{4}\pi\right)
-2\pi\left(\frac{5}{2}-\frac{3}{4}\pi\right)\\
&\qquad+2(1+\pi)\left(-\frac{3}{2}+\frac{1}{2}\pi\right)-2\left(1-\frac{1}{4}\pi\right)\\
&=1
\end{align*}
$$

and the claim follows.

**Note:** The proof of (1) is Theorem 1 in B. Sury's paper *[Identities Involving Reciprocals of Binomials](https://cs.uwaterloo.ca/journals/JIS/VOL7/Sury/sury99.pdf)*. The *small trick* can be found e.g. in the proof of Theorem 2.1 in *[Sums of reciprocals of the central binomial coefficients](https://www.emis.de/journals/INTEGERS/papers/g27/g27.pdf)* by R. Sprugnoli.