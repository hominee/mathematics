---
layout: post
title: What is the difference between a Hamel basis and a Schauder basis
tag:
 - linear-algebra
 - functional-analysis
 - schauder-basis
 - hamel-basis

description: What is the difference between a Hamel basis and a Schauder basis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What is the difference between a Hamel basis and a Schauder basis?

<!–-break-–>


Let $$V$$ be a vector space with infinite dimensions.
 A Hamel basis for $$V$$ is an ordered set of linearly independent vectors $$\{ v_i \ \| \ i \in I\}$$ such that any $$v \in V$$ can be expressed as a finite linear combination of the $$v_i$$'s; so $$\{ v_i \ \| \ i \in I\}$$ spans $$V$$ algebraically: this is the obvious extension of the finite-dimensional notion.
 Moreover, by Zorn Lemma, such a basis always exists.

If we endow $$V$$ with a topology, then we say that an ordered set of linearly independent vectors $$\{ v_i \ \| \ i \in I\}$$ is a Schauder basis if its span is dense in $$V$$ with respect to the chosen topology.
 This amounts to say that any $$v \in V$$ can be expressed as an infinite linear combination of the $$v_i$$'s, i.
e.
 as a series.

As far as we understand, if a $$v$$ can be expressed as finite linear combination of some set $$\{ v_i \ \| \ i \in I\}$$, then it lies in its span; in other words, if $$\{ v_i \ \| \ i \in I\}$$ is a Hamel basis, then it spans the whole $$V$$, and so it is a Schauder basis with respect to any topology on $$V$$.

However Per Enflo has constructed a Banach space without Schauder basis (ref.
 wiki).
 So we guess we should conclude that my reasoning is wrong, but we can't see what's the problem.
 So the point is that the vectors in a Hamel basis are Hamel independent (by def) but need not be Schauder-independent in general.
 As far as we understand, this is the fundamental reason why a Hamel basis is not automatically a Schauder basis.


# Answer 


People keep mentioning the restriction on the size of a Schauder basis, but we think it's more important to emphasize that these bases are bases with respect to different spans.
For an ordinary vector space, only finite linear combinations are defined, and you can't hope for anything more. (Let's call these Hamel combinations.) In this context, you can talk about minimal sets whose Hamel combinations generate a vector space.
When your vector space has a good enough topology, you can define countable linear combinations (which we'll call Schauder combinations) and talk about sets whose Schauder combinations generate the vector space.
If you take a Schauder basis, you can still use it as a Hamel basis and look at its collection of Hamel combinations, and you should see its Schauder-span will normally be strictly larger than its Hamel-span.
This also raises the question of linear independence: when there are two types of span, you now have two types of linear independence conditions. In principle, Schauder-independence is stronger because it implies Hamel-independence of a set of basis elements.
Finally, let me swing back around to the question of the cardinality of the basis. 
we don't actually think (/know) that it's absolutely necessary to have infinitely many elements in a Schauder basis. In the case where you allow finite Schauder bases, you don't actually need infinite linear combinations, and the Schauder and Hamel bases coincide. But definitely there is a difference in the infinite dimensional cases. In that sense, using the modifier "Schauder" actually becomes useful, so maybe that is why some people are convinced Schauder bases might be infinite.
And now about the limit on Schauder bases only being countable. Certainly given any space where countable sums converge, you can take a set of whatever cardinality and still consider its Schauder span (just like you could also consider its Hamel span). we know that the case of a separable space is especially useful and popular, and necessitates a countable basis, so that is probably why people tend to think of Schauder bases as countable. But we had thought uncountable Schauder bases were also used for inseparable Hilbert spaces.

