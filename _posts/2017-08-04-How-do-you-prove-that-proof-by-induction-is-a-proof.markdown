---
layout: post
title: How do you prove that proof by induction is a proof
tag:
 - induction

description: How do you prove that proof by induction is a proof

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How do you prove that proof by induction is a proof?

<!–-break-–>


Are proofs by induction limited to cases where there is an explicit dependance on a integer, like sums? we  cannot grasp the idea of induction being a proof in less explicit cases.

# Answer 


The title suggests puzzlement about the very idea of a proof by induction (maybe we are  misconstruing the question). Anyway, let's take the simplest case, where we want to show that all natural numbers have some property $$P.$$ We obviously can't give separate proofs, one for each $$n$$,  that $$n$$ has $$P$$, because that would be a never-ending task. So how can we proceed? 
Suppose we can show that (i) $$0$$ has some property $$P$$, and also that (ii) if any given number has the property $$P$$ then so does the next: then we can infer that all numbers have  property $$P$$. Using $$\varphi$$ for an expression attributing some property to numbers, we can put the principle like this: 

Given 

(i) $$\varphi(0)$$, 

and 

(ii) $$\forall n(\varphi(n) \to \varphi(n +
    1))$$, 
	
we can infer $$\forall n\varphi(n)$$.

And the headline question seems to be: Why are arguments which appeal to this sort of principle good arguments? 
Well, suppose we establish both the base case (i) and the induction step (ii). By (i) we have $$\varphi(0)$$. By (ii), $$\varphi(0)  \to \varphi(1)$$. Hence we can infer $$\varphi(1)$$. By (ii) again, $$\varphi(1)  \to \varphi(2)$$. Hence we can now infer $$\varphi(2)$$. Likewise, we can use another instance of (ii) to infer $$\varphi(3)$$. And so on and so forth, running as far as we like through the successors of $$0$$ (i.e. through the numbers that can be reached by starting from zero and repeatedly adding one). But the successors of $$0$$ are the only natural numbers. So for every natural number $$n$$, $$\varphi(n)$$. 

The arithmetical induction principle is underwritten, then, by the basic structure of the number sequence, and in particular by the absence of 'stray' numbers that you can't get to step-by-step from zero by applying and reapplying the successor function.

So much for the simplest case. But the principles underlying fancier inductive arguments (not over numbers but e.g structural inductions or transfinite inductions) are similar enough to become clear if you are really clear about this simple case. The crucial thing, in each case, will be to find an appropriate induction step which tells that a certain property gets passed down from 'predecessors' to 'successors', and so ripples through the whole of the relevant domain.

