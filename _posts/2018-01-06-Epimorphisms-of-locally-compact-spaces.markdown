---
layout: post
title: Epimorphisms of locally compact spaces
tag:
 - general-topology
 - category-theory
 - compactness
 - operator-algebras

description: Epimorphisms of locally compact spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Epimorphisms of locally compact spaces

<!–-break-–>


Let $$LCH$$ be the category of locally compact Hausdorff spaces with proper continuous maps.

Question.
 What are the epimorphisms in $$LCH$$?
we suspect them to be surjective, but we haven't been able to prove it.

Here is an idea: Let $$f : X \to Y$$ be an epimorphism.
 The image $$f(X)$$ is closed.
 It follows that $$f(X)^+$$ is closed in $$Y^+$$, where $$+$$ denotes the Alexandrov compactification.
 If $$y \in Y \setminus f(X)$$, by Urysohn's Lemma there is some $$g \in C(Y^+)$$ with $$g(y)=1$$ and $$g(f(X)^+)=0$$.
 Now, $$g(\infty)=0$$ implies that $$g$$ restricts to some $$g \in C_0(Y)$$ such that $$g(y)=1$$ and $$g(f(X))=0$$.
 The remaining problem is that $$g$$ might be not proper.

we have also tried to prove it in the dual category, which is the category $$CommC^*Alg$$ of commutative $$C^*$$-algebras with non-degenerate $$*$$-homomorphisms.
 we already know that surjections become injections under this duality, so that the question would be: Is every monomorphism in $$CommC^*Alg$$ injective? Again, the restrictive morphisms cause some problems in proving this.


# Answer 


Yes, a morphism in this category is epic iff it is surjective. Obviously
surjective morphisms are epic, so it suffices to show that if $$f: X\to Y$$
is not surjective, there is a locally compact Hausdorff space $$Z$$ and distinct $$g_1, g_2 \in \hom(Y,Z)$$ such that $$g_1 \circ f = g_2 \circ f$$.
we will use the notion of a perfect map as defined in Engelking's General Topology, which is a continuous closed map from a Hausdorff space to 
a topological space with compact fibres. With this definition, perfect maps
are proper (thm. 3.7.2) and compositions of perfect maps are perfect. (cor 3.7.3)
In fact, a map from a Hausdorff space to a compactly generated Hausdorff space is 
perfect iff it is continuous and proper. (thm. 3.7.18)

On the product $$Y \times 2$$ define the equivalence relation $$E$$ such that
$$(x, i) \,E\, (y, j)$$ iff $$x = y$$ and ($$i = j$$ or $$x \in f(X)$$). (In 
other words: glue the two copies of $$f(X)$$ together). 

Let $$Z = (Y \times 2)/E$$ and $$q: Y \times 2 \to Z$$ the natural map. Since the fibres of $$q$$ are finite they are compact and, using the fact that $$f(X)$$ is closed, it is easy to verify that if $$F$$ is closed in $$Y \times 2$$, so is $$q^{-1}(q(F))$$. Hence $$q$$ is perfect and since perfect images of locally compact
Hausdorff spaces are also locally compact Hausdorff (thm. 3.7.20, 3.7.21), $$q$$ is a morphism.

If we now take $$g_1$$ and $$g_2$$ to be the compositions of $$q$$ with the 
two natural embeddings $$Y \to Y \times 2$$, we find they differ on $$Y\setminus f(X)$$, but agree on $$f(X)$$,
 therefore $$ g_1 \circ f = g_2 \circ f$$.

