---
layout: post
title: Closed form integral 1
tags:
  - integration   
  - definite-integrals
  - closed-form
  - polylogarithm
description:  
  Closed form integral 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Prove that

$$
 \int\limits_0^1 [\log(x)\log(1-x)+\operatorname{Li}_2(x)]\left[\frac{\operatorname{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}\right]\mathrm dx
$$

<!–-break-–>

$$\mathfrak{I}=\int\limits_0^1 \left[\log(x)\log(1-x)+\operatorname{Li}_2(x)\right]\left[\frac{\operatorname{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}\right]\mathrm dx=4\zeta(2)\zeta(3)-9\zeta(5)\tag1$$

This integral haunts me for while and I am still unable to evaluate it which annoys me even more. For the first time I have encountered it within [*Mathematical Analysis - A collection of Problems* by Tolaso J. Kos](https://www.tolaso.com.gr/documents/A%20collection%20of%20problems%20in%20Analysis.pdf) (Page $$27$$, Problem $$282$$) and I am still stumped by this one.

However, today I am have come across [this question](https://math.stackexchange.com/questions/290250/show-that-int-0-pi-2-frac-log2-sin-x-log2-cos-x-cos-x-sin-x-mathrm) asking for the evaluation of the integral

$$\mathfrak{J}=\int\limits_0^{\pi/2}\frac{\log^2(\sin x)\log^2(\cos x)}{\sin x\cos x}\mathrm dx=\frac12\zeta(5)-\frac14\zeta(2)\zeta(3)\tag2$$

Which can done be *"rather simple"* by invoking the fourth derivative of the Beta Function. I was baffled as I recognized the structure of the final value; moreover reminding me of the logarithmic integral $$(1)$$ I was not able to evaluate. It might turn out that this *relation* is by pure chance but nevertheless it motivated me to look at $$(1)$$ again. It is hardly probable that $$(1)$$ can be done in a similiar way like $$(2)$$ in [*xpaul*'s answer](https://math.stackexchange.com/q/925106) to the linked question due the involved Dilogarithms but anyway you can prove me wrong.

I have not got that far with $$(1)$$ but however I noticed two, I would say quite interesting, facts about the integral. First of all consider the following, well-known functional relation of the Dilogarithm 

$$\operatorname{Li}_2(x)+\operatorname{Li}_2(1-x)=\zeta(2)-\log(x)\log(1-x)$$

which can be used in order to get rid of the $$\log(x)\log(1-x)$$-term within $$(1)$$ and leading to

$$\small\int\limits_0^1 \left[\log(x)\log(1-x)+\operatorname{Li}_2(x)\right]\left[\frac{\operatorname{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}\right]\mathrm dx=\int\limits_0^1 \left[\zeta(2)-\operatorname{Li}_2(1-x)\right]\left[\frac{\operatorname{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}\right]\mathrm dx$$

Secondly applying the subsititution $$x=1-x$$ after a minor reshape yields to

$$
\begin{equation*}
\begin{aligned}
\int\limits_0^1 \left[\zeta(2)-\operatorname{Li}_2(1-x)\right]\left[\frac{\operatorname{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}\right]\mathrm dx&=\int\limits_0^1 \left[\frac{\zeta(2)}{1-x}-\frac{\operatorname{Li}_2(1-x)}{1-x}\right]\left[\frac{\operatorname{Li}_2(x)}x-\zeta(2)\right]\mathrm dx\\
&=\int\limits_0^1 \left[\zeta(2)-\operatorname{Li}_2(1-x)\right]\left[\frac{\operatorname{Li}_2(x)}x-\zeta(2)\right]\frac{\mathrm dx}{1-x}\\
&=\int\limits_0^1 \left[\zeta(2)-\operatorname{Li}_2(x)\right]\left[\frac{\operatorname{Li}_2(1-x)}{1-x}-\zeta(2)\right]\frac{\mathrm dx}x\\
&=\int\limits_0^1 \left[\frac{\zeta(2)}x-\frac{\operatorname{Li}_2(x)}x\right]\left[\frac{\operatorname{Li}_2(1-x)}{1-x}-\zeta(2)\right]\mathrm dx
\end{aligned}
\end{equation*}
$$

I want to point out the quite interesting one could say "almost"-symmetry of the two integrals

>$$\begin{align}
\mathfrak{I}_1&=\int\limits_0^1 \left[\frac{\zeta(2)}{1-x}-\frac{\operatorname{Li}_2(1-x)}{1-x}\right]\left[\frac{\operatorname{Li}_2(x)}x-\zeta(2)\right]\mathrm dx\\
\mathfrak{I}_2&=\int\limits_0^1 \left[\frac{\zeta(2)}x-\frac{\operatorname{Li}_2(x)}x\right]\left[\frac{\operatorname{Li}_2(1-x)}{1-x}-\zeta(2)\right]\mathrm dx
\end{align}$$

which might be helpful for the actual evaluation. But from hereon I have no clue how to continue. 

Just multplying the two brackets out  does not seem like a good idea to me hence one the one hand it is not elegant 
at all and on the other hand it would lead to to the term $$\operatorname{Li}_2(x)\operatorname{Li}_2(1-x)$$ for which
 I have no idea how to deal with concerning the fact that I am not used to e.g. double series and their evaluation.
 I also tried various ways of Integration by Parts but this seems to be pointless since all variations ended up in 
 producing a divergent term unless I have missed a sepcial choice of $$u$$ and $$\mathrm v$$. I have not figured out 
 a suitable substitution nor an appropriate newly introduced parameter (for the application of Feynman's Trick) 
 and the I do not know whether a series expansion would be helpful or not (connected with this issue is the 
 possibility of a double summation with which I cannot really deal).

Thus, I am asking for the closed-form evaluation of $$(1)$$ hopefully equal to the given value (which works out
 numerically according to WolframAlpha). Even though I have troubles with double series I would accept an answer 
 invoking these notwithstanding that I would appreciate a solution without involving them. Hence this integral 
 appeared within a collocation of Analysis Probelms I am rather sure that it has been already evaluated somewhere
 (maybe even here on MSE where I was not able to find it).


# Answer

Cross-posting this integral on AoPS brings Y. Sharifi's solution [here][1] after a day. Quite amazing one!

I will copy here his entire solution:
 Let $$I$$ be your integral. Using the identity 
 
 $$\ln x \ln(1-x)+\text{Li}_2(x)=\zeta(2)-\text{Li}_2(1-x),$$ 
 
we have

$$I=-\int_0^1 \frac{\text{Li}_2(x)\text{Li}_2(1-x)}{x(1-x)} \ dx + \zeta(2)\int_0^1 \left(\frac{\text{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}+\frac{\text{Li}_2(1-x)}{1-x}\right)dx.$$

Let 

$$J=\int_0^1 \frac{\text{Li}_2(x)\text{Li}_2(1-x)}{x(1-x)} \ dx, \ \ \ \ \ K:=\int_0^1 \left(\frac{\text{Li}_2(x)}{x(1-x)}-\frac{\zeta(2)}{1-x}+\frac{\text{Li}_2(1-x)}{1-x}\right)dx.$$ 

So 
$$I=\zeta(2)K - J. \ \ \ \ \ \ \ \ \ (1)$$

We first show that $$K=0.$$ Start with using integration by parts in $$K,$$ with 
$$u=\frac{\text{Li}_2(x)}{x}-\zeta(2)+\text{Li}_2(1-x)$$ and $$dv=\frac{dx}{1-x}.$$ Then 

$$K=\int_0^1 \ln(1-x)\left(\frac{\ln x}{1-x}-\frac{\ln(1-x)}{x^2}-\frac{\text{Li}_2(x)}{x^2}\right)dx. \ \ \ \ \ \ \ \ \ \ (2)$$

Using the Maclaurin series of $$\ln(1-x),$$ we quickly find the first integral in $$K$$  

$$\int_0^1 \frac{\ln x \ln(1-x)}{1-x} \ dx = \int_0^1 \frac{\ln x \ln(1-x)}{x} \ dx=\zeta(3). \ \ \ \ \ \ \ \ \ \ (3)$$

Next, we ignore the second integral in $$K$$ for now and we look at the third one, i.e. $$\int_0^1 \frac{\ln(1-x) \text{Li}_2(x)}{x^2} \ dx.$$ In this integral, we use integration by parts with $$u=\ln(1-x)\text{Li}_2(x)$$ and $$dv=\frac{dx}{x^2};$$ 
notice that we need to choose $$v=1-\frac{1}{x}.$$ So 

$$\int_0^1 \frac{\ln(1-x) \text{Li}_2(x)}{x^2} \ dx=\int_0^1\left(1-\frac{1}{x}\right)\left(\frac{\text{Li}_2(x)}{1-x}+\frac{\ln^2(1-x)}{x}\right) dx$$

$$=-\int_0^1 \frac{\text{Li}_2(x)}{x} \ dx + \int_0^1 \frac{\ln^2(1-x)}{x} \ dx - \int_0^1 \frac{\ln^2(1-x)}{x^2} \ dx=-\zeta(3)+\int_0^1 \frac{\ln^2x}{1-x} \ dx -\int_0^1 \frac{\ln^2(1-x)}{x^2} \ dx.$$

$$=\zeta(3)-\int_0^1 \frac{\ln^2(1-x)}{x^2} \ dx. \ \ \ \ \ \ \ \ \ (4)$$

Thus, by $$(2),(3)$$ and $$(4),$$ we have $$K=0$$ and hence, by $$(1),$$ 

$$I=-J=-\int_0^1 \frac{\text{Li}_2(x)\text{Li}_2(1-x)}{x(1-x)} \ dx=-2\int_0^1 \frac{\text{Li}_2(x)\text{Li}_2(1-x)}{x} \ dx.$$

So integration by parts with $$u=\text{Li}_2(1-x)$$ and $$dv=\frac{\text{Li}_2(x)}{x} \ dx$$ gives 

$$I=2\int_0^1 \frac{\text{Li}_3(x)\ln x}{1-x} \ dx=2\int_0^1 \text{Li}_3(x) \ln x \sum_{m \ge 1}x^{m-1} dx=2\sum_{m \ge 1} \int_0^1 x^{m-1}\text{Li}_3(x) \ln x \ dx$$

$$=2\sum_{m \ge 1} \int_0^1x^{m-1}\sum_{n \ge 1} \frac{x^n}{n^3} \ln x \ dx=2\sum_{m,n \ge 1} \frac{1}{n^3}\int_0^1x^{n+m-1}\ln x \ dx=-2\sum_{m,n \ge 1} \frac{1}{n^3(n+m)^2}$$

$$=-\sum_{m,n \ge 1} \left(\frac{1}{n^3(n+m)^2}+\frac{1}{m^3(n+m)^2}\right). \ \ \ \ \ \ \ \ \ (5)$$

So $$(5)$$ and the following identity 

$$\frac{1}{n^3(n+m)^2}+\frac{1}{m^3(n+m)^2}=\frac{1}{n^3m^2}-\frac{2}{n^2m^3}+\frac{3}{m^3n(n+m)}$$

together give

$$I=-\sum_{m,n \ge 1}\left(\frac{1}{n^3m^2}-\frac{2}{n^2m^3}+\frac{3}{m^3n(n+m)}\right)=\zeta(2)\zeta(3)-3\sum_{m,n \ge 1} \frac{1}{m^3n(n+m)}$$

$$=\zeta(2)\zeta(3)-3\sum_{m \ge 1} \frac{1}{m^4} \sum_{n \ge 1}\left(\frac{1}{n}-\frac{1}{n+m}\right)=\zeta(2)\zeta(3)-3\sum_{m \ge 1} \frac{H_m}{m^4}, \ \ \ \ \ \ \ \ \ (6)$$

where, as usual, $$H_m:=\sum_{j=1}^m \frac{1}{j}$$ is the $$m$$-th harmonic number. Now we use Euler's formula

$$\sum_{m \ge 1} \frac{H_m}{m^k}=\left(1+\frac{k}{2}\right)\zeta(k+1)-\frac{1}{2}\sum_{i=1}^{k-2}\zeta(i+1)\zeta(k-i), \ \ \ \ k \ge 2,$$
with $$k=4$$ to get

$$\sum_{m \ge 1} \frac{H_m}{m^4}=3\zeta(5)-\zeta(2)\zeta(3)$$
and so, by $$(6),$$

$$I=\zeta(2)\zeta(3)-3(3\zeta(5)-\zeta(2)\zeta(3))=4\zeta(2)\zeta(3)-9\zeta(5).$$

[1]:http://artofproblemsolving.com/community/c7h1776009p11685703

[3]:http://www.ssmrmh.ro/wp-content/uploads/2017/08/6-RMM-AUTUMN-EDITION-2017-SOLUTIONS-compressed.pdf
[4]:http://www.ssmrmh.ro/