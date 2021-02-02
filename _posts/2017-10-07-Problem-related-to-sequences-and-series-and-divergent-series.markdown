---
layout: post
title: Problem related to sequences and series and divergent series
tag:
 - sequences-and-series
 - riemann-zeta
 - divergent-series

description: Problem related to sequences and series and divergent series

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Strictly speaking, is it true that $$\zeta(-1)\ne1+2+3+\cdots$$?

<!–-break-–>


There are various notorious proofs that $$1+2+3+\cdots=\frac{-1}{12}.$$
Some of the more accessible proofs basically seem to involve labelling this series as $$S=\sum_\limits{i=1}^
\infty i$$ and playing around with it until you can say $$12S=-1$$.
Even at High School, we could have looked at that and thought "well since you're dealing with infinities and divergent series, those manipulations of $$S$$ are not valid in the first place so you're really just rearranging falsehoods." It's a bit like the error in this proof that $$1=0$$, or $$\forall x.(\text{false}\implies x)$$, it's a collapse of logic.
Greater minds than mine have shown that $$\zeta(-1)=\frac{-1}{12}$$ and we have no argument with that, but we do dispute the claim that $$\zeta(-1)=S$$.
My thinking here is that, although the analytic continuation of $$\zeta$$ is well-defined, that analytic continuation is not the same thing as $$\sum_\limits{i=1}^\infty i$$.
Once you have

defined $$\zeta(s) =\sum_\limits{n=1}^\infty\frac{1}{n^s}$$ where $$\vert s\vert>1$$
defined $$\zeta^\prime(s)=...$$ by analytic continuation for all $$s$$

then you can only claim

$$\zeta(s)=\zeta^\prime(s)$$ where $$\vert s\vert>1$$.

Basicaly, your nice, differentiable-everywhere definition of the Zeta function is not substituable for the original series $$S$$ in the unrestricted domain.
Hence, $$\zeta(-1)=\frac{-1}{12}\nRightarrow S=\frac{-1}{12}$$.
Right? Convince me otherwise.

# Answer 


You only have 


$$

\zeta(s)=\sum_{n=1}^\infty n^{-s}

$$


for $$\mathfrak R(s)>1$$. The right-hand side of the equation is not defined otherwise.
Like you said, $$\zeta(s)$$ is defined by analytic continuation on the rest of the complex numbers, so the formula $$\zeta(s)=\sum_{n=1}^\infty n^{-s}$$ is not valid on $$\mathbb C \setminus \{z\in \mathbb C, \mathfrak R(z)>1\}$$.
Therefore, 


$$

\frac{-1}{12}=\zeta(-1)\ne \sum_{n=1}^\infty n \quad \text{(which =+\infty in the best case scenario)}.

$$


So what you say is correct.

