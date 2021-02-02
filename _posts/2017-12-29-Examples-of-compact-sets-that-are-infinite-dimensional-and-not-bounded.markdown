---
layout: post
title: Examples of compact sets that are infinite dimensional and not bounded
tag:
 - functional-analysis
 - banach-spaces
 - compactness
 - examples-counterexamples
 - normed-spaces

description: Examples of compact sets that are infinite dimensional and not bounded

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Examples of compact sets that are infinite dimensional and not bounded

<!–-break-–>


In an infinite dimensional Banach space, does a compact subset have to be finite dimensional? we know it cannot contain any infinite dimensional balls, if this mean it has to be finite dimensional, then why do we sometimes see phrases like "for any compact subspaces of some vector space"?
Also, do compact sets in infinite dimensional Banach spaces have to be bounded?
Is there a general result that tells us what compact subsets of infinite dimensional vector spaces look like?
Thanks so much!
.


# Answer 



A compact set in a metric space must be bounded. Otherwise we can take $$\{ x_n \}_{n=1}^\infty$$ and a fixed point $$x_0$$ such that $$d(x_n,x_0) \geq n$$. This will have no convergent subsequence, which we can prove by showing that it has no Cauchy subsequence. 
A compact set in a metric space (also in a Hausdorff space) must be closed. Otherwise we can pick a sequence which converges to a point in the closure which is not in the set. This will have no convergent subsequence (within the set, at least).
A closed and bounded set in a metric space need not be compact. In an infinite dimensional Banach space, closed balls are not compact. For example, in $$\ell^p$$, $$\{ e_1,e_2,\dots,e_n,\dots \}$$ is a sequence in the closed unit ball which has no convergent subsequence. In an infinite dimensional Hilbert space we can essentially copy this example by finding an orthonormal sequence. The result holds in any infinite dimensional Banach space, but the details of the construction are not quite so trivial.
A compact subset of an infinite dimensional Banach space can be infinite dimensional, in the sense that it is not contained in any finite dimensional subspace. One way to generate infinite dimensional compact sets is to ensure that any sequence of linearly independent vectors converges to zero. So for example, if $$X=\ell^p$$, consider the set $$\{ 0,e_1,e_2/2,\dots, e_n/n,\dots \}$$. This is clearly infinite dimensional, but it is also compact, since any sequence in this set either converges to $$0$$ or has a constant subsequence.
In general, a subset $$A$$ of a metric space $$X$$ is compact if and only if it is complete and totally bounded. A subset of a metric space is totally bounded if for any $$\varepsilon > 0$$ there exists $$N \in \mathbb{N}$$ and points $$x_1,\dots,x_N$$ such that $$A \subset \bigcup_{n=1}^N B(x_n,\varepsilon)$$. In a Banach space $$X$$, this is equivalent to saying that it is bounded and, for every $$\varepsilon > 0$$ there exists $$N \in \mathbb{N}$$ and a subspace $$V$$ of $$X$$ whose dimension is $$N$$ such that $$(\forall x \in A) \, d(x,V) < \varepsilon$$.


