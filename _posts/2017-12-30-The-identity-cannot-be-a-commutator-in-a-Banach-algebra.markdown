---
layout: post
title: The identity cannot be a commutator in a Banach algebra
tag:
 - functional-analysis
 - banach-algebras

description: The identity cannot be a commutator in a Banach algebra

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

The identity cannot be a commutator in a Banach algebra?

<!–-break-–>


The Wikipedia article on Banach algebras claims, without a proof or reference, that there does not exist a (unital) Banach algebra $$B$$ and elements $$x, y \in B$$ such that $$xy - yx = 1$$.
 This is surprising to me, but maybe the proof is straightforward; anyone have a proof and/or a reference? 
More generally, we would have naively thought that we could embed any ring into a Banach algebra.
 we guess there are actually serious restrictions to doing this; are these issues discussed anywhere? 
.


# Answer 


Here's a sketch of a proof.  Let $$\sigma(x)$$ denote the spectrum of $$x$$.  Then $$\sigma(xy)\cup\{0\} = \sigma(yx)\cup\{0\}$$.  On the other hand, $$\sigma(1+yx)=1+\sigma(yx)$$.  If $$xy=1+yx$$, then the previous two sentences, along with the fact that the spectrum of each element of a Banach algebra is nonempty, imply that $$\sigma(xy)$$ is unbounded.  But every element of a Banach algebra has bounded spectrum.  
(we don't remember where we first learned this proof, nor do we have a reference for it off-hand, but we did not come up with it myself.)
The proof that $$\sigma(xy)\cup\{0\}=\sigma(yx)\cup\{0\}$$ reduces to showing that $$1-xy$$ is invertible if and only if $$1-yx$$ is invertible, a problem that was the subject of a MathOverflow question. 

There's a proof using derivations in section 2.2 of Sakai's book, Operator algebras in dynamical systems: the theory of unbounded derivations in $$C^*$$-algebras. A bounded derivation on a Banach algebra $$A$$ is a bounded linear map $$\delta$$ on $$A$$ such that $$\delta(ab)=\delta(a)b+a\delta(b)$$ for all $$a$$ and $$b$$ in $$A$$.  Theorem 2.2.1 on page 18 shows that if $$\delta$$ is a bounded derivation on $$A$$, and if $$a$$ is an element of $$A$$ such that $$\delta^2(a)=0$$, then $$\lim\limits_{n\to\infty}\|\delta(a)^n\|^{1/n}=0$$.  The proof uses induction with a neat computation to show that $$\delta^2(a)=0$$ implies that $$n!\delta(a)^n=\delta^n(a^n)$$, and then the result follows from boundedness of $$\delta$$ and the fact that $$\lim\limits_{n\to\infty}\frac{1}{\sqrt[n]{n!}}=0$$.  
Corollary 2.2.2 concludes that the identity is not a commutator.  If $$ab-ba=1$$, then the bounded derivation $$\delta_a:A\to A$$ defined by $$\delta_a(x)=ax-xa$$ satisfies $$\delta_a^2(b)=\delta_a(1)=0$$.  By the preceding theorem, this implies that $$1=\lim\limits_{n\to\infty}\|1^n\|^{1/n}=\lim\limits_{n\to\infty}\|\delta_a(b)^n\|^{1/n}=0$$.
(Completeness is not used in this approach.  An element $$x$$ of  $$A$$ satisfies $$\lim\limits_{n\to\infty}\|x^n\|^{1/n}=0$$ if and only if $$\sigma(x)=\{0\}$$, and such an $$x$$ is called a generalized nilpotent.  Incidentally, this also gives an approach to answering the example problem in the MathOverflow question Linear Algebra Problems?  The remainder of Section 2.2 has a number of interesting results on bounded derivations and commutators of bounded operators.)

