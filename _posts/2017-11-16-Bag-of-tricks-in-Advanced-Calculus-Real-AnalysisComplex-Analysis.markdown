---
layout: post
title: Bag of tricks in Advanced Calculus Real AnalysisComplex Analysis
tag:
 - calculus
 - real-analysis
 - complex-analysis
 - big-list

description: Bag of tricks in Advanced Calculus Real AnalysisComplex Analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Bag of tricks in Advanced Calculus/ Real Analysis/Complex Analysis

<!–-break-–>


we are  studying for an exam and we have been studying my butt off
during the winter break for it.
 During the course of my study we have written
down quite a number of tricks, which in my opinion were 'outrageous' :-).
 Meaning there
was no way we would come up with that during an exam if we hadn't seen that before.

Couple of examples.


Sometimes, when you want to prove something about $$\max$$, $$\min$$, you write ( we got this from Baby Rudin)



$$

 \max(a,b)=\frac{a+b+ \vert a-b \vert} {2} 

$$




$$

 \min (a,b)= \frac{a+b-\|a-b\|} {2} 

$$



To prove Hölder's inequality (in its simplest case)
You write $$\int (f+tg)^2 \geq 0$$ and since this stays positive
you get that the discriminant of this must be negative, and magically
you get your Hölder inequality.

When you want to show something about distinct zeroes of complex functions you kind of eliminate the zeroes of f by dividing them with the appropriate Möbius transforms and you still get an analytic functions which has nice properties.


The value of these is that they can be used in other contexts to write neat proofs.
 
That's what we mean by "tricks".
 This might be difficult to answer,
but what are some of the tricks you wise folks have up your sleeve when it comes to
Advanced Calculus (Both single variable, multivariable) and complex Analysis.

Anything you have to share will be greatly appreciated.


# Answer 


Here are a couple of tricks and general plans of approach we know:

If $$x\in\Bbb R$$ and for all $$\epsilon>0$$ we have that $$\|x\|\leq\epsilon$$, then $$x=0$$. we think of this fact as being Real Analysis in a nutshell.
Never forget that if $$A\subseteq\Bbb R$$ is bounded above and $$M=\sup A$$, then for all $$\epsilon>0$$ there is a $$y\in A$$ such that $$M< y+\epsilon$$. Likewise if $$A$$ is bounded below and $$m=\inf A$$, then for all $$\epsilon>0$$ there is a $$y\in A$$ such that $$y-\epsilon< m$$. This is the most important tie between $$\Bbb R$$'s algebraic and ordering properties.
Never underestimate the binomial theorem even if you just want an inequality. As an example, look at theorem 3.20(c) in Rudin and how he uses it.
For all $$x,y\in\Bbb R$$ and any $$\epsilon> 0$$, we have the following inequality:


$$

\|xy\|\leq \frac{\epsilon\,x^2+\epsilon^{-1}\,y^2}{2}

$$

 This can be derived from the observiation that $$(\epsilon\,\|x\|-\|y\|)^2\geq 0$$. This inequality allows us to decide how much 'weight' we want to give to a particular term in a product. This can be used to show that the product of Riemann integrable functions is still Riemann integrable.
A simple inequality to remember is 

$$

(a+b)^p\leq 2^p(a^p+b^p)

$$

 for $$a,b,p\geq 0$$. This can be derived from the even simpler inequality $$(a+b)\leq 2\max(a,b)$$, again for positive values. This inequality can be used to show that the $$L^p$$ spaces are vector spaces.
The Weierstrass M-test is the first friend you call when dealing with series of functions.
Ask yourself whether the problem you're working on can be generalized to topology first. Think about compactness and connectedness and the abstract theorems about them you already know.
Perhaps the greatest topological property that $$\Bbb R$$ has is second-countability. This means that $$\Bbb R$$ is hereditarily-separable, sequential, Frechet-Urysohn, and c.c.c. This property of $$\Bbb R$$ allows us to consider sequences and sequential continuity in place of neighborhoods and continuity. As an adage, if you are working with $$\epsilon$$, wonder to yourself if you can instead work with $$1/n$$ with $$n\in\Bbb N$$.


