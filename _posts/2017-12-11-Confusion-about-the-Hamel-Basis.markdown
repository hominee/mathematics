---
layout: post
title: Confusion about the Hamel Basis
tag:
 - vector-spaces
 - hilbert-spaces
 - definition
 - hamel-basis

description: Confusion about the Hamel Basis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Confusion about the Hamel Basis

<!–-break-–>


Alright, so we are  reading a book on Hilbert spaces and functional analysis, and here it defines a "Hamel basis" to be a "maximal linearly independent set".
 we take this to mean that $$S$$ is a Hamel basis if $$S$$ is linearly independent, and there is no linearly independent set $$T$$ for which $$\|T\|>\|S\|$$.

On the other hand, this article defines (on page

6) a "Hamel basis" to be a basis in which "we do not allow infinite sums" (i.
e.
 in which every element can be expressed as a finite linear combination of basis vectors).

Also, the distinction they make between an orthonormal basis and a Hamel basis makes me think that an orthonormal basis does allow infinite sums, but their definition of "basis" on the first page requires finite linear combinations as well.

we are  just really confused, we can't tell which source we should trust and can't seem to find a single resource that gives the "correct" answer (not sure if we want to trust Wikipedia, though they seem to make the distinction too when defining the Schauder basis).
 What's the correct definition of a Hamel basis? Does the general definition of a "basis" allow for infinite linear combinations, or only finite ones? What about orthonormal and Hamel? Why would the book we are  reading define a Hamel basis in the way it did? What's even the point of making the distinction between a Hamel basis and any other basis; is a Hamel basis also orthonormal?
To completely avoid ambiguity, these are the rigorous definitions we are  using:
Linearly Independent: A subset $$S$$ of a vector space $$V$$ over a field $$K$$ is linearly independent if for every finite subset $$G\subseteq S$$, the only sequence $$\{\alpha_s\}_{s\in G}$$ to $$\sum_{s\in G}\alpha_ss = 0$$ is $$\{\alpha_s\} = 0$$.

Basis: A subset $$S$$ of a vector space $$V$$ is a basis if it is linearly independent, and every vector $$v\in V$$ can be expressed as a finite linear combination of vectors in $$S$$.

Orthonormal Basis: A subset $$S$$ of a Hilbert space $$\Bbb{H}$$ is an orthonormal basis if it is pairwise orthogonal ($$e_1,\ e_2\in S$$ and $$e_1\neq e_2\rightarrow e_1\perp e_2$$), every element is a unit vector, and every element of $$\Bbb{H}$$ can be expressed as a linear combination (finite or infinite) of elements of $$S$$.

Hamel Basis Definition 1: A Hamel basis for a Hilbert space $$\Bbb{H}$$ is a set $$S$$ such that $$S$$ is linearly independent, and there is no linearly independent set $$T$$ with $$\|T\|>\|S\|$$.

Hamel Basis Definition 2: A Hamel basis for a Hilbert space is a (potentially orthonormal?) basis under finite linear combinations.


# Answer 


Your definitions of "linearly independent", "basis", and "orthonormal basis" are all correct.  In particular, an orthonormal basis for an infinite-dimensional Hilbert space is not actually a basis (since you will need to use infinite linear combinations).
"Hamel basis" means exactly the same thing as "basis".  The reason that it is given a different name is to emphasize that you are talking about a basis with respect to finite linear combinations, as opposed to some other kind of object that might be referred to using the word "basis" but which is not actually a basis (such as an orthonormal basis or a Schauder basis).  Indeed, when talking about infinite-dimensional topological vector spaces, it is rare that you actually care about a basis as opposed to some related notion that allows for infinite linear combinations.  So in most contexts if someone refers to a "basis" of such a space, it is actually more likely than not that they are abusing terminology and are using "basis" as an abbreviation for "orthonormal basis" or something similar.  To make it clear that you literally mean just a basis, it is common to say "Hamel basis".
As for your book's definition, note that "maximal" means "cannot be enlarged to a superset", not "cannot be enlarged in cardinality".  So a "maximal linearly independent set" is a linearly independent set $$S$$ such that there is no proper superset $$T$$ of $$S$$ which is linearly independent.  This is equivalent to saying $$S$$ spans the whole space (using finite linear combinations).  Indeed, if $$S$$ does not span the whole space, you can take any vector not in its span and add it to $$S$$ to get a larger linearly independent set.  Conversely, if $$S$$ does span the whole space, any vector not in $$S$$ is a linear combination of elements of $$S$$ and thus would give a linearly dependent set if you added it to $$S$$.

