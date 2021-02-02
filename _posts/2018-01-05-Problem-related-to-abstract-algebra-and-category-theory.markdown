---
layout: post
title: Problem related to abstract algebra and category theory
tag:
 - abstract-algebra
 - reference-request
 - ring-theory
 - category-theory

description: Problem related to abstract algebra and category theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

The category of rings with $$1$$ vs the category of rings with or without $$1$$

<!–-break-–>


The question of whether the definition of a ring should include the existence of an identity for the multiplication (and whether homomorphisms should preserve this identity) seems to divide many mathematicians.
 Many textbooks considered "standard" use different conventions.
 we are  not interested in debating which convention is best.
 However, we are  very interested in the differences between the two categories associated to these two conventions: the category of rings which may or may not have a $$1$$ (where, of course, morphisms do not preserve the $$1$$) and the category of rings with $$1$$ (where morphisms preserve $$1$$).
 
These two categories appear to be very different.
 For example, if we require the existence of a $$1$$, then ideals are no longer objects in our category.
 If we do not require a $$1$$, then the zero ring is both an initial and a terminal object (whereas it is only a terminal object in the category of rings with $$1$$).

Are there other important or "interesting" distinctions between these two categories? Does anyone know of a reference which systematically addresses this question?
.


# Answer 


we wrote a blog post addressing this question. Briefly, it turns out that the category of non-unital rings over a base commutative ring $$k$$ is equivalent to the category of augmented rings, meaning rings equipped with a map $$A \to k$$ called the augmentation. The map in one direction is given by taking the unitalization, and in the other direction it's given by taking the kernel of the augmentation. 
In the commutative case, and taking opposites, this gives us that the category of "non-unital affine schemes" over $$\text{Spec } k$$ is equivalent to the category of pointed affine schemes over $$\text{Spec } k$$. This means the relationship between the two categories is closely analogous to the relationship between sets and pointed sets. 

**Note** that pointed sets also has a zero object. 
In the commutative C*-algebra case, and keeping in mind the commutative Gelfand-Naimark theorem, this gives us that the opposite of the category of non-unital commutative C*-algebras is equivalent to the category of pointed compact Hausdorff spaces. It is sometimes stated, incorrectly, that it is equivalent to the category of locally compact Hausdorff spaces, and that is not true. There are more morphisms in this category; see for example this math.SE question. 

