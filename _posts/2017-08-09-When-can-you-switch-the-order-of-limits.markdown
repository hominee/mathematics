---
layout: post
title: When can you switch the order of limits
tag:
 - real-analysis
 - sequences-and-series
 - limits

description: When can you switch the order of limits

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When can you switch the order of limits?

<!–-break-–>


Suppose you have a double sequence $$\displaystyle a_{nm}$$.  What are sufficient conditions for you to be able to say that $$\displaystyle \lim_{n\to \infty}\,\lim_{m\to \infty}{a_{nm}} = \lim_{m\to \infty}\,\lim_{n\to \infty}{a_{nm}}$$?  Bonus points for necessary and sufficient conditions.
For an example of a sequence where this is not the case, consider $$\displaystyle a_{nm}=\left(\frac{1}{n}\right)^{\frac{1}{m}}$$.  $$\displaystyle \lim_{n\to \infty}\,\lim_{m\to \infty}{a_{nm}}=\lim_{n\to \infty}{\left(\frac{1}{n}\right)^0}=\lim_{n\to \infty}{1}=1$$, but $$\displaystyle \lim_{m\to \infty}\,\lim_{n\to \infty}{a_{nm}}=\lim_{m\to \infty}{0^{\frac{1}{m}}}=\lim_{m\to \infty}{0}=0$$.

# Answer 


if you want to avoid hypotheses that involve uniform convergence, you can always cheat and use the counting measure on {0, 1, 2,...} and then use either the Monotone or Dominated Convergence Theorem from integration theory.
For instance, using the Monotone Convergence Theorem, we get the following (perhaps silly) sufficient criterion:
Proposition: if $$a_{mn}$$ is monotonically increasing in $$m$$, and is such that $$c_{mn} = a_{mn} - a_{m-1,n}$$ is monotonically increasing in $$n$$, then $$\lim\limits_{m \to \infty} \lim\limits_{n \to \infty} a_{mn} = \lim\limits_{n\to\infty}\lim\limits_{m\to\infty} a_{mn}$$.
Proof: Our two hypotheses really just amount to saying that each $$c_{mn} \geq 0$$ and that the $$c_{mn}$$ are monotonically increasing in $$n$$.  So we can use the Monotone Convergence Theorem with respect to the counting measure:

 $$ 
\lim_{n\to \infty} \int c_{mn} = \int \lim_{n\to \infty} c_{mn}
 $$ 

But really, these integrals are sums, so:

 $$ 
\lim_{n\to \infty} \sum_{m=1}^\infty c_{mn} = \sum_{m=1}^\infty \lim_{n\to \infty} c_{mn}
 $$ 

Since infinite sums are just limits of partial sums, we have:

 $$ 
\lim_{n\to \infty} \lim_{M \to \infty} \sum_{m=1}^M c_{mn} = \lim_{M\to\infty}\lim_{n\to \infty} \sum_{m=1}^M c_{mn}
 $$ 

By our construction of $$c_{mn}$$, the left side is $$\lim\limits_{n\to\infty} \lim\limits_{M\to\infty} a_{Mn}$$, and the right side is $$\lim\limits_{M\to\infty} \lim\limits_{n\to\infty}a_{Mn}$$. $$\lozenge$$

**Edit**:
in the above, our index ranges are $$m,n \geq 1$$, and we make the convention that $$a_{0n} = 0$$.
Using the Dominated Convergence Theorem, we could probably get something slightly more useful.

