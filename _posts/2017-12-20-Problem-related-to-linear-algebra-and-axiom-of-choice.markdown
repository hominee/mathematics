---
layout: post
title: Problem related to linear algebra and axiom of choice
tag:
 - linear-algebra
 - functional-analysis
 - inner-product-space
 - axiom-of-choice

description: Problem related to linear algebra and axiom of choice

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Inner product on $$C(\mathbb R)$$

<!–-break-–>


With Axiom of choice it is possible to construct an inner product on $$C(\mathbb R)$$.
 
My question is, is it possible to explicitly construct an inner product on $$C(\mathbb R)$$? I.
e.
 to give a closed formular to calculate the inner product? 
we know it is straight-forward to write down a scalar product using a Hamel basis.
 This is not the answer we are  looking for.

This question came to me, when a student asked me in the lecture today 'whether there are vector spaces without inner products'.
 So we tried to find scalar produces for function spaces.
 we think we managed to write one down for $$L^1((0,1))$$.
 But we failed to construct one for $$C(\mathbb R)$$.


# Answer 


(

**Update**. Added a self-contained proof that under ZF+DC+BP there is no norm.)
Martín-Blas Pérez Pinilla is on the right track.  You can't even put a norm on $$C(\mathbb{R})$$ without using the axiom of choice in an essential way.  Dependent choice is not enough.

Claim. It is consistent with ZF+DC that there does not exist any norm on $$C(\mathbb{R})$$.

Recall that a subset $$E$$ of a topological space is said to have the Baire property if it can be written as a symmetric difference $$E = U \triangle M$$ where $$U$$ is open and $$M$$ is meager (a countable union of nowhere dense sets).  
A celebrated theorem of Shelah says that consistent with ZF+DC is the statement BP: "Every subset of $$\mathbb{R}$$ has the Baire property."  From BP it follows that in fact every subset of any Polish space has the Baire property.
Let $$\tau$$ be the usual topology on $$C(\mathbb{R})$$ (uniform convergence on compact sets).  It is induced by a translation-invariant metric:


$$

d(f,g) := \sum_{n=1}^\infty 2^{-n} \min\left(1, \sup_{[-n,n]} \|f-g\|\right) 

$$


The metric $$d$$ is complete (this comes from the fact that a uniform limit of continuous functions is continuous).  And it's not hard to see that $$\tau$$ is separable (the polynomials with rational coefficients are $$\tau$$-dense, by the Weierstrass approximation theorem).  So $$(C(\mathbb{R}),\tau)$$ is a Polish space.  
Suppose now that $$\|\cdot\|$$ is a norm on $$C(\mathbb{R})$$.  Let $$B$$ be the closed unit $$\|\cdot\|$$-ball.  We will show that $$B$$ does not have the Baire property with respect to $$\tau$$.  Specifically, let $$U$$ be any $$\tau$$-open set; we will show that $$B \triangle U$$ is $$\tau$$-nonmeager.
Suppose first that $$U = \emptyset$$ so that $$B \triangle U = B$$.  Since $$\bigcup_{n=1}^\infty nB = C(\mathbb{R})$$, by the Baire category theorem $$B$$ is $$\tau$$-nonmeager.
Now suppose that $$U$$ is nonempty.  We will show $$U \setminus B$$ is $$\tau$$-nonmeager.  Let us begin by showing $$U \setminus B$$ is nonempty.  Let $$f \in U$$ and let $$g \in C(\mathbb{R})$$ be your favorite nonzero continuous function which is supported in $$[0,1]$$.  Let $$g_n(x) = g(x-n)$$ be translates of $$g$$.  For each $$n$$, let $$a_n$$ be a real number sufficiently large that $$\|f + a_n g_n\| > 1$$, so that $$f + a_n g_n \notin B$$.  Then $$a_n g_n \to 0$$ uniformly on compact sets (i.e. in the $$\tau$$ topology), so for some $$N$$ we have $$h := f + a_N g_N \in U$$.  Thus $$h \in U \setminus B$$.  (To say this another way, every nonempty $$\tau$$-open set is unbounded, but $$B$$ is bounded, so $$U$$ cannot be a subset of $$B$$.) 
Now for any $$u \in C(\mathbb{R})$$, we have $$h + \frac{1}{n} u \to h$$ in both the $$\tau$$ and $$\|\cdot\|$$ topologies.  So for sufficiently large $$n$$, we have $$h + \frac{1}{n} u \in U$$ and $$h + \frac{1}{n} u \in B^c$$ (since $$B$$ is $$\|\cdot\|$$-closed).  That is, $$u \in n((U \setminus B)-h)$$.  Since $$u$$ was arbitrary we have shown $$\bigcup_{n=1}^\infty n((U \setminus B)-h) = C(\mathbb{R})$$.  By the Baire category theorem, $$U \setminus B$$ is $$\tau$$-nonmeager, hence so is $$B \triangle U$$.
So we have shown that if $$C(\mathbb{R})$$ has a norm, then it has a set that lacks the Baire property with respect to $$\tau$$.  Under ZF+DC+BP there is no such set and hence no norm.
(Credit where credit is due: This proof is loosely based on the idea of the proof of the Garnir-Wright closed graph theorem from Theorem 27.45 of Eric Schechter's Handbook of Analysis and its Foundations.)
Incidentally, the only property of the vector space $$C(\mathbb{R})$$ we used is that it admits a Polish topology in which every nonempty open set is unbounded.  So the same argument would apply to other vector spaces with this property, such as $$\mathbb{R}^{\mathbb{N}}$$, $$C^\infty(\mathbb{R}^d)$$, etc.

