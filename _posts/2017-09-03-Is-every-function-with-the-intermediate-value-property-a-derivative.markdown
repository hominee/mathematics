---
layout: post
title: Is every function with the intermediate value property a derivative
tag:
 - real-analysis
 - examples-counterexamples

description: Is every function with the intermediate value property a derivative

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

is every function with the intermediate value property a derivative?

<!–-break-–>


As it is well known every continuous function has the intermediate value property, but even some discontinuous functions like 

 $$ 
f(x)=\left\{
\begin{array}{cl}
\sin\left(\frac{1}{x}\right) & x\neq 0 \\
0 & x=0
\end{array}
\right.
 $$ 

are having this property?

in fact i know that a derivative always have this property. 
My question is, if for every function $$f$$ with the intermediate value property exists a function $$F$$ such that $$F'=f$$.  And if so, is $$F$$ unique (up to a constant you may add)?
My attempts till now: (Just skip them if you feel so)
The most natural way of finding those functions would be integrating, so i  guess the question can be reduced to, if functions with the intermediate value property can be integrated.
This one depends heavy on how you define when a functions is integrable, i (my analysis class) said that i call a function integrable when it is a regulated function (the limits $$x\to x_0^+ f(x)$$ and $$x\to x_0^- f(x)$$ exists ) .
 As my example above shows, not every function with the intermediate value property is a regulated function. But if isay a function is integrabel when every riemann sum converges the above function is integrable, so it seems like this would be a better definition for my problem.  

**Edit**: As Kevin Carlson points out in a commentar that being a derivative is different from being riemann integrable, he even gave an example for a function which is differentiable but it's derivative is not riemann integrable. So i can't show that those functions are riemann integrable as they  are not riemann integrable in general. Now i  have no clue how to find an answer.

# Answer 


if you compose $$ \tan^{-1} $$ with Conway’s Base-$$ 13 $$ Function, 
then you get a bounded real-valued function on the open interval $$ (0,1) $$ 
that satisfies the intermediate Value Property but is discontinuous at every point in $$ (0,1) $$. 
Therefore, by Lebesgue’s theorem on the necessary and sufficient conditions for Riemann-integrability, 
this function is not Riemann-integrable on any non-degenerate closed sub-interval of $$ (0,1) $$.
Now, it cannot be the derivative of any function either, because by the Baire Category Theorem, 
if a function defined on an open interval has an antiderivative, then the function must be continuous 
on a dense set of points. This thread may be of interest to you. :)

