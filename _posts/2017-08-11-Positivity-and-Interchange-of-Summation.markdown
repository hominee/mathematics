---
layout: post
title: Positivity and Interchange of Summation
tag:
 - real-analysis
 - sequences-and-series

description: Positivity and Interchange of Summation

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Positivity and interchange of Summation

<!–-break-–>


Suppose we  have $$\sum\limits_{n = 1}^{\infty}\sum\limits_{m = 1}^{\infty} a_{m, n}$$ where $$a_{m, n} \geq 0$$ for all $$m$$ and $$n$$. Can we  interchange the two summations? if so why?
.

# Answer 


it's worth knowing that rearrangements can change the value of sums or integrals only if the positive and negative parts both diverge to infinity.
Fubini's theorem says rearrangements are fine if both parts are finite.
Tonelli's theorem says rearrangements are fine if what's being summed or integrated is everywhere non-negative.  (it follows that it also works if it's everywhere non-positive, since the minus sign pulls out.)
Putting the two together gives you what we  said in the first paragraph.

