---
layout: post
title: Topologically, is there a definition of differentiability that is dependent on the underlying topology, similar to continuity
tag:
 - real-analysis
 - general-topology
 - derivatives
 - continuity
 - differential-topology

description: Topologically, is there a definition of differentiability that is dependent on the underlying topology, similar to continuity

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Topologically, is there a definition of differentiability that is dependent on the underlying topology, similar to continuity?

<!–-break-–>


we are  studying Analysis on Manifolds by Munkres, and at page 199, it is given that 

Let $$S$$ be a subset of $$\mathbb{R}^k$$; let $$f: S \to \mathbb{R}^n$$.
 We
  say that $$f$$ is of class $$C^r$$, on $$S$$ if $$f$$ may be extended to a
  function $$g: U \to \mathbb{R}^n$$ that is of class $$C^r$$ on an open set
  $$U$$ of $$\mathbb{R}^k$$ containing $$S$$.


It is clear from this definition that, even if we were working on a subspace $$M$$ of $$\mathbb{R}^n$$ (or on the set $$M$$ with different topology other subspace topology), we still consider the opens sets of $$M$$ as a subset of $$\mathbb{R}^n$$, and show the differentiability according to that.

However, for example, if we were to show the continuity of a function $$f : \mathbb{R}^k \to M$$, we would consider open sets of $$M$$, as open sets of $$M$$, i.
e not $$\mathbb{R}^n$$.
 In this sense, the continuity of a function is depends on the topology of the domain & codomain of that function, whereas the differentiability does not, as far as we have seen.

So my question is that, is there any definition of differentiability that is dependent on the underlying topologies of domain & codomain ?
Clarification 
For example, normally, for $$f: A \to \mathbb{R}^m$$, the concept differentiability is defined for $$x \in Int(A)$$, but the very definition of interior needs the definition of what we mean by an open set, which is dependent on the underlying topology, so say (trivially) $$A = \{1,2\}$$, then with the discrete topology both $$1,2 \in Int(A)$$, but can we define differentiability in this space ?
Or let say, $$A = (0,1]$$ as a subspace of $$[0,1]$$ with the standard topology (subspace topology inherited from $$\mathbb{R}$$).
Now if we consider our bigger space as $$[0,1]$$, then we should be able to define differentiability at $$x = 1$$ because $$(0,1]$$ is open in $$[0,1]$$, hence $$1\in Int[0,1]$$.


# Answer 


The notion of differentiability is not involving only a topology but a normed space. And in $$\mathbb R^m$$ all the norms are equivalent.
Therefore the topology used in the definition of differentiability is the one induced by the norm. This topology is unique in $$\mathbb R^n$$. This maybe different in infinite dimensional Banach spaces.
Finally, there is only one relative topology on a subset $$S \subseteq \mathbb R^m$$ induced by the « normed topology » of $$\mathbb R^m$$.

