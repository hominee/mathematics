---
layout: post
title: Is there a general way to tell whether two topological spaces are homeomorphic
tag:
 - general-topology
 - algebraic-topology
 - category-theory

description: Is there a general way to tell whether two topological spaces are homeomorphic

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is there a general way to tell whether two topological spaces are homeomorphic?

<!–-break-–>


We know that if two topological spaces $$X$$ and $$Y$$ are homeomorphic, then they have the same fundamental groups, and the same homology.
 In other words, we have functors


$$

\pi_1 : \mathsf{Top} \to \mathsf{Grp} \quad\text{and}\quad H_n : \mathsf{Top} \to \mathsf{Ab}

$$


(actually this works even if the spaces are homotopy equivalent).
 The important thing here is that these functors can be used to prove that the two spaces are not homeomorphic: for instance $$H_3(S^3) \cong \Bbb Z \not\cong 0 = H_3(S^2)$$, so that $$S^3$$ and $$S^2$$ are not homeomorphic (they don't even have the same homotopy type).

we was wondering whether there was somehow a "converse" to this, i.
e.
 is they a way to prove that two topological spaces are homeomorphic.

More precisely:

Is there a category $$\scr C$$ and a functor $$\mathsf F : \mathsf{Top} \to \mathscr C$$ such that $$\mathsf F(X) \cong \mathsf F(Y) \implies X \cong Y$$ ? Of course, we want to avoid obvious examples as $$\mathsf{Id_{Top}}$$ .


(By the way, we don't know if there is a name for such functors, which are injective on objects.
 Faithful is already used for something different).
 we would also accept discussing the case where the homeomorphism $$ X \cong Y$$ is replaced by a homotopy equivalence $$X \simeq Y$$.

Trying the functor $$\mathsf F(X) = X \times X$$ doesn't work, as shown here.
 The functor $$\mathsf F(X) = X \sqcup X$$doesn't work as well.

The closest result we found is a theorem due to Gelfand and Kolmogorov : given two compact and Hausdorff spaces, if the commutative rings $$C(X)$$ and $$C(Y)$$ of continuous functions $$f\,:\,X,Y\rightarrow \mathbb{R}$$ (under pointwise addition and multiplication) are isomorphic, then $$X$$ and $$Y$$ are homeomorphic.
 Maybe we could try to generalize this to the category of locally compact and Hausdorff spaces, using the Alexandorff compactification.


# Answer 


No, at least in the sense that there are no such functors $$F$$ which are substantially more approachable than the original problem. There are very few general techniques for distinguishing homotopy equivalent, non-homeomorphic spaces: see the following link for work in the last twelve years distinguishing some such pairs of 3-dimensional closed manifolds, which are a ludicrously tiny tip of the iceberg of arbitrary spaces. It's worth noting here, to give a sense of how far from possible a simple, complete homeomorphism invariant is, that even the homotopy equivalence problem runs into uncomputability, insofar as it's undecidable whether two spaces have the same fundamental group, given presentations of those groups.
https://mathoverflow.net/questions/242748/list-of-invariants-that-distinguish-homotopy-equivalent-non-homeomorphic-spaces

