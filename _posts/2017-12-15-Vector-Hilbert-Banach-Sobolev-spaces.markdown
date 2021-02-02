---
layout: post
title: Vector, Hilbert, Banach, Sobolev spaces
tag:
 - functional-analysis
 - vector-spaces
 - banach-spaces
 - hilbert-spaces
 - sobolev-spaces

description: Vector, Hilbert, Banach, Sobolev spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Vector, Hilbert, Banach, Sobolev spaces

<!–-break-–>


Trying to wrap my head around all these different spaces.
 Which one is the most general? Can you summarize the differences between them? Is there a notable space that we missed?
.


# Answer 


Clearly, vector spaces are the most general notion among these, because they can be defined over any field and all, Banach, Hilbert and Sobolev spaces are vector spaces.
Banach spaces make sense over any normed field (e.g. $$\mathbb{R}$$ or $$\mathbb{C}$$). we have  only encountered Hilbert spaces over the reals or the complex numbers so far. Every Hilbert space is a Banach space and every Banach space is a normed vector space.
Sobolev spaces are quite a bit more special. They are a class of function spaces, usually defined for open subsets of $$\mathbb{R}^n$$ or sometimes on manifolds. Sobolev spaces are usually Banach spaces, but they can be Hilbert spaces as well (for the exponent $$p = 2$$).
Finally, you omitted the important classes of locally convex spaces and Fréchet spaces among many other things. Except for general vector spaces all the mentioned classes are (Hausdorff) topological vector spaces, but we don't think it's worthwhile to indulge in name-dropping. Without further information about your goal, it's hard to tell what kind of answer you are looking for. I'd recommend having a look at any introductory text on functional analysis where most of these classes of spaces are touched upon.

