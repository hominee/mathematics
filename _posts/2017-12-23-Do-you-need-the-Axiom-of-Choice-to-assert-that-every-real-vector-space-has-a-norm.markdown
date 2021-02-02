---
layout: post
title: Do you need the Axiom of Choice to assert that every real vector space has a norm
tag:
 - logic
 - vector-spaces
 - axiom-of-choice

description: Do you need the Axiom of Choice to assert that every real vector space has a norm

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Do you need the Axiom of Choice to assert that every real vector space has a norm?

<!–-break-–>


Math people:
This question is 95% answered (the first answer) at Does every $$\mathbb{R},\mathbb{C}$$ vector space have a norm? and Vector Spaces and AC .
  The questions, answers, and links found there seem to assert that if you assume the Axiom of Choice, then every vector space has a Hamel basis and hence a norm, and conversely, if you assume every vector space has Hamel basis, then AC follows.

But a norm doesn't have to be given by a Hamel basis.
  For example, on $$L^2([0,1])$$ you can use the standard norm, which we don't think can be defined using a Hamel basis, though it can be defined using a Schauder basis.
  So we think the question is still open.



**Edit**: we want the underlying field to be the real numbers.

Stefan (STack Exchange FAN)
.


# Answer 


It is consistent that the axiom of choice fails and there is a vector space over the real numbers which cannot be a topological vector space in a nontrivial way, and in particular it means that it cannot be normed, since the norm would induce a nontrivial topology. 
The construction is due to Läuchli, from 1963 (and the extension to real vector spaces follows from my masters thesis). 
The more interesting question is whether the assertion "every vector space has a norm" implies the axiom of choice. The answer to that, we do not know at this time. 

