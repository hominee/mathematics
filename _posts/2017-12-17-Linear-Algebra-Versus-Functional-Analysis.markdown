---
layout: post
title: Linear Algebra Versus Functional Analysis
tag:
 - linear-algebra
 - functional-analysis

description: Linear Algebra Versus Functional Analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Linear Algebra Versus Functional Analysis

<!–-break-–>


As it is mentioned in the answer by Sheldon Axler in this post, we usually  restrict linear algebra to finite dimensional linear spaces and study the infinite dimensional ones in functional analysis.
 
we are  wondering that what are those parts of the theory in linear algebra that restrict it to finite dimensions.
 To clarify myself, here is the main question

Question.

  What are the main theorems in linear algebra that are just valid for finite dimensional linear spaces and are propagated in the sequel of theory, used to prove the following theorems?

Please note that we want to know the main theorems that are just valid for finite dimensions not all of them.
 By main, we mean the minimum number of theorems of this kind such that all other such theorems can be concluded from these.


# Answer 


In finite-dimensional spaces, the main theorem is the one that leads to the definition of dimension itself: that any two bases have the same number of vectors.  All the others (e.g., reducing a quadratic form to a sum of squares) rest on this one.
In infinite-dimensional spaces, (1) the linearity of an operator generally does not imply continuity (boundedness), and, for normed spaces, (2) "closed and bounded" does not imply "compact" and (3) a vector space need not be isomorphic to its dual space via canonical isomorphism. 
Furthermore, in infinite-dimensional vector spaces there is no natural definition of a volume form.
That's why Halmos's Finite-Dimensional Vector Spaces is probably the best book on the subject: he was a functional analyst and taught finite-dimensional while thinking infinite-dimensional.

