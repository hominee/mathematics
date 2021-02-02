---
layout: post
title: Is this operator compact
tag:
 - functional-analysis
 - banach-spaces
 - operator-theory

description: Is this operator compact

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is this operator compact?

<!–-break-–>


Suppose ($$x_n$$) is a normalized, linearly independent,  sequence in a reflexive Banach space $$X$$, and $$T$$ is an injective, strictly singular,  bounded operator on $$X$$ such that $$Tx_n\longrightarrow 0$$.
 Does there exist a subsequence $$(y_n)$$ of $$(x_n)$$ such that $$T$$ restricted to the closed span of $$(y_n)$$ is compact? When $$(x_n)$$ is a basic sequence and $$\sum\|\|Tx_n\|\|$$ converges (so $$Tx_n\longrightarrow 0$$ fast enough), it is not hard to show that $$T$$ restricted to closed span of $$(x_n)$$ is indeed compact (without any need to assume that $$T$$ is strictly singular or $$X$$ is reflexive).
 
An operator is called strictly singular if it is not an isomorphism when restricted to any infinite dimensional subspace.
 Compact operators are always strictly singular but not the other way around.
 However, strictly singular are compact in $$l_p$$  and $$c_0$$.
  
.


# Answer 


The answer is yes, there is such a subsequence.
We do not need to assume strict singularity of $$T$$, we use boundedness and injectivity of $$T$$, that $$\|T x_n\| \xrightarrow{n\to\infty} 0$$ and reflexivity of $$X$$.
Since $$X$$ is reflexive, the unit ball is weakly sequentially compact by the Eberlein–Šmulian theorem, so we may pass to a weakly convergent subsequence $$x_n \to x$$. Since $$T$$ is bounded, we also have that $$Tx_n \to Tx$$ weakly, but by hypothesis $$Tx_n \to 0$$ in norm. Thus $$Tx = 0$$ and by injectivity of $$T$$ we must have that $$x = 0$$.
Since $$(x_n)_{n=1}^\infty$$ is normalized and $$x_n \to 0$$ weakly, the Bessaga–Pełczyński selection principle(1) allows us  to pass to a basic subsequence of $$x_n$$.
Passing to yet another subsequence, we finally find a basic sequence $$(x_{n_k})_{k=1}^\infty$$ such that $$\sum_{k=1}^{\infty} \|Tx_{n_k}\| \lt \infty$$, and this yields that the restriction of $$T$$ to the linear span of $$(x_{n_k})_{k=1}^\infty$$ is compact by what you mentioned in your question.

(1) If $$x_n \to 0$$ weakly and $$\inf_{n\in\mathbb{N}} \|x_n\| \gt 0$$ then there is a basic subsequence $$(x_{n_k})_{k=1}^\infty$$ of $$(x_n)_{n=1}^\infty$$.
The proof of this is known as the “gliding hump argument”, and was established as Corollary C.1, page 156 in Bessaga–Pełczyński, On bases and unconditional convergence of series in Banach spaces, Studia Math. 17 (1958), 151–164.
See also Albiac–Kalton, Topics in Banach Space Theory, Proposition 1.5.2, as well as Proposition 1.3.10 and Theorem 1.4.4.

