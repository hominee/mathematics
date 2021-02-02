---
layout: post
title: Why can't differentiability be generalized as nicely as continuity
tag:
 - general-topology
 - derivatives
 - differential-geometry
 - differential-topology

description: Why can't differentiability be generalized as nicely as continuity

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Why can't differentiability be generalized as nicely as continuity?

<!–-break-–>


The question: Can we define differentiable functions between (some class of) sets, "without $$\Bbb R$$"* so that it

Reduces to the traditional definition when desired?
Has the same use in at least some of the higher contexts where we would use the present differentiable manifolds?


Motivation/Context:
we was a little bit disappointed when we learned to differentiate on manifolds.
 Here's how it went.

A younger me was studying metric spaces as the first unit in a topology course when a shiny new generalization of continuity was presented to me.
 we was thrilled because we could now consider continuity in a whole new sense, on function spaces, finite sets, even the familiar reals with a different metric, etc.
 Still, we felt like we hadn't escaped the reals (why we wanted to we can't say, but we digress) since we was still measuring distance (and therefore continuity, in my mind) with a real number: 

$$

d: X\to\huge\Bbb R

$$


If the reader for some reason shares or at least empathizes with (we honestly can't explain this fixation of mine) the desire to have definitions not appeal to other sets/structures*, then they will understand my excitement in discovering an even more general definition, the standard one on arbitrary topological spaces.
 we was home free; the new definition was totally untied to the ever-convenient real numbers, and of course we could recover my first (calculus) definition, provided we toplogized $$\Bbb R^n$$ adequately (and it seemed very reasonable to toplogize $$\Bbb R^n$$ with Pythagoras' theorem, after all).

Time passed and we kept studying, and through other courses (some simultaneous to topology, some posterior) a new sort of itch began to develop, this time with differentiable functions.
 On the one hand, we had definitions (types of convergence, compact sets, orientable surfaces, etc.
) and theorems (Stone-Weierstrass, Arzelá-Ascoli, Brouwer fixed point, etc.
) completely understandable through my new-found topology.
 On the other hand, the definition of a derivative was still the same as ever, we could not see it nor the subsequent theorems "from high above" as with topological arguments.

But then a new hope (happy may 4th) came with a then distant but closely approaching subject, differential geometry.
 The prospect of "escaping" once again from the terrestrial concepts seemed very promising, so we decided to look ahead and open up a few books to see if we could finally look down on my old derivative from up top in the conceptual clouds.
 My expectation was that, just like topology had first to define a generalized "closeness structure" i.
e.
 lay the grounds on which general continuous functions could be defined via open sets, we would now encounter the analogous "differentiable structure" (we had no idea what this should entail but we didn't either for topology so why not imagine it).
 And so it went: "oh, so you just.
.
.
 and then you take it to $$\Bbb R^n$$.
.
.
 and you use the same definition of differentiable".

Why is this so? How come we're able to abstract continuity into definitions within the same set, but for differentiability, we have to "pass through" the reals? we realize that this really has to do with why we have to generalize in the first place, so what happens is that the respective generalizations have usefulness in the new contexts, hence the second point in my question statement.

Why we imagine this is plausible, a priori, is because there's a historical standard: start with the low-level definitions $$\rightarrow$$ uncover some properties $$\rightarrow$$ realize these are all you wanted anyhow, and redefine as that which possesses the properties.
 Certainly, derivatives have properties that can be just as well stated for slightly more general sets! (e.
g.
 linearity, but of course this is far from enough).
 But then, we'll all agree that there's even been a lust for conducting the above process, everywhere possible, so maybe there are very strong obstructions indeed, which inhibit it's being carried out in this case.
 In this case, we should ask what these obstructions are, or how we should begin identifying them.

* If we are  being honest, before asking this we should really answer the question of what on earth we mean, precisely, by "a structure that doesn't appeal to another".
 First of all, we might come across a new definition that apparently doesn't use $$\Bbb R$$, but is "isomorphic" to having done so (easy example: calling $$\Bbb R$$ a different name).
 Furthermore, we are  always inevitably appealing to (even naïve) set theory, the natural numbers, etc.
 without any fuss.
 So, if my qualms are to have a logical meaning, there should be a quantifiable difference in appealing to $$\Bbb R$$ vs.
 appealing to set theory and other preexisting constructs.
 If the respondent can remark on this, super-kudos (and if they can but the answer would be long and on the whole unrelated, say this and I'll post another question).
 
.


# Answer 


There "is" a way, since in algebraic geometry, we do not work over the real numbers in general, yet we use techniques inspired from differentiation all the time. It is not the way preferred by most differential geometry textbooks who stick to charts and differentiable structures, but it still works. 
A ringed space $$(X,\mathcal O_X)$$ is a topological space together with a sheaf of rings $$\mathcal O_X$$ on it. A locally ringed space is a ringed space such that the stalks $$\mathcal O_{X,p}$$ are local rings for each $$p \in X$$. If $$(X,\mathcal O_X)$$ is a locally ringed space, we can define the cotangent space at $$p$$ via $$\mathfrak m_{X,p}/\mathfrak m_{X,p}^2$$ where $$\mathfrak m_{X,p}$$ is the unique maximal ideal of $$\mathcal O_{X,p}$$. This is a vector space over the field $$k(p) \overset{def}= \mathcal O_{X,p}/\mathfrak m_{X,p}$$, so we can define the tangent space as the dual $$k(p)$$-vector space to $$\mathfrak m_{X,p}/\mathfrak m_{X,p}^2$$, or in other words, the set of all linear maps $$\mathfrak m_{X,p}/\mathfrak m_{X,p}^2 \to k(p)$$. 
The idea is that if you have a linear map $$\mathfrak m_{X,p}/\mathfrak m_{X,p}^2 \to k(p)$$, and you are given a "function" $$f \in \mathfrak m_{X,p}$$, the value of the linear map at $$f$$ should give you the "direction"al derivative of $$f$$. 
Of course, this level of abstraction removes any reference to coordinate patches and such, so it is hard to see what's going on. To remove all the algebro-geometric nonsense and get a particular example, take a manifold $$M$$ (which is a topological space) and consider the sheaf $$\mathcal O_M$$ of $$C^{\infty}$$-functions on $$M$$, that is, if $$U \subseteq M$$ is an open set, $$\mathcal O_M(U)$$ is the set of smooth functions $$U \to \mathbb R$$. Then $$\mathcal O_{M,p}$$ consists of all germs of functions at $$p$$, and $$\mathfrak m_{M,p}$$ is the maximal ideal of those germs whose value at $$p$$ is zero. The ideal $$\mathfrak m_{M,p}^2$$ is the ideal of all finite sums of products of two functions in $$\mathfrak m_{M,p}$$, and in particular such functions always vanish with multiplicity $$\ge 2$$ (this is the product rule for differentiation). It is usually shown that the dual of $$\mathfrak m_{M,p}/\mathfrak m_{M,p}^2$$ corresponds to the space of all derivations at $$p$$ ; note that in this case, we have $$k(p) \simeq \mathbb R$$, so that the linear maps $$\mathfrak m_{M,p}/\mathfrak m_{M,p}^2 \to k(p)$$ actually take values in the real numbers. 
Of course, the sheaf $$\mathcal O_M$$ needs to be defined, and this is usually done at some point using coordinate patches ; you do not get away from dealing with charts when doing differential geometry. Sure, at some point you stop using them if you deal with coordinate-free approaches, but they lie somewhere in the treatment of the theory. My point is that the ideas of differentiation do generalize, and this is just a quick glance of how it does ; algebraic geometry takes "differentiation" to a whole new level. 
As continuity has been weakened and played with in many different ways (weak/weak-star convergence in functional analysis, semi-upper-lower-continuity in optimization, etc.) and differentiation too (Fréchet, Gâteaux, directional derivatives, semi-directional derivatives, Dini derivatives), you should always remember one thing : yes generalizations are useful, but you should never forget why you wanted to generalize in the first place. It can be either because you want to pay attention to a certain class of problems that you cannot solve and want to have a clearer point of view or to build stronger tools, but generalizing for the sake of generalizing usually leads to being confused and losing intuition, which is not what you want. To this day we are  still scared of the use of Dini derivatives...
Hope that helps,

