---
layout: post
title: Difference between metric and norm made concrete The case of Euclid
tag:
 - vector-spaces
 - norm
 - metric-spaces
 - normed-spaces

description: Difference between metric and norm made concrete The case of Euclid

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Difference between metric and norm made concrete: The case of Euclid

<!–-break-–>


This is a follow-up question on this one.

This time we are  making things more concrete: we are  esp.
 interested in the difference between a metric and a norm.
 we understand that the metric gives the distance between two points as a real number.
 The norm gives the length of a a vector as a real number (see def.
 e.
g.
 here).
 we further understand that all normed spaces are metric spaces (for a norm induces a metric) but not the other way around (please correct me if we are  wrong).

Here we are  only talking about vector spaces.
 As an example lets talk about Euclidean distance and Euclidean norm.
 Wikipedia says:

A vector can be described as a
  directed line segment from the origin
  of the Euclidean space (vector tail),
  to a point in that space (vector tip).

  If we consider that its length is
  actually the distance from its tail to
  its tip, it becomes clear that the
  Euclidean norm of a vector is just a
  special case of Euclidean distance:
  the Euclidean distance between its
  tail and its tip.


What confuses me is that they seem to be having it backwards: The Euclidean metric induces the Euclidean norm: You measure the distance between tip and tail and get the length out of that.
 What makes my confusion complete is that $$L^2$$ distance is also called the Euclidean norm (see here).

we would very much appreciate it if somebody could clear the haze.


# Answer 


The metric $$d(u,v)$$ induced by a vector space norm has additional properties that are not true of general metrics. These are:
Translation Invariance: $$d(u+w,v+w)=d(u,v)$$
Scaling Property: For any real number $$t$$, $$d(tu,tv)=\|t\|d(u,v)$$.
Conversely, if a metric has the above properties, then $$d(u,0)$$ is a norm.
More informally, the metric induced by a norm "plays nicely" with the vector space structure.  The usual metric on $$\mathbb{R}^n$$ has the two properties mentioned above.  But there are metrics on $$\mathbb{R}^n$$ that are topologically equivalent to the usual metric, but not translation invariant, and so are not induced by a norm.

