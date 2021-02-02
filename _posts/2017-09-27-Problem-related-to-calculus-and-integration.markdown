---
layout: post
title: Problem related to calculus and integration
tag:
 - calculus
 - integration

description: Problem related to calculus and integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What is so special about $$\alpha=-1$$ in the integral of $$x^\alpha$$?

<!–-break-–>


Of course, it is easy to see, that the integral (or the
antiderivative) of $$f(x) = 1/x$$ is $$\log(|x|)$$ and of course for
$$\alpha\neq - 1$$ the antiderivative of $$f(x) = x^\alpha$$ is
$$x^{\alpha+1}/(\alpha+1)$$.
we was wondering if there is an intuitive (probably geometric)
explanation why the case $$\alpha=-1$$ is so different and why the
logarithm appears?
Some answers which we thought of but which are not convincing:

Taking the limit $$\alpha=-1$$ either from above or below lead to diverging functions.
Some speciality of the case $$\alpha=-1$$ are that both asymptotes are non-integrable. However, the antidrivative is a local thing, and hence, shouldn't care about the behavior at infinity.

.

# Answer 


Assume you know that for every $$\beta$$ the derivative of the function $$x\mapsto x^\beta$$ is the function $$x\mapsto\beta x^{\beta-1}$$ and that you want to choose $$\beta$$ such that the derivative is a multiple of the function $$x\mapsto x^{\alpha}$$. You are led to solve the equation $$\beta-1=\alpha$$, which yields $$\beta=\alpha+1$$. If $$\alpha=-1$$, this gets you $$\beta=0$$, but then the derivative you obtain is the function $$x\mapsto 0x^{-1}=0$$, which is not a nonzero multiple of $$x\mapsto x^{-1}$$. For every other $$\alpha$$, this procedure gets you an antiderivative but for $$\alpha=-1$$, you failed. Or rather, you proved that no power function is an antiderivative of $$x\mapsto x^{-1}$$. Your next step might be (as mathematicians often do when they want to transform one of their failures into a success) to introduce a new function defined as the antiderivative of $$x\mapsto x^{-1}$$ which is zero at $$x=1$$, and maybe to give it a cute name like logarithm, and then, who knows, to start studying its properties...


**Edit** (Second version, maybe more geometric.)
Fix $$s>t>0$$ and $$c>1$$ and consider the area under the curve $$x\mapsto x^\alpha$$ between the abscissæ $$x=t$$ and $$x=s$$ on the one hand and between the abscissæ $$x=ct$$ and $$x=cs$$ on the other hand. Replacing $$x$$ by $$cx$$ multiplies the function by a factor $$c^\alpha$$. The length of the interval of integration is multiplied by $$c$$ hence the integral itself is multiplied by $$c^{\alpha+1}$$.
On the other hand, if an antiderivative $$F$$ of $$x\mapsto x^\alpha$$ is a multiple of  $$x\mapsto x^\beta$$ for a given $$\beta$$, then $$F(ct)=c^\beta F(t)$$ and $$F(cs)=c^\beta F(s)$$ hence $$F(ct)-F(cs)=c^\beta (F(t)-F(s))$$. 

**Note** that this last relation holds even if one assumes only that $$F$$ is the sum of a constant and a multiple of  $$x\mapsto x^\beta$$.
Putting the two parts together yields $$c^{\alpha+1}=c^\beta$$. Once again, if $$\alpha=-1$$, this would yield $$\beta=0$$, hence $$F$$ would be constant and the area $$F(t)-F(s)$$ under the curve $$x\mapsto x^\alpha$$ from $$s$$ to $$t\ge s$$ would be zero for every such $$s$$ and $$t$$, which is impossible since the function $$x\mapsto x^\alpha$$ is not zero. (And for every $$\alpha\ne1$$, this scaling argument yields the correct exponent $$\beta$$.)

