---
layout: post
title: Problem related to real analysis
tag:
 - real-analysis

description: Problem related to real analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Existence of a map $$f: \mathbb{Z}\rightarrow \mathbb{Q}$$

<!–-break-–>


Question is to check which option holds true :
There exist a map $$f: \mathbb{Z}\rightarrow \mathbb{Q}$$ such that 

is bijective and increasing
is onto and decreasing
is bijective and satifies $$f(n)\geq 0$$ if $$n\leq 0$$
has uncountable image.

First of all any subset of $$\mathbb{Q}$$ is countable so there is no point in looking for last option.
Now, As both $$\mathbb{Z}$$ and $$\mathbb{Q}$$ are countable, there could be a possible bijective function..
Now, the first problem is i could not think of a bijection (we are  very sure this exist) and second problem is even if i find some function will that old first or third possibilities.
Please just do not give an answer but please give some hint and give some time to think about.

# Answer 


1) This cannot exist, even if we only suppose that $$f$$ is onto and increasing. Then there is an $$i$$ with 

$$f(i)<f(i+1)$$. Show that there is no $$n\in\mathbb{Z}$$ that can map to $$\frac{f(i)+f(i+1)}{2}$$.

2) $$f$$ onto and decreasing is the same as $$-f$$ onto and increasing, so by 1) this can't exist.

3) This exists. Find bijection $$g$$ from $$\mathbb{N}$$ to $$\mathbb{Q}_{> 0}$$ and try to use this in your construction. For negative integers you can define $$f(n)=g(-n)$$, for positive $$f(n)=-g(n)$$ and $$f(0)=0$$.

