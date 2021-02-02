---
layout: post
title: Which roots of irreducible quartic polynomials are constructible by compass and straightedge
tag:
 - galois-theory
 - geometric-construction

description: Which roots of irreducible quartic polynomials are constructible by compass and straightedge

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Which roots of irreducible quartic polynomials are constructible by compass and straightedge?

<!–-break-–>


A problem in Artin's Algebra, 2nd ed.
 (16.
9.
17) reads:

Determine the real numbers $$\alpha$$ of degree 4 over $$\mathbb{Q}$$ that can be constructed with ruler and compass, in terms of the Galois groups of their irreducible polynomials.


At first we thought this was a relatively simple exercise.
 In the case where the Galois group is $$C_2$$, $$V_4$$, or $$D_4$$, it has subgroups of order $$2^k$$ for each $$2^k$$ dividing its order, so the full splitting field can be constructed by successive quadratic extensions starting from $$\mathbb{Q}$$.
 However, when attempting to prove that the roots are not constructible when the Galois group is $$A_4$$ or $$S_4$$, we ran into some difficulties.

Theorem 15.
5.
6 in the book states,

Let $$p$$ be a constructible point.
 For some integer $$n$$, there is a chain of fields
  

$$

 \mathbb{Q} = F_0 \subset F_1 \subset F_2 \subset \ldots \subset F_n = K,

$$


  such that

$$K$$ is a subfield of the field of real numbers;
the coordinates of $$p$$ are in $$K$$;
for each $$i = 0, \ldots, n - 1$$, the degree $$[F_{i+1} : F_i]$$ is equal to 2.


Therefore the degree $$[K : \mathbb{Q}]$$ is a power of 2.


This theorem does not seem to be powerful enough to establish the desired nonconstructibility result for, say, a root with Galois group $$A_4$$.
 Yes, we know that $$\mathbb{Q}(\alpha)$$ in that case has no subfield that is a quadratic extension of $$\mathbb{Q}$$.
 However, this together with Theorem 15.
5.
6 is not enough, because the theorem only asserts that there is some field $$K$$ at the top of the tower, and $$K$$ is not necessarily $$\mathbb{Q}(\alpha)$$.
 In that sense, the theorem leaves open the possibility that there exists a constructible field $$K$$ that is some proper extension of $$\mathbb{Q}(\alpha)$$, and obviously $$K$$ contains some quadratic extension $$F_1$$ of $$\mathbb{Q}$$, but $$F_1$$ doesn't need to be a subfield of $$\mathbb{Q}(\alpha)$$.

If we had a stronger version of Theorem 15.
5.
6, that might read as follows:

Let $$\alpha$$ be a constructible number, and suppose $$\alpha \in K \subset \mathbb{R}$$ where $$K$$ is a field.
 Then there exists an integer $$n$$ and a tower of quadratic extensions
  

$$

 \mathbb{Q} = F_0 \subset F_1 \subset \ldots \subset F_n

$$


  such that $$p \in F_n \subset K$$.


then it seems that Exercise 16.
9.
17 would be easy to solve, but this stronger result does not seem trivial to prove.


# Answer 


What you have to check is that if $$\alpha$$ is constructible then all its  conjugates are constructible. From here, using composite fields, you should prove that $$\alpha$$ lies in a finite Galois extension of degree a power of $$2$$. 
Conversely, if a number $$\alpha$$ lies in a Galois extension of degree a power of $$2$$, it is constructible.
Therefore the constructible numbers are those for which the Galois group of their minimal polynomial is of order a power of $$2$$. 
Since you know the possiblilities for the Galois  group of an irreducible of degree $$4$$, you should have the answer. 

