---
layout: post
title: Are there any series whose convergence is unknown
tag:
 - real-analysis
 - sequences-and-series
 - soft-question
 - infinity

description: Are there any series whose convergence is unknown

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Are there any series whose convergence is unknown?

<!–-break-–>


Are there any infinite series about which we don't know whether it converges or not? Or are the convergence tests exhaustive, so that in the hands of a competent mathematician any series will eventually be shown to converge or diverge?


**Edit**: People were kind enough to point out that ,without imposing restrictions on the terms, it's trivial to find such "open problem" sequences. So, to clarify, what we had in mind were sequences whose terms are composed of "simple" functions, the kind you would find in an introductory calculus text: exponential, factorial, etc.

# Answer 


It is unknown whether


$$


\sum_{n=1}^\infty\frac{1}{n^3\sin^2n}


$$


converges or not. The difficulty here is that convergence depends on the term $$n\sin n$$ not being too small, which in turn depends on how well $$\pi$$ can be approximated by rational numbers. It is possible that, if $$\pi$$ can be approximated `too well' enough by rationals, then this will diverge. See this MathOverflow question for a discussion of this particular series.
Another even simpler example of a sequence (no summation) for which it is not known whether it converges or not is


$$


x_n=\frac{1}{n^2\sin n}.


$$


We would expect this to tend to zero, but the proof is beyond what is currently known. Suppose that there were only finitely many rational numbers $$p/q$$ with $$\vert p/q-\pi\vert\le q^{-3+\epsilon}$$ (for any $$\epsilon > 0$$), then $$x_n$$ would tend to zero at rate $$O(n^{-\epsilon})$$. If, on the other hand, there were infinitely many rationals satisfying $$\vert p/q-\pi\vert\le q^{-3-\epsilon}$$, then infinitely many $$x_n$$ would be of order at least $$n^\epsilon$$, so it diverges. This can be expressed in terms of the irrationality measure of $$\pi$$. The sequence $$x_n$$ converges to zero if the irrationality measure of $$\pi$$ is less than 3, and diverges if it is geater than 3. Currently, the best known bound for the irrationality measure is that it is no more than about $$7.6063$$ (see the link to the mathworld page above). It is expected that the irrationality measure of $$\pi$$ is 2 (it is known that all but a zero-measure set of real numbers have irrationality measure 2). Therefore, it is expected that $$x_n$$ tends to zero, but there is currently no proof of this.

