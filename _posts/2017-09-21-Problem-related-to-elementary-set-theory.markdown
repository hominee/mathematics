---
layout: post
title: Problem related to elementary set theory
tag:
 - elementary-set-theory

description: Problem related to elementary set theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Bijective map from $$\Bbb Z$$ to $$\Bbb Q$$

<!–-break-–>


There  exists  a  map $$f: \Bbb Z\rightarrow \Bbb Q $$  such  that  $$f$$  is 
A. Bijective  and  increasing
B. Onto  and  decreasing
C. Bijective  and  satisfies  $$f(n)\ge 0$$  if $$n\le 0$$
D. Has  uncountable images
Now  option  D.  is  absurd . Option  C.  is  given  to  be  the  correct  answer.we  was  thinking  since  both  sets  are  countable  bijection  is  obvious. Now  why  cannot  be  increasing  ? we  could  map  $$0$$  to  $$0$$  and  the  negative  integers  to the  negative  rationals and  positive  integers  to  the  positive  rationals. And  if  increasing  would  be  possible  just  interchanging signs  would  give  the  decreasing  map. So  none  is  possible  but  why?
.

# Answer 


The problem is that, while the cardinality of $$\mathbb{Z}$$ and $$\mathbb{Q}$$ is the same, the topology is different.  Consider the following: Given two integers $$a$$ and $$b$$ with $$a < b$$, can we say how many integers $$c$$ satisfy $$a < c < b$$?  Now ask the same question for the rational numbers.
This leads to problems.  For example, lets say $$a$$ and $$b$$ are two such integers with $$k$$ other integers between them.  And we can even assume the $$f(a) = r_{1} < r_{2} = f(b)$$.  But now we can find an increasing sequence of$$k+1$$ rational numbers (at least) between $$r_{1}$$ and $$r_{2}$$, and only $$k$$ potential integers to use as their preimages.

