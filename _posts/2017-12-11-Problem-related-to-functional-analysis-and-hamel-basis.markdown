---
layout: post
title: Problem related to functional analysis and hamel basis
tag:
 - functional-analysis
 - banach-spaces
 - lp-spaces
 - axiom-of-choice
 - hamel-basis

description: Problem related to functional analysis and hamel basis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A Hamel basis for $$\ell^p$$?

<!–-break-–>


we are  looking for an explicit example for a Hamel basis for  $$\ell^{p}$$?.
 As we know that for a Banach space a Hamel basis has either finite or uncountably infinite cardinality and for such a basis one can express any element of the vector space as a finite linear combination of these.
 After some trying we could not write one explicitly.
 A quick google search did not reveal anything useful except for the proof of uncountability of a an infinite Hamel basis.
 Maybe we are  being a bit silly but we don't think the answer is as obvious as for a Schauder basis for the same case.

So, what is an explicit example for a Hamel basis for $$\ell^{p}$$??
.


# Answer 


The existence of a Hamel basis for $$\ell^p$$ cannot be proved without some of the axiom of choice, which in modern terms usually means that we cannot write it explicitly.
It is consistent with ZF+DC (a weak form of the axiom of choice which is sufficient to do a lot of the usual mathematics) that all sets of real numbers have Baire property, and in such model we have that every linear function from $$\ell^p$$ to itself is continuous.
It is also true (in ZF) that $$\ell^p$$ is separable for $$1\leq p<\infty$$. It is a known fact that continuous endomorphisms are determined completely by the countable dense set.
If there exists a Hamel basis then its cardinality is at least $$\frak c$$ (or rather exactly that), and therefore it has $$2^\frak c$$ many permutations, each extends uniquely to a linear automorphism, which is continuous.
Now, note that $$\ell^p$$ has size $$\leq\frak c$$ itself, since it is a separable metric space (and again, this is in fact $$\frak c$$) and therefore it has only $$\frak c$$ many continuous endomorphisms.
Cantor's theorem tells us that $$2^\frak c\neq c$$, and therefore in Shelah's model where every set of real numbers have the Baire property there is no Hamel basis for $$\ell^p$$.

