---
layout: post
title: Problem related to real analysis and examples counterexamples
tag:
 - real-analysis
 - measure-theory
 - functional-analysis
 - banach-spaces
 - examples-counterexamples

description: Problem related to real analysis and examples counterexamples

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is it possible for a function to be in $$L^p$$ for only one $$p$$?

<!–-break-–>


we are  wondering if it's possible for a function to be an $$L^p$$ space for only one value of $$p \in [1,\infty)$$ (on either a bounded domain or an unbounded domain).
One can use interpolation to show that if a function is in two $$L^p$$ spaces, (e.g. $$p_1$$ and $$p_2$$,with $$p_1 \leq p_2$$ then it is in all $$p_1\leq p \leq p_2$$). 
Moreover, if we're on a bounded domain, we also have the relatively standard result that if $$f \in L^{p_1}$$ for some $$p_1 \in [1,\infty)$$, then it is in $$L^p$$ for every $$p\leq p_1$$ (which can be shown using Hölder's inequality).
Thus, we think that the question can be reduced to unbounded domains if we consider the question for any $$p>1$$. 
Intuitively, a function on an unbounded domain is inside an $$L^p$$ space if it decrease quickly enough toward infinity. This makes it seem like we might be able to multiply the function by a slightly larger exponent. At the same time, doing this might cause the function to blow up near zero. That's not precise/rigorous at all though.   
So we are  wondering if it is possible to either construct an example or prove that this can't be true.

# Answer 


Robert's and joriki's examples are of course nice and explicit, but you can get examples on any subset of $$\mathbb{R}^n$$ with infinite measure. 

Here's how:
Take a function $$f$$ that is in $$L^p$$ but not in $$L^q$$ for $$q \gt p$$ (on the unit ball $$B$$ around zero, say). 

Now take a sequence $$x = (x_n)$$ that is in $$\ell^p$$ but not in $$\ell^q$$ for $$q \lt p$$ (there are standard examples for both of these things). 

Now take disjoint balls $$B_n$$ of volume $$1$$ (disjoint from $$B$$) and consider $$g = f + \sum x_n \cdot [B_n]$$ where $$[B_n]$$ denotes the characteristic function of $$B_n$$. Obviously, $$\|g\|_{q}^q = \|f\|_{q}^q + \|x\|_{q}^{q}$$ is in $$L^q$$ if and only if $$q = p$$. If $$q \lt p$$ then $$\|x\|_q = \infty$$ and if $$q \gt p$$ then $$\|f\|_{q}^q = \infty$$.
we leave it to you to make that explicit and to modify it when your domain is not all of $$\mathbb{R}^n$$.

