---
layout: post
title: Problem related to calculus and exponential function
tag:
 - calculus
 - ordinary-differential-equations
 - derivatives
 - exponential-function

description: Problem related to calculus and exponential function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proof that $$C\exp(x)$$ is the only set of functions for which $$f(x) = f'(x)$$

<!–-break-–>


we was wondering the following.
 And we probably know the answer already: NO.

Is there another number with similar properties as $$e$$? So that the derivative of $$\exp(x)$$ is the same as the function itself.

we can guess that it's probably not, because otherwise $$e$$ wouldn't be that special, but is there a proof of it?
.


# Answer 


Of course $$C e^x$$ has the same property for any $$C$$ (including $$C = 0$$). But these are the only ones.
Proposition: Let $$f : \mathbb{R} \to \mathbb{R}$$ be a differentiable function such that $$f(0) = 1$$ and $$f'(x) = f(x)$$. Then it must be the case that $$f = e^x$$.
Proof. Let $$g(x) = f(x) e^{-x}$$. Then 


$$

g'(x) = -f(x) e^{-x} + f'(x) e^{-x} = (f'(x) - f(x)) e^{-x} = 0

$$


by assumption, so $$g$$ is constant. But $$g(0) = 1$$, so $$g(x) = 1$$ identically. 
N.B. 

**Note** that it is also true that $$e^{x+c}$$ has the same property for any $$c$$. Thus there exists a function $$g(c)$$ such that $$e^{x+c} = g(c) e^x = e^c g(x)$$, and setting $$c = 0$$, then $$x = 0$$, we conclude that $$g(c) = e^c$$, hence $$e^{x+c} = e^x e^c$$. 
This observation generalizes to any differential equation with translation symmetry. Apply it to the differential equation $$f''(x) + f(x) = 0$$ and you get the angle addition formulas for sine and cosine. 

