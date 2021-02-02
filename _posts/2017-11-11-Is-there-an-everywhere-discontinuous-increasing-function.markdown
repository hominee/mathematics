---
layout: post
title: Is there an everywhere discontinuous increasing function
tag:
 - calculus
 - real-analysis

description: Is there an everywhere discontinuous increasing function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is there an everywhere discontinuous increasing function?

<!–-break-–>


Does there exist a function $$f : \mathbb{R} \rightarrow \mathbb{R}$$ that is strictly increasing and discontinuous everywhere?
My line of thought (possibly incorrect): we know there are increasing functions such as $$f(x) = x$$, and there are everywhere-discontinuous functions such as the Dirichlet function.
 we also know that when there is a discontinuity at a point $$c$$, there is a finite gap $$\epsilon$$ such that there are points $$d$$ arbitrarily close to $$c$$ such that $$\|f(d) - f(c)\| > \epsilon$$.
 This is where my thinking gets unclear - does it make sense to have a "gap" at every real number?
.


# Answer 


There is no such function. Suppose that $$f:\mathbb{R}\to\mathbb{R}$$ is strictly increasing. For each $$a\in\mathbb{R}$$ let $$f^-(a) =$$  $$\lim\limits_{x\to a^-}f(x)$$ and $$f^+(a) = \lim\limits_{x\to a^+}f(x)$$. Then $$f$$ is discontinuous at $$a$$ if and only if $$f^-(a) < f^+(a)$$. Let $$D = \{a\in\mathbb{R}:f\text{ is not continuous at }a\}$$, and for each $$a\in D$$ let $$q_a$$ be a rational number in the non-empty open interval $$I_a = (f^-(a),f^+(a))$$. 
It’s not hard to check that if $$a,b \in D$$ with $$a<b$$, then $$f^+(a) \le f^-(b)$$, so the intervals $$I_a$$ are pairwise disjoint. This implies that the rational numbers $$q_a$$ are all distinct. (If you want to be fancy, the function from $$D$$ to $$\mathbb{Q}$$ that sends $$a$$ to $$q_a$$ is injective.) But there are only countably many rational numbers, so the set $$D$$ must be countable. In other words, the function $$f$$ can have at most countably many points of discontinuity. And of course $$\mathbb{R}$$ is uncountable, so $$f$$ cannot be discontinuous everywhere.

