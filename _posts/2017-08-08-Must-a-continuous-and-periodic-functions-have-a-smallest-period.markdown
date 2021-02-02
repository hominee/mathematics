---
layout: post
title: Must a continuous and periodic functions have a smallest period
tag:
 - real-analysis
 - continuity
 - periodic-functions

description: Must a continuous and periodic functions have a smallest period

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Must a continuous and periodic functions have a smallest period?

<!–-break-–>


Let $$D\subset\mathbb R$$ and let $$T\in(0,+\infty)$$. A function $$f\colon D\longrightarrow\mathbb R$$ is called a periodic function with period $$T$$ if, for each $$x\in D$$, $$x+T\in D$$ and $$f(x+T)=f(x)$$.

we f $$D\subset\mathbb R$$ and $$f\colon D\longrightarrow\mathbb R$$ is continuous and periodic, must there be, among all periods of $$f$$, a minimal one?

Questions like this one have been posted here before, but in each case, as far as we  can see, the domain of $$f$$ was $$\mathbb R$$, which implies that the set $$P$$ of periods, together with $$0$$ and $$-P$$, is a subgroup of $$(\mathbb{R},+)$$. Using that (together with continuity), it is easy to see that a minimal period must exist indeed. But we  don't know whether it is true or not in the general case.

# Answer 


This has the air of exploiting a hole left in the question parameters, but here comes. 
Let
$$D=\{0\}\cup(1,\infty)$$ and let $$f(x)$$ be a constant function. Then $$T$$ will be a period if and only if $$T+D\subseteq D$$. we n particular:

every $$T>1$$ is a period, but
$$T=1$$ is not a period (and there cannot be smaller periods $$\le 1$$),
so there is no smallest period.


