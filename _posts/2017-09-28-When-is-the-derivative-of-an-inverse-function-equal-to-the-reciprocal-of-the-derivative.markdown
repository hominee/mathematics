---
layout: post
title: When is the derivative of an inverse function equal to the reciprocal of the derivative
tag:
 - calculus
 - derivatives
 - inverse

description: When is the derivative of an inverse function equal to the reciprocal of the derivative

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When is the derivative of an inverse function equal to the reciprocal of the derivative?

<!–-break-–>


When is this statement true?


$$

\dfrac {\mathrm dx}{\mathrm dy} = \frac 1 {\frac {\mathrm dy}{\mathrm dx}}

$$


where $$y=y(x)$$. we think that $$y(x)$$ has to be bijective in order to have an inverse and let the expression $$\dfrac {\mathrm dx}{\mathrm dy}$$ make sense. But is there any other condition?
.

# Answer 


Assume $$g(f(x))=x$$. Then


$$

g'(f(x))f'(x)=1

$$

 and then


$$

g'(f(x))=\frac1{f'(x)}

$$




**Note** that we need also that $$f'(x)\neq 0$$. All the conditions (the injectivity and the differentability of $$f$$ and that $$f'$$ does not vanish) must meet in a neighbourhood of the point where you are differentiating, that is, this works locally.
See the inverse function theorem.

