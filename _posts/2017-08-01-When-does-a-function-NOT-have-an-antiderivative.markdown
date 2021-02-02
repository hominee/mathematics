---
layout: post
title: When does a function NOT have an antiderivative
tag:
 - integration

description: When does a function NOT have an antiderivative
hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When does a function NOT have an antiderivative?

<!–-break-–>



we  know this question may sound naïve but why can't we write $$\int e^{x^2} dx$$ as $$\int e^{2x} dx$$? The former does not have an antiderivative, while the latter has.
we n light of this question, what are sufficient conditions for a function NOT to have an antiderivative. That is, do we need careful examination of a function to say it does not have an antiderivative or is there any way that once you see the function, you can right away say it does not have an antiderivative?
.

# Answer 


As you might have realised, exponentiation is not associative:

 $$ 
\left(a^b\right)^c \ne a^\left(b^c\right)
 $$ 

So what should $$a^{b^c}$$ mean? The convention is that exponentiation is right associative:

 $$ 
a^{b^c} = a^\left(b^c\right)
 $$ 

Because the otherwise left-associative exponentiation is just less useful and redundant, as it can be represented by multiplication inside the power (again as you might have realised):

 $$ 
a^{bc} = \left(a^b\right)^c
 $$ 

Wikipedia on associativity of exponentiation.

