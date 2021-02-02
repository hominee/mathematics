---
layout: post
title: Problem related to real analysis and indefinite integrals
tag:
 - real-analysis
 - indefinite-integrals

description: Problem related to real analysis and indefinite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When we can change $$\int$$ and $$\sum$$ for indefinite integral?

<!–-break-–>


we know, for example, that if the series $$\displaystyle\sum_{n=1}^{\infty}f_n(x)$$ consisting of integrable functions on a closed interval $$[a, b] \subset \mathbb{R}$$ converges uniformly on that closed interval, then its sum is also integrable on $$[a, b]$$ and 

$$

\int_a^b \left(\sum_{n=1}^{\infty}f(x)\right)\, dx=\sum_{n=1}^{\infty} \int_a^b f_n(x)\, dx.

$$


Or, Beppo-Levi lemma (we are working on $$(X, \mathfrak{M}, \mu))$$: Let $$f_n:X \to [0,+\infty]$$ be sequence of measurable functions on $$X$$. Then, for every measurable set $$A \subset X,$$


$$

\int_A \sum_{n=1}^{\infty} f_n \, d\mu =\sum_{n=1}^{\infty} \int_A f_n d\mu.

$$


And similar proposition.
But, we are working here with definite integrals. My question is: What we can say if we are working with indefinite integrals. Is this always true, or we have some restrictions?
.

# Answer 


A well known calculus theorem says: If $$F_n:\>[a,b]\to{\mathbb R}$$ is a sequence of differentiable functions that converges at the point $$\xi\in[a,b]$$, and if the sequence of derivatives $$f_n:=F_n'$$ converges uniformly on $$[a,b]$$ to some function $$f:\>[a,b]\to{\mathbb R}$$ then the $$F_n$$ converge in fact uniformly on $$[a,b]$$ to some function $$F$$, and one has $$F'=f$$.
Given this theorem and the sequence $$(f_n)_{n\geq1}$$ we can fix a point $$\xi\in \ ]a,b[\ $$ and choose for all $$n\geq1$$ the particular primitive of $$f_n$$ that vanishes at $$\xi$$. The $$F_n$$ so determined satisfy the assumptions of the above theorem, and the desired conclusion follows.

