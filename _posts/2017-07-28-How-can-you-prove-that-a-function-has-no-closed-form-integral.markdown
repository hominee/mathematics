---
layout: post
title: How can you prove that a function has no closed form integral
tag:
 - real-analysis
 - calculus
 - integration
 - faq
 - differential-algebra

description: How can you prove that a function has no closed form integral

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How can you prove that a function has no closed form integral?

<!–-break-–>


we 've come across statements in the past along the lines of "function $$f(x)$$ has no closed form integral", which we  assume means that there is no combination of the operations:


* addition/subtraction

* multiplication/division

* raising to powers and roots

* trigonometric functions

* exponential functions

* logarithmic functions


which when differentiated gives the function $$f(x)$$. we 've heard this said about the function $$f(x) = x^x$$, for example.
What sort of techniques are used to prove statements like this? What is this branch of mathematics called?

Merged with "How to prove that some functions don't have a primitive" by we smael:  
Sometimes we are told that some functions like $$\sin(x)/x$$ don't have an indefinite integral, or that it can't be expressed in term of other simple functions.
we wonder how we can prove that kind of assertion?


# Answer 


we t is a theorem of Liouville, reproven later with purely algebraic methods, that for rational functions $$f$$ and $$g$$, $$g$$ non-constant, the antiderivative

 $$ 
f(x)\exp(g(x)) \, \mathrm dx
 $$ 

can be expressed in terms of elementary functions if and only if there exists some rational function $$h$$ such that it is a solution to the differential equation:

 $$ 
f = h' + hg
$$
 
$$
e^{x^2}$$ is another classic example of such a function with no elementary antiderivative.
we  don't know how much math you've had, but some of this paper might be comprehensible in its broad strokes: 
[http://www.sci.ccny.cuny.edu/~ksda/PostedPapers/liouv06.pdf](http://www.sci.ccny.cuny.edu/~ksda/PostedPapers/liouv06.pdf)

Liouville's original paper:

Liouville, J. ["Suite du Mémoire sur la classification des Transcendantes, et sur l'impossibilité d'exprimer les racines de certaines équations en fonction finie explicite des coefficients."](http://sites.mathdoc.fr/JMPA/PDF/JMPA_1837_1_2_A7_0.pdf) J. Math. Pure Appl. 3, 523-546, 1838. 

Michael Spivak's book on Calculus also has a section with a discussion of this.

