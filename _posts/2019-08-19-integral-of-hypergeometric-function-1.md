---
layout: post
title: integral related to hypergeometric function 1
tags:
  - integration   
  - definite-integrals
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  integral related to hypergeometric function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$
 S(m) = \sum_{n=1}^\infty \frac{2^n \cdot n^m}{\binom{2n}n}    
$$

Notation: $$  \dbinom{2n}n $$  denotes the central binomial coefficient, $$  \dfrac{(2n)!}{(n!)^2} $$.

<!–-break-–>

We have the following examples (all verified by WolframAlpha) for $$  m\geq 0$$:

$$
\begin{eqnarray*} 
S(0) &=&\sum_{n=1}^\infty \dfrac{2^n }{\binom{2n}n} = 2+ \dfrac{\pi}2 \\
S(1) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n }{\binom{2n}n} = 3+ \pi \\
S(2) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n^2 }{\binom{2n}n} = 11+ \dfrac{7\pi}2 \\
S(3) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n^3 }{\binom{2n}n} = 55+ \dfrac{35\pi}2 \\
S(4) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n^4 }{\binom{2n}n} = 355 + 113\pi \approx \underline{709.9999}698 \ldots , \quad \text{So close to an integer? Coincidence?} \\
S(5) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n^5 }{\binom{2n}n} = 2807+ \dfrac{1787\pi}2 \\
S(6) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n^6 }{\binom{2n}n} = 26259+ \dfrac{16717\pi}2 \\
S(7) &=&\sum_{n=1}^\infty \dfrac{2^n \cdot n^7 }{\binom{2n}n} = 283623+ 90280\pi \\
\end{eqnarray*} 
$$ 

And for $$  m<0 $$  as well (all verified by WolframAlpha as well):

$$
\begin{eqnarray*} 
S(-1) &=&\sum_{n=1}^\infty \dfrac{2^n \frac 1 n}{\binom{2n}n} = \dfrac{\pi}2 \\
S(-2) &=&\sum_{n=1}^\infty \dfrac{2^n \frac 1 {n^2} }{\binom{2n}n} = \dfrac{\pi^2 }8 \\
S(-3) &=&\sum_{n=1}^\infty \dfrac{2^n \frac 1 {n^3} }{\binom{2n}n} = \pi G - \dfrac{35\zeta(3)}{16} + \dfrac18 \pi^2 \ln2, \quad  G \text{ denotes Catalan's constant} \\
\end{eqnarray*} 
$$ 

**So a natural question arise**: Is there a closed form for $$ S(m) $$  for all integers $$  m $$?


# Answer

We want for $$ m < 0$$  any positive integer :

$$
\tag{1}S_{-m}(x) \equiv
\sum_{n=1}^\infty \frac{(2x)^{2n}}{n^m\binom{2n}{n}}
$$

Let's start again [with][1] :

$$
\tag{2}S_{-2}(x)=2\,\arcsin(x)^2=\sum_{n=1}^\infty \frac{(2x)^{2n}}{n^2\binom{2n}{n}}
$$

Differentiation and multiplication by $$\dfrac x2$$  returns :

$$
\tag{3}S_{-1}(x)=\frac x2\,S_2'(x)=2x\,\frac{\arcsin(x)}{\sqrt{1-x^2}}=\sum_{n=1}^\infty \frac{(2x)^{2n}}{n\binom{2n}{n}}
$$

While multiplication of $$(1)$$ by $$\dfrac 2x$$  and integration gives us :

$$
\tag{4}S_{-3}(x)=\int_0^x \frac 4t\,\arcsin(t)^2\,dt=\sum_{n=1}^\infty \frac{(2x)^{2n}}{n^3\binom{2n}{n}}
$$

This integral may be expressed [using polylogarithms][2] but it will be more convenient to write it 
using (real) [Clausen functions][3] :

$$
\tag{5}\operatorname{Cl}_{2m-1}(x):=\sum_{n=1}^{\infty }\frac{\cos(n\,x)}{n^{2m-1}},\;\operatorname{Cl}_{2m}(x):=\sum_{n=1}^{\infty }\frac{\sin(n\,x)}{n^{2m}}
$$

These functions appear in the [Fourier series from jump discontinuities][4] 
(their [variants are Bernoulli polynomials][5]) and are obtained from successive integrations of 

$$
\;\displaystyle \operatorname{Cl}_1(x)=-\log\left(2\sin\frac x2\right)\;
$$ 

using 

$$
\tag{6}\displaystyle\operatorname{Cl}_{2m}(x)
=\int_0^x \operatorname{Cl}_{2m-1}(t)\,dt,\ \;\operatorname{Cl}_{2m+1}(x)=\zeta(2m+1)-\int_0^x 
\operatorname{Cl}_{2m}(t)\,dt
$$ 

Let's set $$\;t=\sin(u/2)\,$$ and integrate by parts $$\,\log(2\sin(u/2))\,$$ to get  : 

$$
\begin{equation*}
\begin{aligned}
S_{-3}(x)&=\int_0^x \frac 4t\,\arcsin(t)^2\,dt\\
&=4\int_0^{2\arcsin(x)} (u/2)^2\,\frac{\cos(u/2)}{2\,\sin(u/2)}\,du\\
&=\left.u^2\log(2\sin(u/2))\right|_0^{2\arcsin(x)}-\int_0^{2\arcsin(x)} 2\,u\log(2\,\sin(u/2))\,du
\end{aligned}
\end{equation*}
$$

This becomes 

$$
\quad\displaystyle S_{-3}(x)=\,-2\log(2x)\,\operatorname{Ls}_2^{(1)}(2\arcsin(x))+2\,\operatorname{Ls}_3^{(1)}(2\arcsin(x))\;
$$

using Leonard Lewin's notation $$(7.14)$$ for the *generalized log-sine integral* $$\;\operatorname{Ls}$$ :  
(Lewin $$ 1981$$  "Polylogaritms and associated functions" and [Kalmykov and Sheplyakov's $$ 2004 $$][6])

$$
\tag{7}\operatorname{Ls}_j^{(k)}(x)=-\int_0^x t^k\,\left(\log\left(2\sin\frac t2\right)\right)^{j-k-1}dt,\quad k\ge 0,\ j\ge k+1
$$  

What makes the rewriting of $$ S_{-3}$$ interesting is that it may be generalized to any $$\,S_{-m}\,$$ as shown 
by Borwein, Broadhurst and Kamnitzer $$ 2001$$  ["Central binomial sums, multiple Clausen values, and zeta 
values"][7]. The derivation is rather clever (little typo : $$\Gamma(n)$$ should be $$\Gamma(k)$$) and will be
 reproduced in details and slightly generalized as in Kalmykov and Veretin $$ 2000$$  :
 
The [gamma function](https://en.wikipedia.org/wiki/Gamma_function) is defined by 

$$
\;\displaystyle\Gamma(m):=
\int_0^\infty t^{m-1}e^{-t}\,dt=\int_0^\infty (nt)^{m-1}e^{-nt}\,d(nt),\;(n>0)
$$

The substitution $$\;t=-\log u\;$$ gives 

$$
\;\displaystyle\Gamma(m)=n^m\int_0^1 (-\log u)^{m-1}\,u^{n-1}\,du\;$ so that for $\;u:=y^2
$$  

as

$$
\begin{equation*}
\begin{aligned}
S_{-m}(x)&=\sum_{n=1}^\infty \frac{(2x)^{2n}}{\binom{2n}{n}\,n^m}\\
&=\sum_{n=1}^\infty \frac{(2x)^{2n}}{\binom{2n}{n}\,\Gamma(m)}\int_0 ^1 (-2\log y)^{m-1}y^{2n-2}\,d(y^2)\\
&= \frac{(-2)^{m-1}}{(m-1)!}\int_0^1 (\log y)^{m-1}\,\sum_{n=1}^\infty (2x)^{2n}\frac{2\,y^{2n-1}}{\binom{2n}{n}}\,dy\\
&= -\frac{(-2)^{m-1}}{(m-2)!}\int_0^1 \frac{(\log y)^{m-2}}{y}\,\sum_{n=1}^\infty \frac{(2xy)^{2n}}{n\,\binom{2n}{n}}\,dy,\quad\text{(by parts)}\\
&=-\frac{(-2)^{m-1}}{(m-2)!}\int_0^1 (\log y)^{m-2}\frac{(2x)\,\arcsin(xy)}{\sqrt{1-(xy)^2}}\,dy,\quad\text{(using}\,S_{-1}(xy)\,\\
&=-\frac{(-2)^{m-1}}{(m-2)!}\int_0^{2\arcsin x} \left(\log\left(\frac{1}{x}\sin\frac{t}{2}\right)\right)^{m-2}\frac{t}{2}\,dt,\quad \text{(setting} \, xy=\sin\frac{t}{2} \, \text{)}\\
\end{aligned}
\end{equation*}
$$

And 

$$
\begin{equation*}
\tag{8} S_{-m} (x) = \frac {1}{(m-2)!} \int_0 ^{2\arcsin{x}} \left[2 \log(2x)-2\log \left(2\sin{\frac{t}{2}} \right)\right]^{m-2} \,t\,dt
\end{equation*}
$$

$$
\begin{equation*}
\tag{9} S_{-m}(x) = - \sum_{j=0}^{m-2} \frac{(-2)^j}{(m-2-j)!j!} \,\left(2 \log(2x) \right )^{m-2-j} \, \operatorname{Ls}_{j+2}^{(1)} \left(2\arcsin{x} \right)
\end{equation*}
$$

Nan-Yue and Williams gave $$(8)$$ for $$ x=\dfrac 12$$  in $$ 1995$$ ["Values of the Riemann zeta function and integrals involving $$\log\left(2\sinh\frac{\theta}2\right)$$ and $$\log\left(2\sin\frac{\theta}2\right)$$"][8].   
The general identities $$(8)$$ and $$(9)$$ (with a link to BBK's paper) were given in :

 - Kalmykov and Veretin $$ 2000$$  ["Single scale diagrams and multiple binomial sums"][9] $$(8)$$ and 
 - Davydychev and Kalmykov $$ 2001$$  ["New results for the $$\epsilon$$-expansion of certain one-, two- and three-loop Feynman diagrams"][10].

The KV $$ 2000$$  paper contains too an additional intriguing formula 
using [Nielsen's generalized polylogarithm][11]  $$\,\displaystyle \operatorname{S}_{n,p}(z):=\frac {(-1)^{n+p-1}}{(n-1)!p!}\int_0^1 \log^{n-1}(t)\,\log^p(1-zt)\,\frac{dt}t\,$$ that I'll rewrite using $$\,\operatorname{S}_{m-2,1}(z)=\operatorname{Li}_{m-1}(z)\,$$ as :

$$
\tag{10}S_{-m}(x)=\int_0^1\operatorname{Li}_{m-1}\left((2x)^2\,s(1-s)\right)\,\frac {ds}s
$$

This formula is interesting too to evaluate $$\,S_{+m}(x)\,$$ ([rational functions][12] are integrated).  

Now that $$(9)$$ allows us to express $$\,S_{-m}(x)\,$$ as "generalized log-sine integrals" $$\operatorname{Ls}_m^{(1)}\,$$ what can we do with that?


$$\,\operatorname{Ls}_2^{(0)}(x)\,$$ is simply the "Clausen integral" $$\,\operatorname{Cl}_{2}(x)\,$$ 
while (from Lewin's book $$ 1981$$  "Polylogaritms and associated functions" p. $$ 200$$) $$\,\operatorname{Ls}_{n+2}^{(n)}(x)\,$$ may be written as a sum of Clausen functions :

$$
\begin{equation*}
\begin{aligned}
\frac{(-1)^m}{(2m-2)!}\int_0^x t^{2m-2}\log\left(2\sin\frac t2\right)dt
&=\operatorname{Cl}_{2m}(x)+\sum_{k=1}^{m-1}(-1)^{k}\left(\frac{x^{2k-1}}{(2k-1)!}
\operatorname{Cl}_{2m-2k+1}(x)+\frac{x^{2k}}{(2k)!}\operatorname{Cl}_{2m-2k}(x)\right)\\
\end{aligned}
\end{equation*}
$$

$$
\begin{equation*}
\begin{aligned}
\frac{(-1)^{m-1}}{(2m-1)!}\int_0^x t^{2m-1}\log\left(2\sin\frac t2\right)dt
&=\zeta(2m+1)+\sum_{k=0}^{m-1}(-1)^{k}\left(\frac{x^{2k}}{(2k)!}\operatorname{Cl}_{2m-2k+1}(x)+\frac{x^{2k+1}}{(2k+1)!}\operatorname{Cl}_{2m-2k}(x)\right)\\
\end{aligned}
\end{equation*}
$$

Concerning your specific choice of $$\,x=\dfrac 1{\sqrt{2}}\,$$ (so that $$\,\displaystyle 2\arcsin(x)=\frac{\pi}2\,$$ and $$\,2\log(2x)=\log(2)$$) some explicit results were given in DK $$ 2001$$  (appendix A) :

$$
\begin{equation*}
\begin{aligned}
\operatorname{Ls}_{4}^{(1)}\left(\frac{\pi}{2}\right) 
& =  -\tfrac{5}{96} \log^4(2)+ \tfrac{5}{16} \zeta(2) \log^2(2) - \tfrac{35}{32} \zeta(3) \log(2)
+ \tfrac{125}{32} \zeta(4) + \tfrac{1}{2} \pi \operatorname{Ls}_{3}\left(\tfrac{\pi}{2}\right)- \tfrac{5}{4} \operatorname{Li}_{4}\left(\tfrac{1}{2}\right)\\  
\end{aligned}
\end{equation*}
$$

$$
\begin{equation*}
\begin{aligned}
\operatorname{Ls}_{5}^{(1)}\left(\frac{\pi}{2}\right) & =  -\tfrac{1}{16} \log^5(2)
+ \tfrac{5}{16} \zeta(2) \log^3(2)- \tfrac{105}{128} \zeta(3) \log^2(2)
- \tfrac{15}{8} \operatorname{Li}_{4}\left(\tfrac{1}{2}\right) \log(2) - \tfrac{9}{8} \zeta(2) \zeta(3)
\nonumber \\
&\quad + \tfrac{1}{2} \pi \operatorname{Ls}_{4}\left(\tfrac{\pi}{2}\right)
- \tfrac{1209}{256} \zeta(5)
- \tfrac{15}{8} \operatorname{Li}_{5}\left(\tfrac{1}{2}\right)
\end{aligned}
\end{equation*}
$$

In Davydychev and Kalmykov $$ 2004$$  ["Massive Feynman diagrams and inverse binomial sums"][13] one 
finds some general results ($$\,z$$  is our $$(2x)^2\,$$) :

For 

$$
\displaystyle\theta:=2\,\arcsin\left(\frac{\sqrt{z}}2\right),\ l_{\theta}:=\log\left(2\sin\frac{\theta}{2}\right)
$$

 we have :

$$
\begin{equation*}
\begin{aligned}
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n}  
&=  \theta\,\tan\frac{\theta}{2}&\\
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n^2} 
&=\frac{1}{2}\,\theta^2 &\\
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n^4} 
&= - 2 \operatorname{Ls}_{4}^{(1)}(\theta)+ 4 l_{\theta}
\left[\operatorname{Cl}_3(\theta) + \theta \operatorname{Cl}_2(\theta) - \zeta(3) \right] 
+\theta^2 l_{\theta}^2 &\\
\end{aligned}
\end{equation*}
$$

For the conformal variable 

$$
\displaystyle y:=\frac{\sqrt{z-4}-\sqrt{z}}{\sqrt{z-4}+\sqrt{z}}
$$ 

we have :

$$
\begin{equation*}
\begin{aligned}
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n}  & = 
\frac{1-y}{1+y}\,\log(y)\\
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n^2} & = -\frac{1}{2}\,\log^2(y)\\
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n^3} & = 
2 \operatorname{Li}_3(y) - 2\,\log(y)\,\operatorname{Li}_{2}(y) - \log^2(y)\, \log(1-y) 
+ \frac{1}{6}\,\log^3(y)- 2 \zeta(3) \\
\sum_{n=1}^\infty \frac{1}{\left( 2n \atop n\right) } \frac{z^n}{n^4} & =  
  4 \operatorname{S}_{2,2}(y)
- 4 \operatorname{Li}_{4}(y) - 4 \operatorname{S}_{1,2}(y) \log(y) 
+ 4 \operatorname{Li}_{3}(y) \log(1-y) \\
&+ 2 \operatorname{Li}_3(y) \log(y) - 4 \operatorname{Li}_{2}(y) \log(y) \log(1-y) - \log^2(y) \log^2(1-y) 
\\
&+ \frac{1}{3} \log^3(y)\log(1-y) - \frac{1}{24} \log^4(y) 
- 4 \log(1-y)  \zeta(3) + 2 \log(y) \zeta(3)+ 3 \zeta(4)
\end{aligned}
\end{equation*}
$$

  [1]: https://math.stackexchange.com/questions/383068
  [2]: http://www.wolframalpha.com/input/?i=int(4%2Fx*arcsin(x)%5E2,x)
  [3]: http://mathworld.wolfram.com/ClausenFunction.html
  [4]: https://math.stackexchange.com/a/121376/21783
  [5]: https://math.stackexchange.com/a/1210687/21783
  [6]: http://arxiv.org/abs/hep-ph/0411100
  [7]: https://arxiv.org/abs/hep-th/0004153
  [8]: http://msp.org/pjm/1995/168-2/pjm-v168-n2-p04-p.pdf
  [9]: http://arxiv.org/abs/hep-th/0004010
  [10]: http://arxiv.org/abs/hep-th/0012189
  [11]: http://cds.cern.ch/record/147790
  [12]: https://en.wikipedia.org/wiki/Polylogarithm#Particular_values
  [13]: http://arXiv.org/abs/hep-th/0303162