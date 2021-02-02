---
layout: post
title: Is a linearly independent set whose span is dense a Schauder basis
tag:
 - linear-algebra
 - functional-analysis
 - banach-spaces
 - normed-spaces
 - schauder-basis

description: Is a linearly independent set whose span is dense a Schauder basis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is a linearly independent set whose span is dense a Schauder basis?

<!–-break-–>


If $$X$$ is a Banach space, then a Schauder basis of $$X$$ is a subset $$B$$ of $$X$$ such that every element of $$X$$ can be written uniquely as an infinite linear combination of elements of $$B$$.
  My question is, if $$A$$ is a linearly independent subset of $$X$$ such that the closure of the span of $$A$$ equals $$X$$, then is $$A$$ necessarily a Schauder basis of $$X$$?
If not, does anyone know of any counterexamples?
.


# Answer 


No, certainly not.  The linearly independent set $$\{1, x, x^2, x^3, \dots\}$$ has span dense in $$C[0,1]$$ by the Weierstrass approximation theorem. But it is not a Schauder basis of that space, since not every continuous function is given by a power series.
A Schauder basis is, in general, much harder to construct than a set with dense span.  
Since Enflo we know that there are separable Banach spaces (hence they have countable dense subset) that have no Schauder basis at all.

