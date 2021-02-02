---
layout: post
title: Is there any (nontrivial) constructible rational angle
tag:
 - geometry
 - geometric-construction

description: Is there any (nontrivial) constructible rational angle

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is there any (nontrivial) constructible rational angle?

<!–-break-–>


Yesterday, we talked with a friend about a problem where the solution would be an angle of $$2$$ radians (about $$114.
6°$$).
 Then somehow the question arose whether such an angle would be constructible (with straight edge and compass), and it looks like no - but we had not suddenly an idea on how to prove it either way.

The "easily" constructible angles (e.
g.
 the ones for which we would know how to construct them without long thinking) are some rational multiples of $$\pi$$: We know that we can half each angle, and also construct sums and differences of angles, and we have angles of $$\frac\pi3$$ and $$\frac\pi2$$ to start with.
 (Then there are some more from some constructible regular polygons).

Wikipedia says:

[.
.
.
] The angles that are constructible form an abelian group under
  addition modulo $$2\pi$$ ([.
.
.
]).
 The angles that are constructible are
  exactly those whose tangent (or equivalently, sine or cosine) is
  constructible as a number.
 [.
.
.
]

It looks like we don't know enough about these functions to utilize this information.


The only angles of finite order that may be constructed starting
  with two points are those whose order is either a power of two,
  or a product of a power of two and a set of distinct Fermat primes.


Okay, these are the mentioned rational multiples of $$\pi$$.


In addition there is a dense set of constructible angles of infinite order.


All rational angles are angles of infinite order, thus if any would be constructible, it would be in this category.
 And of course, if we had any rational angle, we would get quite a lot other ones from halving and addition.

My question: Is there any rational angle $$\alpha \in \mathbb Q \setminus\{0\}$$ which is constructible, or is there a proof that no such angle exists?
If there are no rational ones, maybe any algebraic one?
.


# Answer 


An angle is constructible if and only if the cosine of the angle is a constructible distance.  In particular, if $$\theta$$ is constructible then $$\cos\theta$$ must be an algebraic number (or more specifically a constructible number).  By the Lindemann-Weierstrass Theorem, this can only occur if $$\theta$$ is transcendental.  Thus no nonzero algebraic angle is constructible.

