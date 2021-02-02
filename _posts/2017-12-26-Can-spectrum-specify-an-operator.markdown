---
layout: post
title: Can spectrum “specify” an operator
tag:
 - soft-question
 - functional-analysis
 - spectral-theory

description: Can spectrum “specify” an operator

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Can spectrum “specify” an operator?

<!–-break-–>


Given a bounded operator $$A$$ on a Banach space $$X$$, one may find the spectrum $$\sigma(A)\subset{\bf C}$$.
 
Here are my questions:


Given some set in the complex plane, say, $$S\subset{\bf C}$$, can one find an operator $$A$$ such that $$\sigma(A)=S$$? 
Is there a "big picture" for this kind of questions?


.


# Answer 


Let $$A$$ be a bounded operator on the Banach space $$X$$.  
The spectrum of $$A$$ must be closed. The set of invertible operators on a Banach space is open, and $$\lambda\mapsto A-\lambda I$$ is continuous.  The resolvent set of $$A$$ (complement of the spectrum) is the inverse image of the invertible operators under this map.  
The spectrum of $$A$$ must be bounded. If $$\|\lambda\|>\|A\|$$, then $$\|\frac{1}{\lambda}A\|=\|I-(I-\frac{1}{\lambda}A)\|<1$$. This implies that $$I-\frac{1}{\lambda}A$$ is invertible, which in turn implies that $$A-\lambda I$$ is invertible.
The spectrum is nonempty.  The function $$\lambda\mapsto (A-\lambda I)^{-1}$$ is holomorphic on the resolvent set and goes to $$0$$ at infinity.  If it were defined on the whole complex plane, it would be identically $$0$$ by Liouville's theorem (you can apply Hahn-Banach and the scalar-valued version of Liouville).  But this is absurd, because $$(A-\lambda I)^{-1}$$ is invertible whenever it exists.
So to have any hope, $$S$$ should be compact and nonempty.  If you are allowing $$X$$ to vary, then this is sufficient, and it is enough to consider Hilbert space as Rasmus already mentioned.  For example, you could let $$\mu$$ be a regular Borel measure with support $$S$$, and then let $$A$$ be the operator on $$L^2(\mu)$$ defined by $$(Af)(x)=xf(x)$$.  (Or you could consider diagonal operators on spaces with chosen bases.)
If you mean that $$X$$ is fixed, then the answer depends on $$X$$, and we don't know what can be said in general.  Of course if $$X$$ is finite dimensional, then the possible spectra are the sets with cardinality no greater than the dimension of $$X$$.  There are also infinite dimensional spaces for which not every nonempty compact set can be the spectrum of an operator.  As mentioned in a comment on Rasmus's answer, Argyros and Haydon showed that there are infinite dimensional Banach spaces on which every operator has the form $$\lambda we +K$$ with $$K$$ compact.  Since compact operators have countable spectrum with $$0$$ as the only possible limit point, $$\lambda I+K$$ has countable spectrum with $$\lambda$$ as the only possible limit point. 

Some searching inspired by Theo Buehler's question (which in turn was inspired by this question and Nate Eldredge's comment above) has turned up the fact that hereditarily indecomposable Banach spaces also have the property that all operators have countable spectrum with at most one limit point.  Every operator on such a space is scalar plus strictly singular, and there were known examples well before Argyros and Haydon's breakthrough, as mentioned on Gowers's blog (and constructed by Gowers himself as well as Maurey).  It is also known that there are hereditarily indecomposable spaces such that not every operator is scalar plus compact.  Maurey's chapter in the Handbook of the geometry of Banach spaces, Volume 2, titled "Banach spaces with few operators," gives an introduction to these and much more.  (we cannot really add anything better than a pointer to this wonderful reference, due to my ignorance.)

