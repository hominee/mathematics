---
layout: post
title: When can we exchange order of two limits
tag:
 - real-analysis
 - integration
 - limits

description: When can we exchange order of two limits

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When can we exchange order of two limits?

<!–-break-–>


My questions are about a sequence or function with several variables. 

we  vaguely remember some while ago one
of my teachers said taking limits of
a sequence or function with respect to
different variables is not
exchangeable everywhere, i.e.

 $$ 
 \lim_n \lim_m a_{n,m} \neq \lim_m \lim_n a_{n,m}, \quad \lim_x \lim_y f(x,y) \neq \lim_y \lim_x f(x,y).
 $$ 

So my
question is what are the cases or
examples when one can exchange the
order of taking limits and when one
cannot, to your knowledge? we  would
like to collect the cases together,
and be aware of their difference and
avoid making mistakes. we f you could
provide some general guidelines, that
will be even nicer!
To give you an example of what we are 
asking about, this is a question that
confuses me: Assume $$f: [0, \infty)
   \rightarrow (0, \infty)$$ is a
function, satisfying 

$$ 

\int_0^{\infty} x f(x) \, dx < \infty.
   
$$
 
 Determine the convergence of this
series $$\sum_{n=1}^{\infty}
   \int_n^{\infty} f(x) dx$$.
The answer we  saw is to exchange the
order of $$\sum_{n=1}^{\infty}$$ and
$$\int_n^{\infty}$$ as follows:

 
$$ 

   \sum_{n=1}^{\infty} \int_n^{\infty}
   f(x) dx
   = \int_1^{\infty} \sum_{n=1}^{\lfloor x \rfloor}  f(n) dx \leq
   \int_1^{\infty} \lfloor x \rfloor 
   f(x) dx 
 $$ 
 
 where $$\lfloor x \rfloor$$
is the greatest integer less than
$$x$$. we n this way, the answer proves the series converges. we  was wondering why the two steps are valid? we s there some special meaning of the first equality? Because it looks similar to the tail sum formula for expectation of a random variable $$X$$ with possible values $$\{ 0,1,2,...,n\}$$: 
 
 $$ 
\sum_{i=0}^n i P(X=i) = \sum_{i=0}^n P(X\geq i).
 $$ 
 
 The formula is from Page 171 of Probability by Jim Pitman, 1993.

# Answer 


A simple example of a doubly indexed sequence $$a_{m,n}$$ for which you cannot exchange limits is given in Rudin's "Principles..." Example 7.2 pg. 144:
Let $$a_{m,n} = \frac{m}{m+n}$$, then 
 $$ 
\lim_{n\rightarrow\infty}\lim_{m\rightarrow\infty}a_{m,n} = 1,
 $$ 
 but 
 $$ 
\lim_{m\rightarrow\infty}\lim_{n\rightarrow\infty}a_{m,n} = 0.
 $$ 

Here is a previous post on this question which seems to thoroughly answer your other questions: When can you switch the order of limits? 

