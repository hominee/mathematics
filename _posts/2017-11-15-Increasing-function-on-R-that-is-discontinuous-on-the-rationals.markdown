---
layout: post
title: Increasing function on R that is discontinuous on the rationals
tag:
 - real-analysis

description: Increasing function on R that is discontinuous on the rationals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Increasing function on R that is discontinuous on the rationals

<!–-break-–>


The question (Folland's Real Analysis, 3.
5.
30) asks to produce an increasing function on $$\mathbb{R}$$ whose set of discontinuities is the rationals.
 My train of thought is as follows:
Let $$f_0$$ be the identity.
 We want to create a jump at every rational number, while keeping the function increasing.
 Create $$f_1$$ by cutting $$f_0$$ at each integer, and halving the slope of each resulting line segment, fixing the left endpoints.
 This results in a sort of slanted stair that is still increasing and discontinuous exactly at the integers.
 Given $$f_{n-1}$$, we create $$f_n$$ by cutting each segment of $$f_{n-1}$$ into $$n$$ parts and halving the slope of each resulting segment, again fixing the left endpoints.
 

**Note**: this is equivalent to making cuts at all rational points $$\frac{m}{n!}$$ at the $$n^\text{th}$$ step, with $$m$$ and $$n$$ not necessarily coprime.

The limit of such sequence of functions exists.
 It's easy to prove that any rational point is eventually a left endpoint, and is thus kept fixed by all successive functions in the sequence.
 For an irrational point $$x$$ we can make two sequences $$a_n$$ and $$b_n$$ of rationals converging from the left and right respectively, such that $$a_n=\frac{m}{n!}<x$$ and $$b_n=\frac{m+1}{n!}>x$$.
 Given $$\epsilon$$, we can then choose $$N$$ large enough with $$a_N$$ and $$b_N$$ on the same segment of $$f_{N-1}$$ (so the jump from $$f_{N-1}(a_N)$$ to $$f_{N-1}(b_N)$$ is small), with this jump being less than $$\epsilon$$.
 Since we can pinpoint the value of $$f_n(x)$$ between arbitrarily close values, the limit $$f(x)=\lim_n f_n(x)$$ exists.

It's clear that the function is discontinuous at all rationals since it is constructed to be, and it is increasing since each $$f_n$$ is increasing.

Can we say that $$f$$ is continuous at each irrational? My gut feeling is that, since any $$\delta$$-ball around an irrational contains a rational to the left and one to the right, we cannot necessarily say $$f$$ is continuous there.
 However we know by theorem 3.
23 in the book that the set of discontinuities of an increasing function is countable.


# Answer 


There is a simpler construction:
If we take a numeration $$(q_n)_{n \in \mathbb{N}}$$ of $$\mathbb{Q}$$, we can define


$$

f(x) := \sum_{k=1}^\infty \frac{1}{2^k} 1_{[q_k, \infty)}(x).

$$


The convergence is uniform and this function is monotone increasing by construction. Since all $$1_{[q_n,\infty)}$$ are continuous in all points of $$\mathbb{R} \setminus \mathbb{Q}$$, the limes is this too. (If $$x$$ is irrational, then we can take $$\varepsilon >0$$ so small that $$(x-\varepsilon,x+\varepsilon)$$ doesn't contain the points $$q_1,\ldots,q_n$$. So $$\|f(x)-f(y)\| \le \sum_{k=n}^\infty 2^{-k} \le 2^{1-n}$$.)
Fix $$n$$. For any $$\max_{q_i < q_n,i=1,\ldots n} q_i < x < q_n < y < \max_{q_i > q_n,i =1 \ldots, n}$$ q_i we have
$$f(x) + 2^{-n} \le f(y)$$. Thus $$f$$ is discontinuous in any point of $$\mathbb{Q}$$.

