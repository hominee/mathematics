---
layout: post
title: Problem related to real analysis and elementary set theory
tag:
 - real-analysis
 - elementary-set-theory

description: Problem related to real analysis and elementary set theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Examples of bijective map from $$\mathbb{R}^3\rightarrow \mathbb{R}$$ 

<!–-break-–>



# Answer 


First, note that it is enough to find a bijection $$f:\Bbb R^2\to \Bbb R$$, since then $$g(x,y,z) = f(f(x,y),z)$$ is automatically a bijection from $$\Bbb R^3$$ to $$\Bbb R$$.
Next, note that since there is a bijection from $$[0,1]\to\Bbb R$$ (see appendix), it is enough to find a bijection from the unit square $$[0,1]^2$$ to the unit interval $$[0,1]$$. By constructions in the appendix, it does not really matter whether we consider $$[0,1]$$, $$(0,1]$$, or $$(0,1)$$, since there are easy bijections between all of these.
Mapping the unit square to the unit interval

There are a number of ways to proceed in finding a bijection from the unit square to the unit interval.  One approach is to fix up the "interleaving" technique we mentioned in the comments, writing $$\langle 0.a_1a_2a_3\ldots, 0.b_1b_2b_3\ldots\rangle$$ to $$0.a_1b_2a_2b_2a_3b_3\ldots$$.  This doesn't quite work, as we noted in the comments, because there is a question of whether to represent $$\frac12$$ as $$0.5000\ldots$$ or as $$0.4999\ldots$$. We can't use both, since then $$\left\langle\frac12,0\right\rangle$$ goes to both $$\frac12 = 0.5000\ldots$$ and to $$\frac9{22} =  0.40909\ldots$$ and we don't even have a function, much less a bijection.  But if we arbitrarily choose to the second representation, then there is no element of $$[0,1]^2$$ that is mapped to $$\frac12$$, and if we choose the first there is no element that is mapped to $$\frac9{22}$$, so either way we fail to have a bijection.
This problem can be fixed.

(In answering this question, we tried many web searches to try to remember the fix, and we was amazed at how many sources we found that ignored the problem, either entirely, or by handwaving. we never did find it; we had to remember it. Sadly, we cannot remember where we saw it first.)
First, we will deal with $$(0,1]$$ rather than with $$[0,1]$$; bijections between these two sets are well-known, or see the appendix. For real numbers with two decimal expansions, such as $$\frac12$$, we will agree to choose the one that ends with nines rather than with zeroes. So for example we represent $$\frac12$$ as $$0.4999\ldots$$.
Now instead of interleaving single digits, we will break each input number into chunks, where each chunk consists of some number of zeroes (possibly none) followed by a single non-zero digit.  For example, $$\frac1{200} = 0.00499\ldots$$ is broken up as $$004\ 9\ 9\ 9\ldots$$, and $$0.01003430901111\ldots$$ is broken up as $$01\ 003\ 4\ 3\ 09\ 01\ 1\ 1\ldots$$. 
This is well-defined since we are ignoring representations that contain infinite sequences of zeroes.
Now instead of interleaving digits, we interleave chunks.  To interleave $$0.004999\ldots$$ and $$0.01003430901111\ldots$$, we get $$0.004\ 01\ 9\ 003\ 9\ 4\ 9\ldots$$.  This is obviously reversible. It can never produce a result that ends with an infinite sequence of zeroes, and similarly the reverse mapping can never produce a number with an infinite sequence of trailing zeroes, so we win.  A problem example similar to the one from a few paragraphs ago is resolved as follows: $$\frac12 = 0.4999\ldots$$ is the unique image of $$\langle 0.4999\ldots, 0.999\ldots\rangle$$ and $$\frac9{22} = 0.40909\ldots$$ is the unique image of $$\langle 0.40909\ldots, 0.0909\ldots\rangle$$.
This is enough to answer the question posted, but we will give some alternative approaches.
Continued fractions

According to the paper "Was Cantor Surprised?" by Fernando Q. Gouveâ, Cantor originally tried interleaving the digits himself, but Dedekind pointed out the problem of nonunique decimal representations. Cantor then switched to an argument like the one Robert Israel gave in his answer, based on continued fraction representations of irrational numbers.  He first constructed a bijection from $$(0,1)$$ to its irrational subset (see this question for the mapping Cantor used and other mappings that work), and then from pairs of irrational numbers to a single irrational number by interleaving the terms of the infinite continued fractions.  Since Cantor dealt with numbers in $$(0,1)$$, he could guarantee that every irrational number had an infinite continued fraction representation of the form 

$$

x = x_0 + \dfrac{1}{x_1 + \dfrac{1}{x_2 + \ldots}}

$$


where $$x_0$$ was zero, avoiding the special-case handling for $$x_0$$ in Robert Israel's solution.
Cantor-Schröder-Bernstein mappings

The Cantor-Schröder-Bernstein theorem takes an injection $$f:A\to B$$ and an injection $$g:B\to A$$, and constructs a bijection between $$A$$ and $$B$$.
So if we can find an injection $$f:[0,1)^2\to[0,1)$$ and an injection $$g:[0,1)\to[0,1)^2$$, we can invoke the CSB theorem and we will be done.
$$g$$ is quite trivial;  $$x\mapsto \langle x, 0\rangle$$ is one of many obvious injections.

For $$f$$ we can use the interleaving-digits trick again, and we don't have to be so careful because we need only an injection, not a  bijection. We can choose the representation of the input numbers arbitrarily; say we will take the $$0.5000\ldots$$ representation rather than the $$0.4999\ldots$$ representation. Then we interleave the digits of the two input numbers.  There is no way for the result to end with an infinite sequence of nines, so we are guaranteed an injection.
Then we apply CSB to $$f$$ and $$g$$ and we are done.
Appendix

There is a bijection from $$(-\infty, \infty)$$ to $$(0, \infty)$$.  The map $$x\mapsto e^x$$ is an example.
There is a bijection from $$(0, \infty)$$ to $$(0, 1)$$.  The map $$x\mapsto \frac2\pi\tan^{-1} x$$ is an example, as is $$x\mapsto{x\over x+1}$$.
There is a bijection from $$[0,1]$$ to $$(0,1]$$.  Have $$0\mapsto \frac12, \frac12\mapsto\frac23,\frac23\mapsto\frac34,$$ and so on. That takes care of $$\left\{0, \frac12, \frac23, \frac34,\ldots\right\}$$.  For any other $$x$$, just map $$x\mapsto x$$. 
Similarly, there is a bijection from $$(0,1]$$ to $$(0,1)$$.


