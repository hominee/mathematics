---
layout: post
title: Problem related to real analysis and functional equations
tag:
 - real-analysis
 - continuity
 - functional-equations

description: Problem related to real analysis and functional equations

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Find a real function $$f:\mathbb{R}\to\mathbb{R}$$ such that $$f(f(x)) = -x$$?

<!–-break-–>


we 've been perusing the internet looking for interesting problems to solve. we  found the following problem and have been going at it for the past 30 minutes with no success:

Find a function $$f: \mathbb{R} \to \mathbb{R}$$ satisfying $$f(f(x)) = -x$$ for all $$x \in \mathbb{R}$$.

we are  also wondering, can ifind $$f$$ so that is continuous?
we  was thinking of letting $$f$$ be a periodic function, and adding half the period to x each time. we  had no success with this, and am now thinking that such a function does not exist.
Source: http://www.halfaya.org/Casti/CalculusTheory2/challenge.pdf
.

# Answer 


An important piece of information is:
Theorem: $$f$$ is not continuous.
Proof: Observe that $$f$$ is invertible, because

 $$ 
f(f(f(f(x)))) = f(f(-x)) = x
 $$ 

and so $$f \circ f \circ f = f^{-1}$$. Any continuous invertible function on $$\mathbb{R}$$ is either strictly increasing or strictly decreasing.
if $$f$$ is strictly increasing, then:

$$
1 < 2
$$

$$
f(1) < f(2)
$$

$$
f(f(1)) < f(f(2))
$$

$$
-1 < -2$$

contradiction! Similarly, if $$f$$ is strictly decreasing, then:

$$ 
1 < 2 
$$

$$
f(1) > f(2)
$$

$$
f(f(1)) < f(f(2))
$$

$$
-1 < -2
$$

contradiction! Therefore, we conclude $$f$$ is not continuous. $$\square$$

For the sake of completeness, the entire solution space for $$f$$ consists of functions defined as follows:

Partition the set of all positive real numbers into ordered pairs $$(a,b)$$
Define $$f$$ by, whenever $$(a,b)$$ is one of our chosen pairs,

$$f(0) = 0$$

$$
f(a) = b
$$

$$
f(b) = -a
$$

$$
f(-a) = -b
$$

$$
f(-b) = a
$$


To see that every solution is of this form, let $$f$$ be a solution. Then we must have $$f(0) = 0$$ because:

Let $$f(0) = a$$. Then $$f(a) = f(f(0)) = 0$$ but $$-a = f(f(a)) = f(0) = a$$, and so $$f(0) = 0$$

if $$a \neq 0$$, then let $$f(a) = b$$. We have:

$$f(b) = f(f(a)) = -a
$$
f(-a) = f(f(b)) = -b
$$
f(-b) = f(f(-a)) = a$$

From here it's easy to see the set $$\{ (a,f(a)) \mid a>0, f(a)>0 \}$$ partitions the positive real numbers and so is of the form we  describe above.

One particular solution is

 $$ 
 f(x) = \begin{cases}
   0   & x = 0
\\ x+1 & x > 0 \wedge \lceil x \rceil \text{ is odd}
\\ 1-x & x > 0 \wedge \lceil x \rceil \text{ is even}
\\ x-1 & x < 0 \wedge \lfloor x \rfloor \text{ is odd}
\\ -1-x & x < 0 \wedge \lfloor x \rfloor \text{ is even}
\end{cases}
 $$ 

e.g. $$f(1/2) = 3/2$$, $$f(3/2) = -1/2$$, $$f(-1/2) = -3/2$$, and $$f(-3/2) = 1/2$$.
(This works out to be Jyrki Lahtonen's example)

