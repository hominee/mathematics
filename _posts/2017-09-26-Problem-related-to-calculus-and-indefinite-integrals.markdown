---
layout: post
title: Problem related to calculus and indefinite integrals
tag:
 - calculus
 - real-analysis
 - logarithms
 - indefinite-integrals

description: Problem related to calculus and indefinite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

The deep reason why $$\int \frac{1}{x}\operatorname{d}x$$ is a transcendental function ($$\log$$)

<!–-break-–>


In general, the indefinite integral of $$x^n$$  has power $$n+1$$.  This is the standard power rule.  Why does it "break" for $$n=-1$$?  In other words, the derivative rule 

$$

\frac{d}{dx} x^{n} = nx^{n-1}

$$

 fails to hold for $$n=0$$.
Is there some deep reason for this discontinuity?
.

# Answer 


I'll try to give a soft answer to what we see as the spirit of the question, which is not why you get exactly log, but why the behaviour is different when integrating $$x^{k}$$ for $$k=-1$$.
The way we see it is that the logarithm would actually be there for other powers of $$x$$ too, but it's "hidden" by the fact that in a geometric series one term "gobbles up" all the others together, except in the very special case when all terms are equal. Put in other words, the intuition is very close to the reason why $$\sum_{i=a}^b c^i$$ can be reasonably approximated by just the first term of the sum ($$c^a$$) if $$c<1$$, and just by the last ($$c^b$$) if $$c>1$$, regardless of how large $$b-a$$ is, i.e. of how many terms you have in the sum. But if $$c=1$$ no single term dominates all the others, and that's when you have to count them all, and you end up seeing the $$b-a$$ term "emerge" in $$\sum_{i=a}^b 1^i=b-a+1$$.
Informally, you can see how this applies to the case at hand writing $$\int_{x_0}^{x_f} x^k dx$$ as $$\int_{x_0}^{2 x_0} x^k dx + \int_{2x_0}^{4x_0} x^k dx + ...$$. Each of the $$\approx \log_2 \frac{x_f}{x_0}$$ terms has the same weight as the others if, and only if, $$k$$ has a very specific value (which?), in which case $$\int_{x_0}^{x_f} x^k dx$$ equals $$\approx \log_2 \frac{x_f}{x_0}$$ times $$\int_{x_0}^{2 x_0} x^k dx$$. If it's just an $$\epsilon$$ smaller, or larger, you get the sum within a constant factor of either $$\int_{x_0}^{2 x_0} x^k dx$$ or of $$\int_{\frac{1}{2}x_f}^{x_f} x^k dx$$, respectively, regardless of $$\frac{x_f}{x_0}$$. 

**Note** that instead of using $$2$$ as a base, we could have used $$3$$, or $$e$$, or $$7.24$$, or $$\pi$$, and the critical value of $$k$$ would have remained the same: it's the value that ensures that if you integrate $$x^k$$ over an interval $$7.24$$ longer, but with a starting point $$7.24$$ times larger, the integral does not change, $$k=-1$$.
This is actually a phenomenon that we have  seen pop up really really often in math, physics, and computer science. You often have a sum of many terms, and a parameter that, for small values, makes the first term of the sum dominate all the others put together, and for large values, makes the last term dominate all the others put together, regardless of how many terms you have in the sum. But when the parameter equals exactly the critical value at which the transition between the two regimes occurs, all sort of strange quantities related to the number of terms in the sum appear in any approximation of it.

