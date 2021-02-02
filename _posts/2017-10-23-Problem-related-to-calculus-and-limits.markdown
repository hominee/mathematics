---
layout: post
title: Problem related to calculus and limits
tag:
 - calculus
 - real-analysis
 - limits

description: Problem related to calculus and limits

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Does there exist a function such that $$\lim_{x \to a} f(x) = L$$ for all $$a \in \mathbb R$$ but $$f(x)$$ is never $$L$$?

<!–-break-–>



Does there exist a function $$f:\mathbb R \to \mathbb R$$ such that $$\lim_{x \to a} f(x) = L$$ for
  all $$a \in \mathbb R$$ but $$f(x) \neq L$$ for all $$x$$?

we found such a function in $$\mathbb Q \to \mathbb Q$$, where $$f(\frac{p}{q})= \text{first p+q digits of }\pi$$ satisfies the above condition.
 However, we have not been able to extend it to reals.
 So, is such a function possible, and if it is, is there any explicit example preferably related to the above function in rationals? 
.


# Answer 


Let's consider an arbitrary closed interval $$[a, b]$$. Let $$\epsilon > 0$$ be arbitrarily given. For each point $$c$$ of $$[a, b]$$ there is a neighborhood $$I_{c}$$ of $$c$$ such that 

$$

\|f(x) - L\| < \epsilon

$$

 for all $$x \in I_{c} \setminus \{c\}$$. Clearly all such intervals $$I_{c}$$ form an open cover for $$[a, b]$$ and by Heine Borel Theorem a finite number of such intervals say $$I_{c_{1}}, I_{c_{2}}, \ldots, I_{c_{m}}$$ cover $$[a, b]$$.
It thus follows that $$\|f(x) - L\| < \epsilon$$ for all $$x \in [a, b]$$ except for a finite number of points $$c_{1}, c_{2}, \ldots, c_{m}$$. Now we choose specific values of $$\epsilon$$. For each positive integer $$n$$ we have a finite number, say $$k_{n}$$, of points in $$[a, b]$$ for which $$\|f(x) - L\| \geq 1/n$$. Let the set of points in $$[a, b]$$ for which $$\|f(x) - L\| \geq 1/n$$ be denoted by $$A_{n}$$. Then $$A_{n}$$ is a finite set of cardinality $$k_{n}$$ and since the set of points in $$[a, b]$$ for which $$f(x) \neq L$$ is obviously contained in the union $$\bigcup_{n = 1}^{\infty}A_{n}$$ it follows that the set of points in $$[a, b]$$ for which $$f(x) \neq L$$ is countable. It follows that $$f(x) = L$$ on $$[a, b]$$ for uncountably many points $$x$$.

