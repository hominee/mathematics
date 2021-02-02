---
layout: post
title: Problem related to elementary set theory and cardinals
tag:
 - elementary-set-theory
 - cardinals

description: Problem related to elementary set theory and cardinals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Does $$\mathbb R^2$$ contain more numbers than $$\mathbb R^1$$? 

<!–-break-–>



Possible Duplicate:
bijective map from $$\mathbb{R}^3\rightarrow \mathbb{R}$$

Do the real numbers and the complex numbers have the same cardinality? 

Does $$\mathbb R^2$$ contain more numbers than $$\mathbb R^1$$? we know that there are the same number of even integers as integers, but those are both countable sets. Does the same type of argument apply to uncountable sets? If there exists a 1-1 mapping from $$\mathbb R^2$$ to $$\mathbb R^1$$, would that mean that 2 real-valued parameters could be encoded as a single real-valued parameter?


# Answer 


Indeed $$\mathbb R^2$$ has the same cardinality as $$\mathbb R$$, as the answers in this thread show.

And indeed it means that functions of two variables can be encoded as functions of one variable. 
However do note that such encoding cannot be continuous, but can be measurable.

Lastly, to extend this result to all infinite sets one needs the axiom of choice. In fact the assertion "For every infinite $$A$$ there is a bijection between $$A$$ and $$A^2$$" is equivalent to the axiom of choice. If one requires that $$A$$ is well-ordered then this is true without the axiom of choice, but for many "sets of interest" (e.g. the real numbers) one cannot prove the existence of a well-ordering without some form of choice.

Despite the last sentence, the existence of a bijection between $$\mathbb R$$ and $$\mathbb R^n$$ does not require the axiom of choice (for $$n>0$$, of course).

