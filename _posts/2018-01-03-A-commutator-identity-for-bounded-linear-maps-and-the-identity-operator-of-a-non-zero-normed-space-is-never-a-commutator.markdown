---
layout: post
title: A commutator identity for bounded linear maps and the identity operator of a non-zero normed space is never a commutator
tag:
 - functional-analysis
 - normed-spaces

description: A commutator identity for bounded linear maps and the identity operator of a non-zero normed space is never a commutator

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A commutator identity for bounded linear maps and the identity operator of a non-zero normed space is never a commutator

<!–-break-–>


Let $$ \mathcal{X} $$ be a normed linear space and $$ S,T: \mathcal{X} \to \mathcal{X} $$ be linear operators such that $$ S \circ T- T \circ S=1 $$.


Show that $$ S \circ T^{n+1}- T^{n+1} \circ S=(n+1)T^n $$ for $$ n=0,1,2,.
.
.
 $$
Deduce that if $$ S$$ is bounded then $$ T$$ is unbounded.


For the first part we thought of applying the principle of mathematical induction.


# Answer 



Yes, induction is the way to go. The case $$n=0$$ is the hypothesis $$ST - TS = 1$$, and for the induction step assume $$(n+1)T^{n} = ST^{n+1} - T^{n+1}S$$ and use $$ST = TS + 1$$ to calculate 

$$

\begin{align*}(n +1) T^{n+1} &= (n+1)T^{n}T = (ST^{n+1} - T^{n+1}S)T = ST^{n+2} - T^{n+1}(TS+1) \\&= ST^{n+2} - T^{n+2}S - T^{n+1}\end{align*}

$$


which after rearranging is the identity you want to prove.
we do not see how the second part is obvious "[s]ince $$S \circ T - T\circ S = 1$$ is the commutator", unless you are in positive finite dimension and apply the trace to reach the contradiction $$0 = \dim\mathcal{X}$$ or you know about the Wielandt-Wintner theorem, which is a consequence of the exercise you're solving.
Anyway, exclude the case $$\mathcal{X} = 0$$ and look at the identity from part 1.  If $$T^{N} = 0$$ for some $$N$$, let $$n$$ be the smallest $$n$$ such that $$T^{n+1} = 0$$. Then $$ST^{n+1} - T^{n+1}S = (n+1)T^{n} = 0$$ hence $$T^{n} = 0$$ contradicting the choice of $$n$$. So, suppose $$T^{n} \neq 0$$ for all $$n$$ and assume that $$T$$ is bounded. Take the norm on both sides. Leave the right hand side as it is and for the left hand side you get the estimate


$$

\lVert S T^{n+1} - T^{n+1}S\rVert \leq 2 \lVert S\rVert \lVert T^{n} \rVert \lVert T\rVert.

$$

 
Then you can deduce that $$2 \lVert S \rVert \lVert T \rVert \geq n+1$$ by dividing by $$\lVert T^n\Vert$$ on both sides. This quickly leads to a contradiction.


