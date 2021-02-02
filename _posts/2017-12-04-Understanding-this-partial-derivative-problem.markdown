---
layout: post
title: Understanding this partial derivative problem
tag:
 - multivariable-calculus

description: Understanding this partial derivative problem

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Understanding this partial derivative problem

<!–-break-–>



Problem:
Considering $$x$$ and $$y$$ as independent
   variables, find $$\frac{\partial
 r}{\partial x}, \frac{\partial
 r}{\partial y}, \frac{\partial
 \theta}{\partial x}, \frac{\partial
 \theta}{\partial y}$$ when $$x = e^{2r}
 \cos \theta, y = e^{3r} \sin \theta$$.

Solution:
First differentiate the given
   relations with respect to $$x$$:
$$1 = 2e^{2r} \cos \theta
   \frac{\partial r}{\partial x} - e^{2r}
   \sin \theta \frac{\partial
   \theta}{\partial x}$$ and $$0 =
 3e^{3r}\sin \theta \frac{\partial
 r}{\partial x} + e^{3r} \cos \theta
 \frac{\partial \theta}{\partial x}$$.

Then solve simultaneously to obtain
   $$\frac{\partial r}{\partial x} =
 \frac{\cos \theta}{e^{2r}(2+\sin^{2}
 \theta)}$$ and $$\frac{\partial
 \theta}{\partial x} = - \frac{3 \sin
 \theta}{e^{2r}(2+sin^2 \theta)}$$

Question:
(1)
So first of all, why does differentiating with respect to $$x$$ result in $$\frac{\partial r}{\partial x}$$ and $$\frac{\partial \theta}{\partial x}$$ (by the way what are these called?)? Is this because the problem says "$$x$$ and $$y$$ as independent variables" ? My initial reaction was to do $$r$$ and $$\theta$$ separately while regarding all other variables as constants.
.
.
 This is implicit (partial?) differentiation, right?
How should we understand what is being done here? A lot of times it seems that things like this turn out to really just be a mapping.
 Can we think of this that way as well? we couldn't even say what the domain and codomain would be.
.
.

Whenever we perform this operation, do we just take partial derivatives of both sides treating all independent variables (other than the variable with respect to which we are  differentiating) as constants and all non-independent (dependent?) variables as variables that need to be differentiated and will have that partial derivative symbol? Once we accept that we can see how they got the first implicit partial differentiation (if that's what it is called).

(2)
What do they mean by "solve simultaneously" ? we tried to solve for each (again we don't know what they're called yet) "partial differential" resulting in: $$\frac{\partial \theta}{\partial x} = -\frac{\sin \theta \frac{\partial r}{\partial x}}{\cos \theta}$$ and $$\frac{\partial r}{\partial x} = \frac{1+e^{2r}\sin \theta \frac{\partial \theta}{\partial x}}{2e^{2r}\cos \theta}$$.
 But we couldn't get the same answer.
.
.
 we tried to substitute this further, but looking at that answer, we was sure we was missing something.
.
.


# Answer 



That's just the Chain Rule (with partials because you know there are 'really' two variables around). Think of $$r$$ as a function $$r(x,y)$$, and $$\theta$$ as a function $$\theta(x,y)$$, and you are just doing implicit differentiation/chain rule. The fact that "$$x$$ and $$y$$ are independent variables" tells you that $$\frac{dy}{dx} = 0$$, so that's why you get that differentiating the relation $$y=e^{3r}\cos\theta$$ with respect to $$x$$ gives you $$0$$ on the left hand side.
You have two expressions, both involving the unknown functions $$\frac{\partial r}{\partial x}$$, $$\frac{\partial \theta}{\partial x}$$. Think of those two as the "unknowns" in a $$2\times 2$$ system, and solve the system (like you would a regular system of two equations in two unknowns) to get expressions for each involving only $$r$$s and $$\theta$$s, and no partials, $$x$$s, or $$y$$s.
E.g., take the second equation and multiply through by $$2\cos\theta$$ to get


$$

0 = 6e^{3r}\sin\theta\cos\theta\frac{\partial r}{\partial x} + 2e^{3r}\cos^2\theta\frac{\partial\theta}{\partial x}.

$$


Then take the first equation and multiply through by $$-3e^r\sin\theta$$ to get


$$

-3e^r\sin\theta = -6e^{3r}\sin\theta\cos\theta\frac{\partial r}{\partial x} +3e^{3r}\sin^2\theta \frac{\partial\theta}{\partial x}.

$$


Adding both equations eliminates $$\frac{\partial r}{\partial x}$$, so now you can solve for $$\frac{\partial\theta}{\partial x}$$. Etc.

Then you do the same thing but with partials with respect to $$y$$, using the fact that $$x$$ and $$y$$ are independent to get that $$\frac{dx}{dy}=0$$. 

