---
layout: post
title: Problem related to linear algebra and hamel basis
tag:
 - linear-algebra
 - functional-analysis
 - lp-spaces
 - normed-spaces
 - hamel-basis

description: Problem related to linear algebra and hamel basis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What is the basis of the vector space $$l^\infty$$?

<!–-break-–>


We know that every vector space has a Hamel basis and also every normed space need not have a Schauder basis.
 As the normed space $$l^\infty$$ is not Separable so can't have the Schauder basis, but on the other side $$l^\infty$$ is also a vector space so what will be the Hamel basis of $$l^\infty$$?
.


# Answer 


An indication that you cannot expect explicit example is that this cannot be proven in ZF. 
In an infinite-dimensional normed space, existence of Hamel basis implies existence of discontinuous linear functional. And it is consistent with ZF that there are no discontinuous linear functionals on $$\ell_\infty$$, see here: On every infinite-dimensional Banach space there exists a discontinuous linear functional. (Perhaps there is a more straightforward argument, but this is is what we was able to come up with.)
However, if you only want proof that $$\ell_\infty$$ has Hamel basis, it is as standard application of Zorn's lemma. In fact, every linearly independent set is contained in a basis. (And for this proof there is nothing special about $$\ell_\infty$$ - it works for any vector space exactly in the same way.)

