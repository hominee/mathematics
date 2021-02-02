---
layout: post
title: Problem related to real analysis and real numbers
tag:
 - real-analysis
 - induction
 - real-numbers

description: Problem related to real analysis and real numbers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

we n-Depth Explanation of How to Do Mathematical we nduction Over the Set $$\mathbb{R}$$ of All Real Numbers?

<!–-break-–>


     we 've seen in the answers to a few different questions here on the Mathematics Stack Exchange that one can clearly do mathematical induction over the set $$\mathbb{R}$$ of all real numbers.  we are , however, having quite a difficult time understanding how the methods described in both those questions' answers and some reference materials to which they link.  in particular,  we  can't seem to figure out exactly how the techniques described therein parallel the methods codified in the axiom of induction for use when doing mathematical induction over the set $$\mathbb{N}$$ of all natural numbers.
     if somebody would be so kind as to provide me with a more detailed explanation of how to do mathematical induction over the set $$\mathbb{R}$$ of all real numbers within about the next day or so, then we  would be very grateful!  
Questions About induction Over the Real Numbers. 


# Answer 


we  feel like we are  jumping into this discussion rather late, but we  feel that the other answers given so far have to a large extent missed the point of the question.
As a matter of fact, you CAN do induction on the real numbers under the standard order! This is called "real induction," and the main result is proven and described at length in the references given by the original poster. Explicitly, suppose $$S$$ is a subset of the closed interval $$[a,b]$$ with the following properties:

$$a$$ is in $$S$$.
For every $$x$$ in $$[a,b)$$, there is a number $$y$$ in $$[a,b]$$ such that every number $$z$$ in $$[x,y]$$ is in $$S$$.
For every $$x$$ in $$[a,b]$$, if $$[a,x)$$ is a subset of $$S$$, then $$x$$ is in $$S$$.

Then $$S=[a,b]$$.
Although it doesn't involve a successor function, this captures a lot of the flavor of both induction on the natural numbers and transfinite induction. Moreover, because it uses the usual order on $$\mathbb{R}$$, it can be used to prove interesting theorems about real numbers, including the intermediate Value Theorem, the Extreme Value Theorem, and the Bolzano-Weierstrass Theorem.
For an example of how to use real induction in a proof, look at Theorem 5 (the Extreme Value Theorem) in the first reference. Clark proves that every continuous function on a closed interval $$[a,b]$$ is bounded as follows:
Let $$f$$ be a continuous real-valued function on the closed interval $$[a,b]$$. Take $$S$$ to be the set of numbers $$x$$ in $$[a,b]$$ for which $$f$$ is bounded on $$[a,x]$$. 

Clearly $$f$$ is bounded on $$[a,a]$$ (any number greater than $$f(a)$$ is an upper bound, and any number less than $$f(a)$$ is a lower bound), so $$a$$ is in $$S$$. 
Suppose $$x$$ is in $$S$$. Then $$f$$ is bounded on $$[a,x]$$. Since $$f$$ is continuous at $$x$$, there is a $$\delta>0$$ such that, for all $$y$$ in $$[x-\delta,x+\delta]$$,$$\left|f(y)\right|<\left|f(x)\right|+1$$, so $$f$$ is bounded on $$[a,x+\delta]$$. 
Now suppose  $$[a,x)$$ is a subset of $$S$$. Since $$f$$ is continuous at $$x$$, there is a positive number $$\delta < x − a$$ such that $$f$$ is bounded on $$[x − \delta, x]$$. But since $$a < x − \delta < x$$, we know also that $$f$$ is bounded on $$[a, x − \delta]$$, so $$f$$ is bounded on $$[a, x]$$.

Since $$S$$ satisfies the three properties given above, it follows by real induction that $$S=[a,b]$$, so $$f$$ is bounded on $$[a,b]$$.

