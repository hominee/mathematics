---
layout: post
title: Problem related to calculus and indeterminate forms
tag:
 - calculus
 - real-analysis
 - analysis
 - infinity
 - indeterminate-forms

description: Problem related to calculus and indeterminate forms

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Why is $$1^{\infty}$$ considered to be an indeterminate form

<!–-break-–>


From Wikipedia: in calculus and other branches of mathematical analysis, an indeterminate form is an algebraic expression obtained in the context of limits. Limits involving algebraic operations are often performed by replacing subexpressions by their limits; if the expression obtained after this substitution does not give enough information to determine the original limit, it is known as an indeterminate form. 

The indeterminate forms include $$0^{0},\frac{0}{0},(\infty - \infty),1^{\infty}, \ \text{etc}\cdots$$

My question is can anyone give me a nice explanation of why $$1^{\infty}$$ is considered to be an indeterminate form? Because, i don't see any justification of this fact. we are  still perplexed.

# Answer 


Forms are indeterminate because, depending on the specific expressions involved, they can evaluate to different quantities.  For example, all of the following limits are of the form $$1^{\infty}$$, yet they all evaluate to different numbers.

 $$ 
\lim_{n \to \infty} \left(1 + \frac{1}{n^2}\right)^n = 1
 $$ 


 $$ 
\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e
 $$ 


 $$ 
\lim_{n \to \infty} \left(1 + \frac{1}{\ln n}\right)^n = \infty
 $$ 

To expand on this some (and this thought process can be applied to other indeterminate forms, too), one way to think about it is that there's a race going on between the expression that's trying to go to 1 and the expression that's trying to go to $$\infty$$.  if the expression that's going to 1 is in some sense faster, then the limit will evaluate to 1.  if the expression that's going to $$\infty$$ is in some sense faster, then the limit will evaluate to $$\infty$$.  if the two expressions are headed toward their respective values at essentially the same rate, then the two effects sort of cancel each other out and you get something strictly between 1 and $$\infty$$.
There are some other cases, too, like 

 $$ 
\lim_{n \to \infty} \left(1 - \frac{1}{\ln n}\right)^n = 0,
 $$ 

but this still has the expression going to $$\infty$$ "winning."  Since $$1 - \frac{1}{\ln n}$$ is less than 1 (once $$n > 1$$), the exponentiation forces the limit to 0 rather than $$\infty$$.

