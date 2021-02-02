---
layout: post
title: Problem related to real analysis and elementary set theory
tag:
 - real-analysis
 - functions
 - elementary-set-theory

description: Problem related to real analysis and elementary set theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to define a bijection between $$(0,1)$$ and $$(0,1]$$?

<!–-break-–>



How to define a bijection between $$(0,1)$$ and $$(0,1]$$?
  Or any other open and closed intervals?

we f the intervals are both open like $$(-1,2)\text{ and }(-5,4)$$ we  do a cheap trick (don't know if that's how you're supposed to do it):
we  make a function $$f : (-1, 2)\rightarrow (-5, 4)$$ of the form $$f(x)=mx+b$$ by
\begin{align*}
-5 = f(-1) &= m(-1)+b \\
4 = f(2) &= m(2) + b
\end{align*}
Solving for $$m$$ and $$b$$ we  find $$m=3\text{ and }b=-2$$ so then $$f(x)=3x-2.$$
Then we  show that $$f$$ is a bijection by showing that it is injective and surjective.

# Answer 


Choose an infinite sequence $$(x_n)_{n\geqslant1}$$ of distinct elements of $$(0,1)$$. Let $$X=\{x_n\mid n\geqslant1\}$$, hence $$X\subset(0,1)$$. Let $$x_0=1$$. Define $$f(x_n)=x_{n+1}$$ for every $$n\geqslant0$$ and $$f(x)=x$$ for every $$x$$ in $$(0,1)\setminus X$$. Then $$f$$ is defined on $$(0,1]$$ and the map $$f:(0,1]\to(0,1)$$ is bijective.
To sum up, one extracts a copy of $$\mathbb N$$ from $$(0,1)$$ and one uses the fact that the map $$n\mapsto n+1$$ is a bijection between $$\mathbb N\cup\{0\}$$ and $$\mathbb N$$.

