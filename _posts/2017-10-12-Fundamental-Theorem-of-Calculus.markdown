---
layout: post
title: Fundamental Theorem of Calculus
tag:
 - real-analysis
 - soft-question

description: Fundamental Theorem of Calculus

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Fundamental Theorem of Calculus

<!–-break-–>


The Fundamental Theorem of Calculus says the following:

Theorem. If $$f$$ is the derivative of $$F$$ at every point on $$[a,b]$$, then under suitable hypotheses we have that 

$$

\int_{a}^{b} f(t) \ dt = F(b)-F(a)

$$


Theorem. If $$f$$ is integrable on $$[a,b]$$, then under suitable hypotheses we have that 

$$

\frac{d}{dx} \int_{a}^{x} f(t) \ dt = f(x)

$$



we are  trying to put myself in the shoes of Poisson, Cauchy and Riemann. The first theorem is basically saying that to find the area under a curve, we need to find any anti-derivative and evaluate it at the endpoints? 
The second theorem is saying that we can view the integral as a function of $$x$$ and take its derivative to get $$f(x)$$. 
Wasn't the goal of Poisson, Cauchy and Riemann to find the area under a curve? So they hypothesized the first theorem and then only later proposed the second theorem? Both theorems deal with finding the area under a curve (i.e. they are equivalent)? 
Do these theorems still hold under other types of integration (i.e. the Lebesgue integral)?
.

# Answer 


Added.
The relationship between the definite integral and the total change of an accumulation function goes back to well before Poisson, Cauchy, or Riemann. There's a nice historical overview in a recent article by David M. Bressoud, Historical reflections on teaching the Fundamental Theorem of Integral Calculus published in the Monthly last February. You can find one version in Leibniz's work in 1693, where he writes:

"we shall now show that the general problem of quadratures can be reduced to the finding of a line that has a given law of tangency, that is, for which the sides of the characteristic triangle have a given mutual relation. Then we shall show how this line can be described by a motion that we have invented." 

"The problem of quadratures" is the problem of finding areas. Leibniz's proof, which is entirely geometric (you can find it in Bressoud's article) follows from the understanding of areas and tangents as certain sums and differences. But it does not originate with Leibniz: Isaac Barrow gave a proof in his Lectiones geometricae (1670); and James Gregory gives one in his Geometriae pars universalis (1668). Gregory shows that finding the length of a curve is equivalent to finding the area under a related curve: he shows that there is a constant $$c$$, chosen depending on certain given ratios, the length of the curve $$y=f(x)$$ from $$x=a$$ to $$x=b$$ equals the area under the curve $$y=c\sqrt{1+(f'(x))^2}$$ (though of course, not expressed that way). He then deals with the converse: given $$y=g(x)$$ on $$[a,b]$$, finding a curve $$y=u(x)$$ so that the area under the $$y=g(x)$$ is equal to the length of $$y=u(x)$$. He proves that if


$$

u(x) = \frac{1}{c}\int_a^x z(t)\,dt

$$


then $$z/c$$ describes the slope of the tangent to $$u$$; this "contains" the second FTC. 
Even earlier, the first part of what Gregory did had been done by Hendrick van Heureat, published in 1659 in van Schooten's edition of Descartes' Geometry.
Newton, by contrast, gives a kind of "dinamic proof" of the FTC; it has its roots in Oresme's Tractatus de configurationibus qualitatum et motuum (1350), in which he shows that if you represent velocity by a curve, then the area under the curve corresponds to the distance traveled (that is, the integral of the derivative equals the total change of the function, the first part of the FTC). 
So by the time Cauchy and Riemann gave their definitions of integrals, the FTC (both parts) was already on "the table"; they had the onus of showing that their definitions implied the FTC. So the FTC was already "visible" to them (just like it was to Lebesgue), they didn't need to hypothesize the first or second theorem, nor propose them. They only had to show that their definitions were such that the theorems held for their integrals. Much like Lebesgue needed to show that his definition of integral agreed with that of Riemann where they were both defined, but that didn't mean he had to come up with Riemann's definition of integral from scratch: it was already there, he just needed to show his definition did not change the old properties. 

Yes, there are versions of the Fundamental Theorem of Calculus that hold for other types of integrals. A good resource is A Garden of Integrals, by Frank E. Burke. The following statements are taken from there.
The Cauchy Integral
The Cauchy definition of integral (from 1823) is the following:
Given a bounded function $$f$$ on $$[a,b]$$, divide $$[a,b]$$ into a finite number of contiguous subintervals $$[x_{k-1},x_k]$$, $$a= x_0\lt x_1\lt\cdots\lt x_n=b$$. The Cauchy sum of $$f$$ is


$$

\sum_{k=1}^n f(x_{k-1})(x_k-x_{k-1}).

$$


(This is the equivalent of a left-hand sum evaluation in today's parlance). We say that $$f$$ is Cauchy-integrable on $$[a,b]$$ if and only if there exists a number $$A$$ such that for every $$\epsilon\gt 0$$ there exists $$\delta\gt 0$$ such that for any partition $$P$$ of $$[a,b]$$ whose subintervals have length less than $$\delta$$, we have


$$

\left|\sum_{P} f(x_{k-1})(x_k-x_{k-1}) - A\right| \lt \epsilon.

$$


Cauchy proved that continuous functions are Cauchy-integrable, though this does not exhaust the class. We have the following "FTC"s for the Cauchy integral:

FTC for the Cauchy Integral. If $$F$$ is a differentiable function on $$[a,b]$$, and $$F'$$ is continuous on $$[a,b]$$, then $$F'$$ is Cauchy integrable on $$[a,b]$$ and
  

$$

C\int_a^x F'(t)\,dt = F(x)-F(a)

$$


  for each $$x$$ in $$[a,b]$$.

Here, $$C\int$$ denotes the Cauchy integral. 

FTC part 2 for the Cauchy Integral. If $$f$$ is a continuous function on the interval $$[a,b]$$, and we define a function $$F$$ on $$[a,b]$$ by $$F(x) = C\int_a^xf(t)\,dt$$, then $$F$$ is differentiable on $$[a,b]$$, $$F' = f$$ on $$[a,b]$$, and $$F$$ is absolutely continuous on $$[a,b]$$. 

We also have a convergence theorem:

Convergence for Cauchy Integrable Functions. If $$\{f_k\}$$ is a sequence of continuous functions converging uniformly to $$f$$ on $$[a,b]$$, then $$f$$ is Cauchy integrable on $$[a,b]$$ and $$C\int_a^bf(x)\,dx = \lim C\int_a^b f_k(x)\,dx$$. 

The Riemann Integral
The definition of the Riemann integral is the usual one. Lebesgue proved in 1902 that a bounded function on $$[a,b]$$ is Riemann integrable on $$[a,b]$$ if and only if it is continuous almost everywhere.

FTC for the Riemann Integral. If $$F$$ is a differentiable function on the interval $$[a,b]$$, and $$F'$$ is bounded and continuous almost everywhere on $$[a,b]$$, then $$F'$$ is Riemann integrable on $$[a,b]$$, and 

$$

R\int_a^x F'(t)\,dt = F(x) - F(a)

$$

 for each $$x$$ in the interval $$[a,b]$$.
FTC part 2 for the Riemann Integral. Suppose $$f$$ is a bounded and continuous almost everywhere function on the interval $$[a,b]$$. Let $$F$$ on $$[a,b]$$ be defined by $$F(x)=R\int_a^x f(t)\,dt$$. Then $$F$$ is absolutely continuous on $$[a,b]$$; if $$f$$ is continuous at $$x_0\in[a,b]$$, then $$F$$ is differentiable at $$x_0$$ and $$F'(x_0)=f(x_0)$$; and $$F'=f$$ almost everywhere.
Convergence for Riemann Integrable Functions. If $$\{f_k\}$$ is a sequence of Riemann integrable functions converging uniformly to $$f$$ on $$[a,b]$$, then $$f$$ is Riemann integrable and $$R\int_a^b f(x)\,dx = \lim R\int_a^b f_k(x)\,dx$$.

Riemann-Stieltjes Integral
Let $$f$$ and $$\phi$$ be two bounded functions on $$[a,b]$$. We say that $$f$$ is Riemann-Stieltjes integrable with respect to $$\phi$$ if and only if there exists a number $$A$$ such that for every $$\epsilon\gt 0$$ there exists a $$\delta\gt 0$$ such that


$$

\left|\sum_{k=1}^n f(c_k)\bigl(\phi(x_k) - \phi(x_{k-1})\bigr) - A\right|\lt \epsilon

$$


where $$x_{k-1}\leq c_k\leq x_k$$, for every partition $$P$$ of $$[a,b]$$ whose subintervals has length less than $$\delta$$. We write


$$

RS\int_a^b f(x)d\phi(x) = A.

$$



FTC for Riemann Stieltjes Integrals. If $$f$$ is continuous and $$\phi$$ is differentiable, with $$\phi'$$ Riemann integrable on $$[a,b]$$, then 
  

$$

RS\int_a^b f(x)\,d\phi(x) = R\int_a^b f(x)\phi'(x)\,dx.

$$


Theorem. If $$f$$ and $$\phi$$ are bounded functions with no common discontinuities on $$[a,b]$$, and the Riemann-Stieltjes integral of $$f$$ with respect to $$\phi$$ exists, then the Riemann-Stieltjes integral of $$\phi$$ with respect to $$f$$ exists, and
  

$$

RS\int_a^b\phi(x)\,df(x) = f(b)\phi(b) - f(a)\phi(a) - RS\int_a^bf(x)\,d\phi(x).

$$


FTC part two for Riemann-Stieltjes Integrals. If $$f$$ is continuous on $$[a,b]$$ and $$\phi$$ is monotonic increasing on $$[a,b]$$, then $$f$$ is Riemann-Stieltjes integrable with respect to $$\phi$$. If we define $$F$$ on $$[a,b]$$ by
  

$$

F(x) = RS\int_a^x f(t)d\phi(t),

$$


  then $$F$$ is continuous at any point where $$\phi$$ is continuous; and $$F$$ is differentiable at each point where $$\phi$$ is differentiable (almost everywhere) and at such points, $$F' = f\phi'$$.
Convergence Theorem for Riemann-Stieltjes Integrals. If $$\{f_k\}$$ is a sequence of functions that converge uniformly to $$f$$ on $$[a,b]$$ and $$\phi$$ is monotone increasing on $$[a,b]$$, then the $$f_k$$ is Riemann-Stieltjes integrable with respect to $$\phi$$ for each $$k$$, $$f$$ is Riemann-Stieltjes integrable with respect to $$\phi$$, and 

$$

RS\int_a^bf(x)\,d\phi(x) = \lim RS\int_a^b f_k(x)\,d\phi(x).

$$



Lebesgue Integral

FTC for the Lebesgue Integral. If $$F$$ is differentiable, and the derivative $$F'$$ is bounded on $$[a,b]$$, then $$F'$$ is Lebesgue integrable on $$[a,b]$$ and 
  

$$

\int_{[a,x]}F'\,d\mu = F(x)-F(a)

$$


  for $$x$$ in $$[a,b]$$. 
Lebesgue's FTC. If $$F$$ is absolutely continuous on $$[a,b]$$, then $$F'$$ is Lebesgue integrable and
  

$$

\int_{[a,x]} F'\,d\mu = F(x)- F(a)

$$


  for $$x$$ in $$[a,b]$$. 
FTC Part 2 for the Lebesgue Integral. If $$f$$ is Lebesgue integrable on $$[a,b]$$, and we define $$F$$ on $$[a,b]$$ by $$F(x) = \int_{[a,x]}f\,d\mu$$, then $$F$$ is absolutely continuous on $$[a,b]$$ and $$F'=f$$ almost everywhere on $$[a,b]$$.
Dominated Convergence Theorem. If $$\{f_k\}$$ is a sequence of Lebesgue integrable functions converging pointwise almost everywhere to $$f$$ on $$[a,b]$$, and $$g$$ is a Lebesgue integrable function such that 
$$|f_k|\leq g$$ on $$[a,b]$$, then $$f$$ is Lebesgue integrable on $$[a,b]$$ and
  

$$

\int_{[a,b]}f\,d\mu = \lim \int_{[a,b]} f_k\,d\mu.

$$



Henstock-Kurzweil Integral
A function $$\delta\colon [a,b]\to (0,\infty)$$ is called a gauge on $$[a,b]$$. A tagged partition of $$[a,b]$$ is a finite collection of pointed intervals $$(c_k,[x_{k-1},x_k])$$, where $$x_{k-1}\leq c_k\leq x_k$$, $$a=x_0\lt x_1\lt x_2\lt\cdots\lt x_n=b$$. We say a tagged partition of $$[a,b]$$ is $$\delta$$ fine if $$c_k-\delta(c_k) \lt x_{k-1}\leq c_k \leq x_k \lt c_k+\delta(c_k)$$. 
A function $$f$$ on $$[a,b]$$ is said to be Henstock-Kurzweil integrable on $$[a,b]$$ if there is a number $$A$$ such that for every $$\epsilon\gt 0$$ there exists a positive function $$\delta_{\epsilon}\colon [a,b]\to (0,\infty)$$ such that for any $$\delta_{\epsilon}$$-fine partition on $$[a,b]$$ with $$c_{k}-\delta_{\epsilon}(c_k) \lt x_{k-1}\leq c_k \leq x_{k}\lt c_k+\delta_{\epsilon}(c_k)$$, we have:


$$

\left|\sum_{k=1}^n f(c_k)(x_k-x_{k-1}) - A\right|\lt \epsilon.

$$


In that case, we write $$HK\int_a^b f(x)\,dx = A$$.

FTC for the Henstock-Kurzweil Integral. If $$F$$ is continuous on $$[a,b]$$ and $$F$$ is differentiable on $$[a,b]$$ with at most a countable number of exceptional points, then $$F'$$ is Henstock-Kurzweil integrable on $$[a,b]$$, and
  

$$

HK\int_a^x F'(t)\,dt = F(x) - F(a)

$$


  for each $$x$$ in $$[a,b]$$. 
FTC part two for the Henstock-Kurzweil Integral. If $$f$$ is Henstock-Kurtzweil integrable on $$[a,b]$$, and we define $$F$$ by $$F(x) = HK\int_a^x f(t)\,dt$$, then $$F$$ is continuous on $$[a,b]$$, $$F'=f$$ almost everywhere, and $$f$$ is Lebesgue measurable.
Dominated Convergence for Henstock-Kurzweil Integral. If $$\{f_k\}$$ is a sequence of Henstock-Kurzweil integrable functions that converge pointwise to $$f$$ on $$[a,b]$$, and there exist Henstock-Kurzweil integrable functions $$\phi$$ and $$\psi$$ such that $$\phi\leq f_k\leq \psi$$ for all $$k$$, then $$f$$ is Henstock-Kurzweil integrable and
  

$$

HK\int_a^b f(x)\,dx = \lim HK\int_a^b f_k(x)\,dx.

$$




The integrals above are given in increasing order of strength, in the following sense: if $$f$$ is a function on $$[a,b]$$, then:


$$

\begin{align*}
f\text{ is Cauchy integrable on }[a,b] &\Longrightarrow f\text{ is Riemann integrable on }[a,b]\\
&\Longrightarrow f\text{ is Lebesgue integrable on }[a,b]\\
&\Longrightarrow f\text{ is Henstock-Kurzweil integrable on }[a,b]
\end{align*}

$$


and none of the implications are reversible. The Riemann-Stieltjes (and its variant, the Lebesgue-Stieltjes) integral is not included in the chain of implications, because integrability there depends on both the function $$f$$ and the function $$\phi$$.

