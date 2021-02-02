---
layout: post
title: Problem related to real analysis and harmonic numbers
tag:
 - real-analysis
 - sequences-and-series
 - closed-form
 - zeta-functions
 - harmonic-numbers

description: Problem related to real analysis and harmonic numbers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Infinite Series $$\sum_{n=1}^\infty\frac{H_n}{n^22^n}$$

<!–-break-–>


How can we prove that 


$$

\sum_{n=1}^{\infty}\frac{H_n}{n^2 2^n}=\zeta(3)-\frac{1}{2}\log(2)\zeta(2).
$$


# Answer 


Let's start with the product of $$\;-\ln(1-x)\,$$ and $$\dfrac 1{1-x}$$ to get the product generating function
(for 
$$|x|<1$$) :


$$

\tag{1}f(x):=-\frac {\ln(1-x)}{1-x}=\sum_{n=1}^\infty H_n\, x^n

$$


Dividing by $$x$$ and integrating we get :



$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_n}n\, x^n&=\int \frac{f(x)}xdx\\
&=-\int \frac{\ln(1-x)}{1-x}dx-\int\frac{\ln(1-x)}xdx\\
\tag{2}&=C+\frac 12\ln(1-x)^2+\operatorname{Li}_2(x)\\
\end{align*}

$$

(with $$C=0$$ from $$x=0$$)
The first integral was obtained by integration by parts, the second from the integral definition of the dilogarithm or the recurrence for the polylogarihm (with $$\;\operatorname{Li}_1(x)=-\ln(1-x)$$) : 

$$

\tag{3}\operatorname{Li}_{s+1}(x)=\int\frac {\operatorname{Li}_{s}(x)}x dx

$$


Dividing $$(2)$$ by $$x$$ and integrating again returns (using $$(3)$$ again) :



$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_n}{n^2}\, x^n&=\int \frac {\ln(1-x)^2}{2\,x}dx+\int \frac{\operatorname{Li}_2(x)}x dx\\
&=C+I(x)+\operatorname{Li}_3(x)\\
\end{align*}


$$

with $$I(x)$$ obtained by integration by parts (since $$\frac d{dx}\operatorname{Li}_2(1-x)=\dfrac {\ln(x)}{1-x}$$) :



$$
\begin{align*}
I(x)&:=\int \frac {\ln(1-x)^2}{2\,x}dx\\
&=\left.\frac{\ln(1-x)^2\ln(x)}{2}\right|+\int \ln(1-x)\frac {\ln(x)}{1-x}dx\\
&=\left.\frac{\ln(1-x)^2\ln(x)}{2}+\ln(1-x)\operatorname{Li}_2(1-x)\right|+\int \frac{\operatorname{Li}_2(1-x)}{1-x}dx\\
&=\left.\frac{\ln(1-x)^2\ln(x)}{2}+\ln(1-x)\operatorname{Li}_2(1-x)-\operatorname{Li}_3(1-x)\right|\\
\end{align*}
$$



getting the general relation :


$$

\tag{4}\sum_{n=1}^\infty \frac{H_n}{n^2}\, x^n=C+\frac{\ln(1-x)^2\ln(x)}{2}+\ln(1-x)\operatorname{Li}_2(1-x)+\operatorname{Li}_3(x)-\operatorname{Li}_3(1-x)

$$


(with $$C=\operatorname{Li}_3(1)=\zeta(3)$$ here)
applied to $$x=\dfrac 12$$ with $$\operatorname{Li}_2\left(\frac 12\right)=\dfrac{\zeta(2)-\ln(2)^2}2$$ from the link returns the wished :



$$
\begin{align*}
\sum_{n=1}^\infty \frac{H_n}{n^2\;2^n}&=\zeta(3)-\frac{\ln(2)^3}2-\ln(2)\frac{\zeta(2)-\ln(2)^2}2\\
\tag{5}\sum_{n=1}^\infty \frac{H_n}{n^2\;2^n}&=\zeta(3)-\ln(2)\frac{\zeta(2)}2
\end{align*}


$$

