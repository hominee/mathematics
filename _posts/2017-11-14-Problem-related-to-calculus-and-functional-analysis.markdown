---
layout: post
title: Problem related to calculus and functional analysis
tag:
 - calculus
 - real-analysis
 - functional-analysis

description: Problem related to calculus and functional analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Prove there is an increasing function on closed bounded interval that is continuous only at points in $$[a,b] \setminus C$$

<!–-break-–>



Let $$C$$ be a countable subset of $$(a,b)$$.
 Then there is an increasing function on $$(a,b)$$ that is continuous only on $$(a,b)\setminus C$$

This is an example from Royden's real analysis book.
 The function defined on $$(a,b)$$ is $$f(x)=\sum_{\{n:q_n \le x\}}\frac{1}{2^n}$$ where $$\{q_n\}$$ is an enumeration of $$C$$ .
 To show continuity on $$(a,b)\setminus C$$ he says let $$x_0$$ be in $$(a,b)\setminus C$$ and let $$n$$ be any natural number.
 Then there exists an interval, $$I$$, that contains $$x_0$$.
 In addition, $$q_n$$ is not in $$I$$ for $$1\le k \le n$$.
 Then this implys that $$\|f(x)-f(x_0)\| < \frac{1}{2^n}$$ for $$x \in I$$.
 
we understand this part.
 Then there is a problem right after this proof says:


Let $$C$$ be a countable subset of the nondegenerate closed bounded interval $$[a,b]$$.
 Then there is an increasing  function on $$[a,b]$$ that is continuous only on $$[a,b]\setminus C$$.



Show that there is a strictly increasing function on $$[0,1]$$ that is continuous only at the irrationals in $$[0,1]$$.

Let $$f$$ be a monotone function on a subset $$E$$ of $$\mathbb R$$.
 Show that $$f$$ is continuous except possibly at a countable number of points n $$E$$.
 
Let $$E$$ be a subset of $$\mathbb R$$ and $$C$$ a countable subset of $$E$$.
 Is there a monotone function on $$E$$ that is continuous only at points $$E \setminus C$$?


These are four successive problems on Page 109 from Royden's real analysis book.
 So we think for problem 2, we can just use the result from problem 1 and let $$C$$ be the rationals.
 Did we miss something here?
And for 3 and 4, what are the difference between them? we mean if 3 is true which means we do have this function.


# Answer 


For the case $$[a,b],$$ the function $$f$$ is continuous at $$a,$$ but it may be that $$a\in C.$$ 
If $$a\not\in C $$ let $$g=f$$. 
If $$a\in C $$ let $$g(a)=-1$$ and $$g(x)=f(x)$$ for $$x\in (a,b]. $$
Then $$g$$ is continuous only on $$[a,b]$$ \ $$C.$$ 

