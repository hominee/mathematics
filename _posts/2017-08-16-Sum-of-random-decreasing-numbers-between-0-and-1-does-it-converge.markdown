---
layout: post
title: Sum of random decreasing numbers between 0 and 1 does it converge
tag:
 - real-analysis
 - probability
 - sequences-and-series
 - convergence

description: Sum of random decreasing numbers between 0 and 1 does it converge

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Sum of random decreasing numbers between 0 and 1: does it converge??

<!–-break-–>


Let's define a sequence of numbers between 0 and 1. The first term, $$r_1$$ will be chosen uniformly randomly from $$(0, 1)$$, but now we iterate this process choosing $$r_2$$ from $$(0, r_1)$$, and so on, so $$r_3\in(0, r_2)$$, $$r_4\in(0, r_3)$$... The set of all possible sequences generated this way contains the sequence of the reciprocals of all natural numbers, which sum diverges; but it also contains all geometric sequences in which all terms are less than 1, and they all have convergent sums. The question is: does $$\sum_{n=1}^{\infty} r_n$$ converge in general? (we  think this is called almost sure convergence?) we f so, what is the distribution of the limits of all convergent series from this family?
.

# Answer 


Let $$(u_i)$$ be a sequence of i.i.d. uniform(0,1) random variables. Then the sum you are interested in can be expressed as 

 $$ 
S_n=u_1+u_1u_2+u_1u_2u_3+\cdots +u_1u_2u_3\cdots u_n.
 $$ 

The sequence $$(S_n)$$ is non-decreasing and certainly converges, possibly to $$+\infty$$.
On the other hand, taking expectations gives 

 $$ 
E(S_n)={1\over 2}+{1\over 2^2}+{1\over 2^3}+\cdots +{1\over 2^n},
 $$ 

so $$\lim_n E(S_n)=1.$$ Now by Fatou's lemma,

 $$ 
E(S_\infty)\leq \liminf_n E(S_n)=1,
 $$ 

so that $$S_\infty$$ has finite expectation and so is finite almost surely.

