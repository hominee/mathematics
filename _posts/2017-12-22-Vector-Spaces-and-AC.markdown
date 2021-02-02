---
layout: post
title: Vector Spaces and AC
tag:
 - linear-algebra
 - vector-spaces
 - axiom-of-choice
 - hamel-basis

description: Vector Spaces and AC

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Vector Spaces and AC

<!–-break-–>


we know that the proof that every vector space has a basis uses the Axiom of Choice, or Zorn's Lemma.
 If we consider an axiom system without the Axiom of Choice, are there vector spaces that provably have no basis?
.


# Answer 


If you only consider a system without the axiom of choice you cannot prove that there is such vector space, simply because while you are not assuming AC -- it might still be true.
However Andreas Blass proved in 1984 that if every vector space has a basis then the axiom of choice holds [1]. In particular it means that if you assume the axiom of choice fails then there is provably a space without a basis.

Semi-constructively, the proof given by Blass uses the equivalence (in ZF) between the axiom of choice the axiom of multiple choice.

The axiom of multiple choice (AMC) asserts that given a family $$\cal A$$ of non-empty sets, such that every $$A\in\cal A$$ has at least two elements, then there is a function $$F$$ such that $$F(A)$$ is a non-empty, finite, proper subset of $$A$$ for all $$A\in\cal A$$.

Blass used this equivalence as follows: given a family of non-empty sets he defines a vector space using this family and by the existence of a basis he constructs $$F$$ showing that AMC holds.
If we assume the axiom of choice fails, then also AMC fails in this model. Therefore there is a family of sets each containing at least two elements, but there is no $$F$$ as required. Using this family we can construct the same vector space, but now we can prove that it has no basis. If it had a basis then Blass' proof would follow and a contradiction would be found.


**Note** that this is semi-constructive since we cannot constructively point out a family of non-empty sets without a choice function, simply because it is consistent that there is none of those. However if we assume that the axiom of choice fails, then we can only infer that such family exists, give it a name and move along. For more see [2]. 
We can assume "anti-choice" axioms which also tell us particular sets cannot be well-ordered (or families without choice functions), for example we may assume that the real numbers cannot be well-ordered or even a stronger assumption: we can directly assume that the real numbers do not have a basis over $$\mathbb Q$$. Such assumptions are indeed consistent with ZF, but they are "focused" versions of the negation of the axiom of choice, they tell us a lot about how it fails.

Bibliography:

Andreas Blass, Existence of bases implies the axiom of choice. Contemporary Mathematics vol. 31 pp. 31-33, 1984.
Asaf Karagila, Which set is unwell-orderable? Mathematics StackExchange, Sep. 2012.


