---
layout: post
title: Two exercises in functional analysis.
tag:
 - functional-analysis

description: Two exercises in functional analysis.

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Two exercises in functional analysis.

<!–-break-–>


we have met two questions which, after some attempts have we have yet been able to solve nor find any available solutions online.
 Could anyone please offer me some insights?

Let $$ H $$ be a Hilbert space over $$\mathbb{C}$$ and $$T \in B(H,H)$$ an unitary operator.
 For $$ n \in \mathbb{N} $$ set 

$$

 S_n : = \frac
{1}{n}( we + T + .
.
.
 + T^{n-1} ) .


$$


Show that $$S_{n}v \longrightarrow P_{M}v $$ as $$ n \rightarrow \infty $$ where $$ P_{M} $$ is the orthogonal projection onto the subspace $$ \text{Ker}(we - T) $$.

Let $$E$$ be a normed vector space over $$\mathbb{K}$$, let $$M \subseteq E $$ be a subset and suppose that $$ \sup_{ v \in M} \|f(v)\| < \infty $$ for a all functional $$f \in B(E, \mathbb{K})$$.
 Show that $$M$$ is bounded.


From what we have heard the second question is not meant to be difficult.
 However as $$E$$ is not complete there is not much theorem we could work with.
 we thought maybe by working with the Banach space $$ B(E,\mathbb{K}) $$ but came to no result.


# Answer 


The second question is an application of uniform boundedness. Let $$j:E\to E^{**}$$ be the natural embedding and consider $$j(M)\subset B(E^*,\Bbb K)$$. For all $$f\in E^*$$ you have $$\{ j(m)\,(f)=f(m) \mid m\in M\}$$ is bounded. By uniform boundedness the set $$j(M)$$ is bounded in $$E^{**}$$. But $$j$$ is an isometric embedding, so $$M$$ must be bounded in $$E$$.

The first question can be done either with the spectral theorem for unitary operators or by explicitly showing $$S_nv\to 0$$ if $$v\in \ker(I-T)^\perp$$ and noting $$S_nv=v$$ if $$v\in \ker(I-T)$$. From this follows that $$S_n$$ converges pointwise to the projection onto $$\ker(I-T)$$.
Now the second part is trivial, for the first note $$\|S_n(I-T)\| = \|\frac1n(I-T^n)\|≤\frac2n$$. Now $$\langle(I-T)v,w\rangle=\langle v,(I-T^*)w\rangle$$ from which


$$

\mathrm{im}(I-T)^\perp = \ker(I-T^*)=\ker(I-T).

$$


This means that $$\mathrm{im}(I-T)$$ is dense in $$\ker(I-T)^\perp$$. So for any $$\epsilon>0, v\in \ker(I-T)^\perp$$ we find a $$w$$ with $$\|v-(I-T)w\|<\epsilon$$. It follows


$$

\|S_nv\|≤\|S_n\|\,\|v-(I-T)w\|+\|S_n(I-T)w\|≤\epsilon+\frac2n\|w\|.

$$


As $$n$$ goes to infinity you find that $$\limsup_n\|S_nv\|≤\epsilon$$, which was arbitrary. It follows $$S_nv\to 0$$ for $$v\in \ker(I-T)^\perp$$.

