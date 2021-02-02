---
layout: post
title: Are commutative C-algebras really dual to locally compact Hausdorff spaces
tag:
 - general-topology
 - functional-analysis
 - operator-algebras

description: Are commutative C-algebras really dual to locally compact Hausdorff spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Are commutative C*-algebras really dual to locally compact Hausdorff spaces?

<!–-break-–>


Several online sources (e.
g.
 Wikipedia, the nLab) assert that the Gelfand representation defines a contravariant equivalence from the category of (non-unital) commutative $$C^{\ast}$$-algebras to the category of locally compact Hausdorff (LCH) spaces.
 This seems wrong to me.
 
The naive choice is to take all continuous maps between LCH spaces.
 This doesn't work.
 For example, the constant map $$\mathbb{R} \to \bullet$$ does not come from a morphism $$\mathbb{C} \to C_0(\mathbb{R})$$, the problem being that composing with the map $$\bullet \to \mathbb{C}$$ sending $$\bullet$$ to $$1$$ gives a function on $$\mathbb{R}$$ which doesn't vanish at infinity.
 It is necessary for us to restrict our attention to proper maps.

But this still doesn't work.
 If $$A, B$$ are any commutative $$C^{\ast}$$-algebras we can consider the morphism


$$

A \ni a \mapsto (a, 0) \in A \times B.


$$


This morphism does not define a map on Gelfand spectra; if $$\lambda : A \times B \to \mathbb{C}$$ is a character factoring through the projection $$A \times B \to B$$, then composing with the above morphism gives the zero map $$A \to \mathbb{C}$$.
 This contradicts the nLab's claim that taking Gelfand spectra gives a functor into locally compact Hausdorff spaces (if one requires that the morphisms are defined everywhere on the latter category).
 
The correct statement appears to be that commutative $$C^{\ast}$$-algebras are contravariantly equivalent to the category $$\text{CHaus}_{\bullet}$$ of pointed compact Hausdorff spaces; the functor takes an algebra to the Gelfand spectrum of its unitization (we adjoin a unit whether or not the algebra already had one).
 There is an inclusion of the category of LCH spaces and proper maps into this category but it is not an equivalence because maps $$(C, \bullet) \to (D, \bullet)$$ in $$\text{CHaus}_{\bullet}$$ may send points other than the distinguished point of $$C$$ to the distinguished point of $$D$$.
 
So do sources mean something else when they claim the equivalence with locally compact Hausdorff spaces? 
.


# Answer 


It is true that the category of locally compact Hausdorff spaces is equivalent to the category of commutative $$C^*$$-algebras . . . with appropriately chosen morphisms.
Let $$A$$ and $$B$$ be commutative $$C^*$$-algebras.  Then, a morphism from $$A$$ to $$B$$ is defined to be a nondegenerate homomorphism of $$^*$$-algebras from $$\phi :A\rightarrow M(B)$$, where $$M(B)$$ is the multiplier algebra of $$B$$.  Here, nondegeneracy means that the the span of $$\left\{ \pi (a)b:a\in A,b\in M(B)\right\}$$ is dense in $$M(B)$$.  

**Note** that you need a bit of machinery to even make this into a category because it is not obvious a priori that composition makes sense.  Nevertheless, it does work out.  Proposition 1 on pg. 11 and Theorem 2 on pg. 12 of Superstrings, Geometry, Topology, and $$C^*$$-algebras (in fact this chapter is on the arXiv) respectively show that this forms a category and that the dual of this category is equivalent to the category of locally compact Hausdorff spaces.

