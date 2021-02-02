---
layout: post
title: When can a sum and integral be interchanged
tag:
 - real-analysis
 - analysis

description: When can a sum and integral be interchanged

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When can a sum and integral be interchanged?

<!–-break-–>


Let's say we have $$\int_{0}^{\infty}\sum_{n = 0}^{\infty} f_{n}(x)\, dx$$ with $$f_{n}(x)$$ being continuous functions. When can interchange the integral and summation? Is $$f_{n}(x) \geq 0$$ for all $$x$$ and for all $$n$$ sufficient? How about when $$\sum f_{n}(x)$$ converges absolutely? If so why?


# Answer 


we like to remember this as a special case of the Fubini/Tonelli theorems, where the measures are counting measure on $$\mathbb{N}$$ and Lebesgue measure on $$\mathbb{R}$$ (or $$[0,\infty)$$ as you've written it here).  In particular, Tonelli's theorem says if $$f_n(x) \ge 0$$ for all $$n,x$$, then 

$$

\sum \int f_n(x) dx = \int \sum f_n(x) dx

$$

 without any further conditions needed.  (You can also prove this with the monotone convergence theorem.)
Then Fubini's theorem says that for general $$f_n$$, if $$\int \sum \|f_n\| < \infty$$ or $$\sum \int \|f_n\| < \infty$$ (by Tonelli the two conditions are equivalent), then $$\int \sum f_n = \sum \int f_n$$.  (You can also prove this with the dominated convergence theorem.)
There may be weaker conditions that would also suffice, but these tend to work in 99% of cases.

Elaborating on request: the usual statement of Fubini's theorem goes something like this:

Let $$(X,\mathcal{F}, \mu),(Y,\mathcal{G}, \nu)$$ be $$\sigma$$-finite measure spaces, and let $$g : X \times Y \to \mathbb{R}$$ be measurable with respect to the product $$\sigma$$-algebra $$\mathcal{F} \otimes \mathcal{G}$$.  
Suppose that $$\int_X \int_Y \|g(x,y)\| \nu(dy) \mu(dx)$$ is finite.  (

**Note**: By Tonelli's theorem, this happens if and only if $$\int_Y \int_X \|g(x,y)\|\mu(dx)\nu(dy)$$ is finite, since both iterated integrals are equal.)   Then 

$$

\int_X \int_Y g(x,y) \nu(dy)\mu(dx) = \int_Y \int_X g(x,y) \mu(dx) \nu(dy).

$$



Let $$X = \mathbb{R}$$, $$\mathcal{F}$$ the Borel $$\sigma$$-algebra, and $$\mu$$ Lebesgue measure.  Let $$Y = \mathbb{N}$$, $$\mathcal{G} = 2^{\mathbb{N}}$$ the discrete $$\sigma$$-algebra, and $$\nu$$ counting measure.  Define $$g(x,n) = f_n(x)$$.  Exercise: since each $$f_n$$ is measurable, verify that $$g$$ is measurable with respect to $$\mathcal{F} \otimes \mathcal{G}$$.  Exercise: verify that integration with respect to counting measure is the same as summation, where the integral exists and is finite iff the sum converges absolutely.  (That is, given a sequence of real numbers $$a_n$$, define a function $$b : \mathbb{N} \to \mathbb{R}$$ by $$b(n) = a_n$$.  Then $$\int_{\mathbb{N}} b\,d\nu = \sum_{n=1}^\infty a_n$$.)
As such, the conclusion of Fubini's theorem reduces to the statement that was to be proved.

