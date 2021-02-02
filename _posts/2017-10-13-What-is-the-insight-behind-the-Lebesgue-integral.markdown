---
layout: post
title: What is the insight behind the Lebesgue integral
tag:
 - probability
 - analysis
 - integration
 - measure-theory
 - functional-analysis

description: What is the insight behind the Lebesgue integral

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What is the insight behind the Lebesgue integral?

<!–-break-–>




**Edit** 3: OK, we had an insight, inspired in part by Ben-Blum Smith's comment, and the post he linked to.  (we have no idea if this insight is right; it's barely a hunch, and that's why we are  not submitting it as an answer to my original question [see below], but I'll throw it out there for criticism.)  we vaguely remember a theorem on the rearrangement the terms of infinite series showing that, at least for some series, for any $$L$$, it was possible to find a rearrangement of the terms that would cause the rearranged series to "converge" to $$L$$.  IIRC, this fact was somehow related to the such series were somewhat difficult to work with.  In any case, allowing any rearrangement of the terms, it seems, causes problems down the line, but if we were able to agree upon some reasonable canonicalization of the rearrangement procedure, or to put it differently, if we could find a reasonable way to define admissible rearrangements, this could be the basis for a new definition of an infinite series such that more series would converge (i.e. such that there would be a more robust definition of the series' limiting value).  One such canonicalization would go like this: divide the range of the series by some standard mesh (e.g. by numbers of the form $$m/2^n$$, for some fixed integer $$n$$, and all integers $$m$$ in some suitable interval).  Now rearrange the series by collecting together all the terms of the original series whose values lie within the same cell of the mesh, and ordering these "grouped terms" in decreasing order of their cell's value.  Then the series could be approximated by a weighted sum of these cell values.  This canonicalized sum would be immune to the pathologies caused by arbitrary rearrangements.  One would then need to show that this procedure behaves reasonably as one lets the size of the mesh go to zero.  Could something like this lead to the Lebesgue integral?


**Edit** 4: One point we did not make sufficiently clear in "

**Edit** 3" is that one could rationalize the concern with rearrangements by noting that one property that would be desirable in a definition of an integral is that it remains invariant relative to order in which the sum is performed.  The standard definition of the Riemann integral, as a sum that is ordered along the domain of integration, is susceptible to all the problems that one runs into when reordering infinite series (as alluded to above), which is unfortunate, considering that, when one works with sufficiently general functions, the ordering of the domain of integration should be irrelevant to the value of the integral: it should be possible to rearrange the domain of integration in fairly crazy ways and end up with the exact same integral.  In contrast, the procedure described in 

**Edit** 3 eliminates this dependence on any particular ordering of the domain of integration, and replaces it with a focus on the ordering of the range, which at least has a meaningful relationship to the value of the integral.  Also, it is clear why this alternative viewpoint shifts the focus to the problem of defining "measures" on sets, since these "measures" are precisely the weights assigned to the grouped terms in the new summation procedure.

[Original post]
we understand the definitions of the Lebesgue integral and of the Riemann integral, but it is not obvious to me from these definitions that the former would be the more suitable of the two for, say, probability theory, or for defining the Fourier transform, or for defining inner products in Hilbert space, etc.  What was exactly the insight that led to the Lebesgue integral as a superior alternative to the Riemann integral?
Thanks!



**Edit** 1: after looking at the comments/answers so far (with one exception) we realized that the leading wording of my question was quite inept.  we have  highlighted the part of my original question that is least ineptly put.  we know that Lebesgue integrals have all the advantages cited, but it is utterly mystifying to me how anyone could have seen ahead of time that this had to be the case.  What made this alternative approach (of the Lebesgue integral) look promising?  we know that it's perfectly possible that there was no clue that this approach would be fruitful: someone (Lebesgue, we suppose) just tried it, played with it for a while, and discovered all these unsuspected benefits, and had the latter not happened, the new approach would have been quietly forgotten.  But, just in case there is some clue (even a "clue-in-hindsight") of the alternative POV's superiority, we would love to see it.  (The "one exception" we mentioned above is Christian Blatter's answer, which goes in the direction we was trying to get at, but I'd like to give my question a second shot.)


**Edit** 2: To be fair to the commenters, we have not finished digesting all the previous posts linked to in the comments; they may very well be what we was looking for.  (In particular, the one with the metaphor featuring a shop owner, etc., may be just the thing.)
.

# Answer 




**Edit** (in response to your 3rd edit)
It seems you're really close to considering the concept of the gauge integral. One of the problems with the Riemann integral is that the definition is very restrictive: For every $$\varepsilon > 0$$ there must exist a tagged partition $$P$$ such that for all finer partitions $$P^*$$ [$$\ldots$$].
But what if we had some way to throw "bad" partitions away? Then there would be fewer obstructions to being integrable and thus it would be easier for this process to "converge" (q.v. Wikipedia::Net for a more precise definition) - and that's exactly what the gauge integral does.

Original post
What made measure theory look fruitful? To answer this question one needs to understand that Lebesgue's ideas weren't conceived ex nihilo. Lebesgue was certainly familiar with Jordan's work on the subject and from this he would surely have known that a bounded function $$f: [a,b] \to \mathbb R$$ is Riemann integrable if and only if the two sets 


$$

\begin{align*}
A_+ &:= \{(x,y) \in \mathbb R^2 \;|\; a \leq x \leq b \land 0 \leq y \leq f(x)\} \text{ and} \\
A_- &:= \{(x,y) \in \mathbb R^2 \;|\; a \leq x \leq b \land f(x) \leq y \leq 0\}
\end{align*}

$$


are Jordan measureable. And in that case we have 


$$

\int_a^b f(x)\,dx = m(A_+) - m(A_-)

$$


where $$m$$ is the Jordan measure.
The Jordan measure is only finitely additive, so Lebesgue could conclude that to get something new he'd have to consider at least countable additivity - and since uncountable additivity is right out (an interval is made up of uncountably many singletons each of measure $$0$$), that would be a natural starting place.
What we find to be the true genius in Lebesgue's work on the integral is his idea to start from a list of requirements and work towards constructing something that satisfies the items on the list. This was quite a novel approach at the time, and it has become so commonplace that when students today are introduced to the Lebesgue integral the idea of a list of desired properties shouldn't seem novel at all.

