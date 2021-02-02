---
layout: post
title: Lebesgue integral basics
tag:
 - real-analysis
 - integration
 - probability-theory
 - lebesgue-integral

description: Lebesgue integral basics

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Lebesgue integral basics

<!–-break-–>


we are  having trouble finding a good explanation of the Lebesgue integral. As per the definition, it is the expectation of a random variable. Then how does it model the area under the curve? Let's take for example a function $$f(x) = x^2$$.  How do we find the integral of $$f(x)$$ under $$[0,1]$$ using the Lebesgue integral?


# Answer 


As has been noted, the usual definition of the Lebesgue integral has little to do with probability or random variables (though the notions of measure theory and the integral can then be applied to the setting of probability, where under suitable interpretations it will turn out that the (Lebesgue) integral of (a certain) functions corresponds to the expectation of (a certain) random variable).
But this is not the origin of the Lebesgue integral. Here is an intuitive idea of what the Lebesgue integral is, as compared to the Riemann integral.
Recall from Calculus the idea behind the Riemann integral: the integral $$\int_a^b f(x)\,dx$$ is meant to represent the net signed area between the $$x$$-axis, the graph of $$y=f(x)$$, and the lines $$x=a$$ and $$x=b$$. The way we attempt to do this is by breaking up the domain, $$[a,b]$$, into subintervals $$[a=x_0,x_1]$$, $$[x_1,x_2],\ldots,[x_{n-1},x_n=b]$$. Then, on each subinterval $$[x_i,x_{i+1}]$$ we pick a point $$x_i^*$$, and we estimate the area under the graph of the function with the rectangle of height $$f(x_i^*)$$ and base $$[x_i,x_{i+1}]$$. This leads to the Riemann sums


$$

 \sum_{i=0}^{n-1} f(x_i^*)(x_{i+1}-x_i)

$$


as estimates of the area under the graph. We then consider finer and finer partitions of $$[a,b]$$ and take limits to estimate the area.
Lebesgue's idea was that instead of partitioning the domain, we will partition the range; if the function takes values between $$c$$ and $$d$$, we can divide the range $$[c,d]$$ into subintervals $$[c=y_0,y_1]$$, $$[y_1,y_2],\ldots,[y_{m-1},y_m=d]$$. Then, we let $$E_i$$ be the set of all points in $$[a,b]$$ whose value under $$f$$ lies between $$y_i$$ and $$y_{i+1}$$. That is,


$$

 E_i = f^{-1}([y_i,y_{i+1}]) = \{ x\in[a,b]\,|\, y_i \leq f(x) \leq y_{i+1}\}.

$$


If we have a way of assigning a "size" to $$E_i$$, call it its "measure" $$\mu(E_i)$$, then the portion of the graph of $$y=f(x)$$ that lies between the horizontal lines $$y=y_i$$ and $$y=y_{i+1}$$ will be $$A$$, where,


$$

 y_i\mu(E_i) \leq A \leq y_{i+1}\mu(E_i).

$$


So Lebesgue suggests to approximate the the area by picking a number $$y_i^*$$ between $$y_i$$ and $$y_{i+1}$$, and considering the sums


$$

 \sum_{i=0}^{n-1} \mu(E_i)y_i^*.

$$


Then consider finer and finer partitions of $$[c,d]$$, and this gives finer and finer approximations of of the area by these sums. The Lebesgue integral will be the limit of these sums. (The analogy given by Mike Spivey is very apt for the distinction between partitioning the domain and partitioning the range to find the sum.)
But in order for this to make sense, we need to develop a way of measuring fairly intricate subsets of the line, so that we can compute $$\mu(E_i)$$. So we first develop a way of doing this; turns out that if you accept the Axiom of Choice, then it is impossible to come up with a way of measuring that will 

(i) assign to an interval $$[a,b]$$ the "measure" $$b-a$$; 

(ii) will be invariant under translation, so so that if 

$$F=E+c = \{e+c | e\in E\}$$ 

then $$\mu(F)=\mu(E)$$; 

(iii) will be countably additive: if $$E = \cup_{i=1}^{\infty}E_i$$ and the $$E_i$$ are pairwise disjoint, 

then $$\mu(E) = \sum\mu(E_i)$$; and (iv) every subset of the line will have a well-defined (possibly infinite) measure. (If you don't accept the Axiom of Choice, then there are models of the reals where we can achieve this). So one drops the restriction (iv), and constructs a measure for which some sets will be "too weird" to have a measure. We then restrict attention to certain kinds of functions (called the measurable functions), which are the ones for which the sets we get in the process described above are all measurable sets. And then we define the Lebesgue integral for those functions, following the idea described above (but one does not define it exactly that way; instead the usual way is to describe $$f$$ as a limit of functions for which the integral is easy, and then compute the integral of $$f$$ as a limit of the integrals that are easy).
For your function, $$f(x)=x^2$$, this is fairly easy: the value all lie between $$0$$ and $$1$$, so say that we break up the range into subintervals of length $$1/n$$, so $$y_i = i/n$$, $$i=0,\ldots,n$$. Then 


$$

f^{-1}([y_i,y_{i+1}]) = f^{-1}([i/n, (i+1)/n]) = [\sqrt{i/n},\sqrt{(i+1)/n}],

$$


so the $$n$$th estimate, picking $$y_i^* = y_i = i/n$$ is just


$$

\sum_{i=0}^n (i/n)\left(\sqrt{(i+1)/n} - \sqrt{i/n}\right).

$$


Take the limit as $$n\to\infty$$, and you will get that the limit is $$\frac{1}{3}$$, as expected. (we will spare you the details; see the end of this answer for a high-power way of getting the answer similar to the way you do it with the Riemann integral).
It turns out that not every function is Lebesgue-integrable, just like not every function is Riemann-integrable. But every function that is Riemann-integrable will also be Lebesgue integrable, and the value of its Lebesgue integral will be the same as the value of its Riemann integral. But there are functions that are not Riemann-integrable but are Lebesgue-integrable (for example, the characteristic function of the rationals is Lebesgue-integrable, with integral $$0$$ over any interval, but is not Riemann-integrable). We also have a "Fundamental Theorem of Calculus" for the Lebesgue Integral:
Theorem. If $$F$$ is a differentiable function, and the derivative $$F'$$ is bounded on the interval $$[a,b]$$, then $$F'$$ is Lebesgue integrable on $$[a,b]$$ and


$$

\int_a^x F'\,d\mu = F(x) - F(a).

$$



Here, the integral is the Lebesgue integral. 
In particular, to finally answer the question you ask about your example, since $$F(x)=\frac{x^3}{3}$$ is a differentiable function whose derivative is bounded over any finite interval, in particular over $$[0,1]$$, then from this theorem you can deduce that the integral over the interval $$[0,1]$$ of the derivative $$F'(x)=x^2$$ is equal to $$F(1)-F(0)$$; that is,


$$

\int_0^1 x^2\,d\mu = \int_0^1 \left(\frac{x^3}{3}\right)'\,d\mu = \frac{1}{3} - \frac{0}{3} =\frac{1}{3}.

$$


we recommend the book A Garden of Integrals by Frank E. Burk (Dolciani Mathematical Expositions 31, MAA, 2007, ISBN 9-780883-853375); it discusses and compares the Cauchy integral, the Riemann integral, the Riemann-Stieltjes integral, the Lebesgue integral, the Lebesgue-Stieltjes integral, and the Henstock-Kurzweil integral; it also discusses the Wiener and Feynman integral. we just finished reading it recently.

