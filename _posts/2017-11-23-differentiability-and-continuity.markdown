---
layout: post
title: differentiability and continuity
tag:
 - general-topology
 - soft-question

description: differentiability and continuity

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

differentiability and continuity

<!–-break-–>


we have a question which is quite "candid" and for which we can hardly formalize properly every concepts but nonetheless, we was wondering if there were some topoligical and/or algebraic structure properties over spaces (to be defined) that make the set of continuous functions and the set of differentiable functions the same.
 
Maybe this is simply impossible or only for trivial examples.

Best regards
PS : Motivation is simple curiosity
.


# Answer 


Lie groups almost provide another example.
A continuous homomorphism between Lie groups is automatically smooth.  Of course, one needs to assume it's a homomorphism which is very strong condition (hence, the "almost" above).
The idea of the proof is in two big steps.  First one proves that any closed subgroup of a Lie group is automatically smooth (known as Cartan's theorem).  The idea of this proof is that one can identify what the tangent space to the identity should be using the group exponential map and show this tangent space is actually closed under addition using closedness.
The second step is a bit easier:  given $$f:G\mapsto H$$, consider the map $$g:G\mapsto G\times H$$ given by $$g(x) = (x,f(x))$$.  Using hypothesis on $$f$$, one proves that the image of $$g$$ is a closed subgroup, hence smooth by step 1.  This implies the two projection maps, when restricted to the image of $$g$$, are smooth.  With a bit more work, one shows $$f$$ can be written as a composition of projection maps and their inverses, so is smooth.

