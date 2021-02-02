---
layout: post
title: Problem related to real analysis
tag:
 - real-analysis

description: Problem related to real analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

if $$f:[0,1] \to \mathbb{R}$$ is increasing, show that $$f$$ is the pointwise limit of a sequence of continuous functions over $$[0,1]$$ 

<!–-break-–>


Clearly there is a sequence converging pointwise to $$f$$, we can set:
$$\forall n \in \mathbb{N}, f_n = f$$.

How to prove there is at least one which is made up of continuous functions $$f_n, \forall n \in \mathbb{N}$$ over $$[0,1]$$ we can't quite figure out the argument.
 
.


# Answer 


Let $$\mathcal{D}$$ be the set of discontinuities of $$f$$. We know that $$\mathcal{D}$$ is at most countable, so we enumerate this set by $$\mathcal{D} = \{ x_0, x_1, \cdots \}$$. Now for each $$n \geq 0$$, let


$$

 \Pi_n = \{ \tfrac{k}{2^n} : 0 \leq k \leq 2^n \} \cup \{ x_0, \cdots, x_n \} 

$$


and define $$f_n : [0, 1] \to \mathbb{R}$$ as the linear interpolation of the points $$\{ (x, f(x)) : x \in \Pi_n\}$$ ordered from left to right. Then

It is clear that $$f_n$$ is continuous and increasing for each $$n\geq 0$$.
If $$x \in \cup_{n\geq 0} \Pi_n$$, then $$x \in \Pi_N$$ for some $$N$$ and hence by construction, $$f_n(x) = f(x)$$ for all $$n \geq N$$. So we have $$f_n(x) \to f(x)$$ as $$n\to\infty$$. 
If $$x \in [0, 1] \setminus \mathcal{D}$$, then for each fixed $$m$$ there is $$a_m, b_m \in \Pi_m$$ such that $$a_m \leq x \leq b_m$$ and $$\|b_m - a_m\| \leq 2^{-m}$$. Taking limit as $$n\to\infty$$ to the inequality $$f_n(a_m) \leq f_n(x) \leq f_n(b_m)$$, we obtain

$$
\begin{align*}
f(a_m)
= \lim_{n\to\infty} f_n (a_m)
&\leq \liminf_{n\to\infty} f_n (x) \\
&\leq \limsup_{n\to\infty} f_n (x)
 \leq \lim_{n\to\infty} f_n (b_m)
 = f(b_m).
\end{align*}
$$

Taking $$m \to \infty$$, both $$(a_m)$$ and $$(b_m)$$ converge to $$x$$. Since $$x$$ is a continuity point of $$f$$, we have


$$

 f(x) \leq \liminf_{n\to\infty} f_n (x) \leq \limsup_{n\to\infty} f_n (x) \leq f(x) 

$$


and hence $$f_n(x) \to f(x)$$.

Combining altogether, it follows that $$f_n \to f$$ pointwise on $$[0, 1]$$ as expected.

