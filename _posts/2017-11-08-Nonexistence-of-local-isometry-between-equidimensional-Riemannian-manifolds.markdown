---
layout: post
title: Nonexistence of local isometry between equidimensional Riemannian manifolds
tag:
 - differential-geometry
 - riemannian-geometry
 - inner-product-space
 - isometry

description: Nonexistence of local isometry between equidimensional Riemannian manifolds

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Nonexistence of local isometry between equidimensional Riemannian manifolds

<!–-break-–>


Recall that all inner product spaces of the same dimension are isometric.

For example, if $$(M,\mathrm{g})$$ and $$(N,\mathrm{h})$$ are Riemannian manifolds of the same dimension, then $$(T_pM,\mathrm{g}_p)$$ and $$(T_qN,\mathrm{h}_q)$$ are isometric inner product spaces.
 Let $$\beta:T_pM\to T_qN$$ be a (linear) isometry.


Question: Why isn't $$\exp_q\!\circ\,\beta\circ\exp_p^{-1}$$ a local isometry wherever it is defined?

To clarify, we know that it isn't a local isometry, at least in general.
 If it was, then I'd have a local isometry between neighborhoods of every point on each equidimensional Riemannian manifold, which is clearly absurd.
 we are  looking for an explanation as to why this composition is not a local isometry.
 we are  not looking for a counterexample.

we think my mental impasse comes from Gauss' lemma, but we are  not sure.
 Using the chain rule, shouldn't $$\exp_{q*}\!\circ\,\beta\circ\exp_{p*}^{-1}$$, as a composition of linear isometries, itself be a linear isometry?
.


# Answer 


The differential is an isometry of vector spaces. The local map between Manifolds is a radial isometry, but in general it will fail to map geodesic distance spheres from the base point to isometric distance spheres. Simply because these need not admit an isometry. So a path orthogonal to geodesic rays starting in the base points will be mapped onto a path with different length.
Just map a hyperbolic geodesic ball around some point to a Euclidean on in standard models, or to a spheric one. (Recall spheric trigonometry)...


**Edit**: actually this can be made much more precise and to some extent even quantified. If you want to learn more about the topic search for 'Comparison theorems in Riemannian Geometry'. The classic is Cheeger, Ebin (with exactly that keyword as title), which was quite an eye opener for me. Another key word is 'Jacobi fields', these are the vector fields which describe the tangent distortions (and are the objects which are investigate in the study of comparison theorems).

