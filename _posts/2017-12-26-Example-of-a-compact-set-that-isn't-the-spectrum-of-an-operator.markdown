---
layout: post
title: Example of a compact set that isn't the spectrum of an operator
tag:
 - functional-analysis
 - banach-spaces
 - spectral-theory

description: Example of a compact set that isn't the spectrum of an operator

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Example of a compact set that isn't the spectrum of an operator

<!–-break-–>


This question is a follow-up to this recent question and related to that one.


Is there an easy example of an (infinite-dimensional) Banach space $$X$$ and a non-empty compact set $$K \subset \mathbb{C}$$ that can't be the spectrum of a bounded operator $$A: X \to X$$?

Of course, if $$X$$ contains an infinite-dimensional Hilbert space as a norm one complemented subspace and $$\emptyset \neq K \subset \mathbb{C}$$ is an arbitrary compact set then we can produce an operator $$A: X \to X$$ such that $$\sigma(A) = K$$.

As Jonas Meyer pointed out in his answer, the recent breakthrough by Argyros and Haydon settling the long-standing scalar-plus-compact problem (see Gowers's blog entry for some background) shows that there is a space with the property that the only possbile spectra of bounded operators are the countable and compact subsets of $$\mathbb{C}$$ with at most one accumulation point.
 (

**Update**: Jonas Meyer has added further information and pointers to the literature to his answer, I'll refrain from repeating this information here since we couldn't add anything of interest.
) But these examples are definitely far more involved than we would like them to be.
 If it turns out that the example has to be so difficult for some reason that eludes me, I'd like to hear about that, too.

More optimistically, one might ask: 

Are there known classes of infinite-dimensional Banach spaces for which there is a characterization of the compact subsets of $$\mathbb{C}$$ that may arise as spectra of bounded operators?

A nice answer to this optimistic question would be: The class of such-and-such Banach spaces has the property that only/precisely the, say, totally disconnected compact subsets of $$\mathbb{C}$$ arise as spectra of bounded operators.
 

**Update**: In view of the question in the title, we are  of course most interested in answers that exclude certain compact subsets of $$\mathbb{C}$$.



**Update** 2: we asked a slightly updated version of this question on MathOverflow.


# Answer 


Jonas asked me to add an answer to avoid letting the bounty wither away. Unfortunately, the question on MO did not lead to a conclusive answer so far. However, Bill Johnson — a world renowned expert on the theory of Banach spaces — left the following two comments (we quote):


we are  not aware of an example before Gowers-Maurey of a Banach space such that not every compact subset of the plane is the spectrum of an operator on the space.
To realize every compact subset of the plane as the spectrum of some operator on a space, it is enough that the space has a complemented subspace with an unconditional basis. Before Gowers-Maurey, there were known to exist separable spaces (such as the Kalton-Peck twisted sum of two Hilbert spaces) such that no complemented subspace has an unconditional basis.


From comment 1. we feel that it is safe to conclude:

The question does not seem to have a simple positive answer. If it should, rather surprisingly, happen to have one, it probably hasn't been found or noticed so far.

Let me quickly indicate my thoughts on comment 2.
First of all, Bill is referring to the twisted sum construction introduced in the paper
MR0542869 (82g:46021) 
Kalton, N. J.; Peck, N. T.,
Twisted sums of sequence spaces and the three space problem. 
Trans. Amer. Math. Soc. 255 (1979), 1–30.
Now, as Bill notes, a necessary condition for $$X$$ to possibly exclude certain compact sets as spectra is the absence of any complemented infinite-dimensional subspace admitting an unconditional basis. One of the corollaries of Kalton-Peck's work (precisely their corollary 6.9) is that the twisted sum $$Z_{p}$$ of two $$\ell^{p}$$-spaces for $$1 \lt p \lt \infty$$ does not admit such a complemented subspace. As the paper by Kalton-Peck is well writtan and it's getting late here, we are  not entering into details now.
Thus, $$Z_{p}$$ would be a possible candidate. However, it is not obvious to me at all to decide whether this actually yields the desired example or not. Let me mention that the Kalton-Peck construction has a very nice homological algebra interpretation in terms of non-triviality of Yoneda-Exts of Banach spaces and explicit constructions using what they call quasi-linear maps. we will elaborate in the next few days as we still need to check some details.
we are  accepting this answer in order to close this question here and because we have little doubt that this question will remain unanswered for quite a bit. If you should happen to know anything of interest, please leave a comment here or answer the question on MO. Any input will be very very welcome, of course.

