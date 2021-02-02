---
layout: post
title: integral related to hypergeometric function 4
tags:
  - integration   
  - definite-integrals
  - closed-form
  - hypergeometric-function
  - real-analysis
  - gamma-function
  
description:  
  integral related to hypergeometric function 4
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :

 
 $$ 

\sum_{n=1}^\infty\frac{\Gamma\left(n+\frac{1}{2}\right)}{(2n+1)^4\,4^n\,n!}
 
 $$ 



<!–-break-–>


# Answer

First, in view of Legrende's duplication formula, 

 $$ 
S=\sum_{n=1}^\infty\frac{\Gamma\left(n+\frac{1}{2}\right)}{(2n+1)^4\,4^n\,n!}=2\sqrt{\pi}\sum_{n=1}^\infty\frac{\Gamma(2n)}{\Gamma(n)\,n!\,(2n+1)^4\, 16^n}
\\=-\frac{\sqrt{\pi}}{3}\int_0^1 \ln^3(x)\sum_{n=1}^{\infty}\frac{\Gamma(2n)}{\Gamma(n)\,n!}\left(\frac{x^2}{16}\right)^ndx\\
=-\sqrt{\pi}-\frac{\sqrt{\pi}}{6}\int_0^1\frac{\ln^3(x)}{\sqrt{1-x^2/4}}dx=-\sqrt{\pi}-\frac{\sqrt{\pi}}{3}\int_0^{\frac{\pi}{6}}\ln^3(2\sin x)dx
 $$ 


Claim: for $$0<a\leq \frac{\pi}{2}$$,
 
 $$ 
\int_0^a \ln^3\left(\frac{\sin x}{\sin a}\right)dx\tag{0}=\frac{4a-3\pi}{2}a^2\ln(2\sin a)-\frac{3\pi}{4}\zeta(3)+3\left(\frac{\pi}{2}-a\right)\Re\left(\frac12 \operatorname{Li}_3(e^{2ia})+\operatorname{Li}_3(1-e^{2ia})\right)+3\Im\left(\frac14\operatorname{Li}_4(e^{2ia})+\operatorname{Li}_4(1-e^{2ia})\right)

 $$ 


Proof.
The idea is exactly identical to the proof displayed in [this question](https://math.stackexchange.com/questions/1438381/closed-form-of-int-01-frac-ln2x-sqrtxa-bx-dx). The proof is rather tedious (and obviously inefficient), and ends with a somewhat of a cancellation (implying the existence of a shortcut) , so I omit the boring algebra and outline the main ideas, which can be repeated systematically to obtain closed forms for even higher powers of logsine.

things to know: 

 $$ 
\ln(2\sin x)=\ln(1-e^{2ix})+i\left(\frac{\pi}{2}-x\right) \tag{1}
 $$ 


 $$ 
\small\int\frac{\ln^3(1-x)}{x}dx=\ln^3(1-x)\ln(x)+3\ln^2(1-x)\text{Li}_2(1-x)-6\ln(1-x)\text{Li}_3(1-x)+6\text{Li}_4(1-x) \tag{2}
 $$ 


 $$ 
\int_0^a x\ln(2\sin x)dx=-\frac{a}{2}\text{Cl}_2(2a)-\frac14\Re\text{Li}_3(e^{2ia})+\frac{\zeta(3)}{4}\tag{3}
 $$ 


 $$ 
\int_0^a x^2\ln(2\sin x)dx=-\frac{a^2}{2}\text{Cl}_2(2a)-\frac{a}{2}\Re\text{Li}_3(e^{2ia})+\frac14\Im\text{Li}_4(e^{2ia})\tag{4}
 $$ 


 $$ 
\int_0^a \ln(\sin x)dx=-a\ln2-\frac12 \text{Cl}_2(2a)\tag{5}
 $$ 


 $$ 
\int_0^a \ln^2(\sin x)dx=\frac{a^3}{3}+a\ln^2 2-a\ln^2(2\sin a)-\ln(\sin a)\text{Cl}_2(2a)-\Im\text{Li}_3(1-e^{2ia})\tag{6}
 $$ 



$$(1)$$ is trivial, $$(2)$$ is not too hard to find, $$(5)$$ and $$(6)$$ are shown in the linked answer, and $$(3)$$&$$(4)$$ are easily found using $$\,\,\ln(2\sin x)=-\sum_{n\geq1}\frac{\cos(2xn)}{n}$$.
 
It is obvious that since we have $$(5)$$ and $$(6)$$, the claim $$(0)$$ depends on a closed form for $$\displaystyle\int_0^a \ln^3(\sin x)dx$$, and the latter may be evaluated in terms of $$\displaystyle\int_0^a \ln^3(2\sin x)dx$$.

But, with the help of $$(1)$$, 

 $$ 
\int_0^a \ln^3(2\sin x)dx=\Re\int_0^a \ln^3(1-e^{2ix})dx+3\int_0^a \ln(2\sin x)\left(\frac{\pi}{2}-x\right)^2dx\\
=\frac12\Im\int_1^{e^{2ia}}\frac{\ln^3(1-x)}{x} dx+3\int_0^a \ln(2\sin x)\left(\frac{\pi}{2}-x\right)^2dx
 $$ 


(Same idea @RandomVariable had in [this answer](https://math.stackexchange.com/questions/917154/looking-for-closed-forms-of-int-0-pi-4-ln2-sin-x-dx-and-int-0-pi-4?lq=1).)

Now we employ $$(2),(3),(4),$$ and $$(5)$$. Some expressions cancel and claim follows.$$\square $$ 

This result, together with the fact that $$e^{i\pi/3}$$ and $$1-e^{i\pi/3}$$ are conjugates, yields $$\displaystyle \int_0^{\frac{\pi}{6}} \ln^3(2\sin x)dx=-\frac{\pi}{4}\zeta(3)-\frac94\Im\text{Li}_4(e^{i\pi/3})$$,
and

 $$ 
S=\sqrt{\pi}\left(\frac{\pi}{12}\zeta(3)+\frac{9}{12}\Im\text{Li}_4(e^{i\pi/3})-1\right)
 $$ 



This form is equivalent to @user153012's form, as 

 $$ 
\frac{2}{\sqrt{3}}\Im\text{Li}_4(e^{i\pi/3})=\sum_{n\geq 0}\frac{(-1)^n}{(3n+1)^4}+\sum_{n\geq 0}\frac{(-1)^n}{(3n+2)^4} \\=\frac{\psi^{(3)}\left(\frac13\right)}{216}-\frac{\pi^4}{81}
 $$ 


---

Also, as noted in the comments in the linked question, this may be used to write a closed form for a certain hypergeometric function.

---

This serves as a generalisation for the series, because $$\displaystyle \sum_{n=1}^{\infty} \frac{\Gamma(n+1/2)}{(2n+1)^4 n!}a^{2n}=-\sqrt{\pi}\left(1+\frac1{6a}\int_0^{\sin^{-1} a}\ln^3\left(\frac{\sin x}{a}\right)dx\right)$$ 

As an example, using closed forms for trilogarithms displayed in [this post](https://math.stackexchange.com/questions/932932/known-exact-values-of-the-operatornameli-3-function?rq=1), we have

 $$ 
\int_0^{\frac{\pi}{4}}\ln^3(\sqrt{2}\sin x)dx=-\frac{\pi^3}{128}\ln2-\frac{3\pi}{8}\zeta(3)+\frac34\beta(4)+3\Im\text{Li}_4(1-i)
 $$ 


where $$\beta(4)=\Im\text{Li}_4(i)$$ is a value of Dirichlet's beta function.

Or equivalently, 

 $$ 
\sum_{n=1}^{\infty} \frac{\Gamma\left(n+\frac12\right)}{(2n+1)^4\,2^n\,n!}=-\sqrt{\pi}-\frac{\sqrt{2\pi}}{6}\left(-\frac{\pi^3}{128}\ln2-\frac{3\pi}{8}\zeta(3)+\frac34\beta(4)+3\Im\text{Li}_4(1-i)\right)
 $$ 
