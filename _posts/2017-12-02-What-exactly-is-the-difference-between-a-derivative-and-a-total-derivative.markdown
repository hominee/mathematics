---
layout: post
title: What exactly is the difference between a derivative and a total derivative
tag:
 - multivariable-calculus
 - derivatives

description: What exactly is the difference between a derivative and a total derivative

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What exactly is the difference between a derivative and a total derivative?

<!–-break-–>


we are  not too grounded in differentiation but today, we was posed with a supposedly easy question $$w = f(x,y) = x^2 + y^2$$ where $$x = r\sin\theta $$ and $$y = r\cos\theta$$ requiring the solution to $$\partial w / \partial r$$ and $$\partial w / \partial \theta $$.
 we simply solved the former using the trig identity $$\sin^2 \theta + \cos^2 \theta = 1$$, resulting to $$\partial w / \partial r = 2r$$.

However we was told that this solution could not be applied to this question because we should be solving for the total derivative.
 we could not find any good resource online to explain clearly to me the difference between a normal derivative and a total derivative and why my solution here was wrong.
 Is there anyone who could explain the difference to me using a practical example? Thanks!
.


# Answer 


The key difference is that when you take a partial derivative, you operate under a sort of assumption that you hold one variable fixed while the other changes. When computing a total derivative, you allow changes in one variable to affect the other.
So, for instance, if you have $$f(x,y) = 2x+3y$$, then when you compute the partial derivative $$\frac{\partial f}{\partial x}$$, you temporarily assume $$y$$ constant and treat it as such, yielding $$\frac{\partial f}{\partial x} = 2 + \frac{\partial (3y)}{\partial x} = 2 + 0 = 2$$.
However, if $$x=x(r,\theta)$$ and $$y=y(r,\theta)$$, then the assumption that $$y$$ stays constant when $$x$$ changes is no longer valid. Since $$x = x(r,\theta)$$, then if $$x$$ changes, this implies that at least one of $$r$$ or $$\theta$$ change. And if $$r$$ or $$\theta$$ change, then $$y$$ changes. And if $$y$$ changes, then obviously it has some sort of effect on the derivative and we can no longer assume it to be equal to zero.
In your example, you are given $$f(x,y) = x^2+y^2$$, but what you really have is the following:
$$f(x,y) = f(x(r,\theta),y(r,\theta))$$.
So if you compute $$\frac{\partial f}{\partial x}$$, you cannot assume that the change in $$x$$ computed in this derivative has no effect on a change in $$y$$.
What you need to compute instead is $$\frac{\rm{d} f}{\rm{d}\theta}$$ and $$\frac{\rm{d} f}{\rm{d} r}$$, the first of which can be computed as:
$$\frac{\rm{d} f}{\rm{d}\theta} = \frac{\partial f}{\partial \theta} + \frac{\partial f}{\partial x}\frac{\rm{d} x}{\rm{d} \theta} + \frac{\partial f}{\partial y}\frac{\rm{d} y}{\rm{d} \theta}$$

