---
layout: post
title: Problem related to real analysis and proof writing
tag:
 - real-analysis
 - integration
 - proof-verification
 - proof-writing

description: Problem related to real analysis and proof writing

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

If $$g$$ is Riemann-integrable in a closed interval and $$f$$ is a increasing function in a closed interval, is $$g\circ f$$ Riemann-integrable?

<!–-break-–>



If $$g$$ is Riemann-integrable in a closed interval and $$f$$ is a increasing function in a closed interval, is $$g\circ f$$ Riemann-integrable?

To clarify: the problem stated that the composition is well defined.
 we think that the statement of the question is true but Im having trouble to write/concrete a proof.

we know that a monotone function defined in a closed interval is Riemann-integrable by a previous result.
 And we know that the reverse statement ($$g$$ being monotone and $$f$$ integrable) is not true in general.

After thinking some moment my idea for the proof is to show that $$g\circ f$$ have, at most, countable discontinuities.
 To do this we was thinking how to show some kind of order-correspondence between the points of the domain of a monotone function and it image.
 Some hint will be appreciated.



**Edit**: we get a new idea, design a partition of $$f$$ that take any possible discontinuity into a closed interval of known length, and after see what happen in the composition with this closed intervals with discontinuities, and by the other hand see what happen with the parts of continuous mapping.


After reading this answer we get the idea to provide a proof for the validity of the statement.

First we will characterize the different kind of images of closed intervals that a monotonic function can create.
 For an increasing function we have that $$x<y$$ implies that $$f(x)\le f(y)$$, and that at most a monotone function can have a countable number of discontinuities in any closed interval.

No discontinuities on the image: if the image of $$f([x_1,x_2])$$ is continuous then it can be at most of three types: 

A constant function $$f([x_1,x_2])=\{a\}$$.
 Then $$(g\circ f)([x_1,x_2])=g(\{a\})=\{c\}$$, then the function $$(g\circ f)$$ is constant in $$[x_1,x_2]$$ so is Riemann-integrable
A strictly increasing function i.
e.
 $$f([x_1,x_2])=[a,b]$$.
 Then $$(g\circ f)([x_1,x_2])=g([a,b])=[c,d]$$.
 If $$g$$ is Riemann integrable in $$[a,b]$$ then exists a sequence of partitions $$(P_n)$$ such that



$$

\lim_{n\to\infty}U(g,P_n)-L(g,P_n)=0

$$


Then because $$f$$ is bijective in $$[a,b]$$ then for every $$P_n$$ exists a partition $$P'_n$$ in $$[x_1,x_2]$$ such that


$$

\lim_{n\to\infty}U(g\circ f,P'_n)-L(g\circ f,P'_n)=0

$$


so $$g\circ f$$ is Riemann-integrable in $$[x_1,x_2]$$

A mix of both previous cases.
 Then the interval $$[x_1,x_2]$$ can be partitioned on types of subintervals discussed previously (constant and strictly monotonic images), so $$g\circ f$$ is Riemann-integrable here too.


Discontinuity in the image: a jump discontinuity in $$[x_1,x_2]$$ is mapped into two types of the previously discussed intervals with the difference that can be the case that in the image exists an interval with an open boundary of the kind $$[a,b)$$ or $$(a,b]$$.

But cause $$f$$ and $$g$$ are Riemann integrable in closed intervals this mean that they are bounded, and if $$g$$ is integrable in any subinterval $$[a-\varepsilon,b]$$ then is integrable in $$(a,b]$$ (this is known by a previous proof).



**Edit** 2: as the user @ParamanandSingh pointed in the comments it is possible that the discontinuities cannot be isolated, one by one, inside some interval.
 So we will search further for a correct proof of the statement.


# Answer 


we will try to explain the counterexample provided in ParamanandSingh's math overflow link. We will need a few prerequisites but they're hopefully not too advanced.

Null Set/Measure Zero Set: A null set $$N \subset \mathbb{R}$$, also called a measure zero set, is a set that can be convered by a countable union of intervals with arbitrarily small total length. See this wikipedia link.

Measure zero here anticipates the Lebesgue measure for the reals. The Lebesgue measure assigns 'length' to sets of the real line in the natural/expected way. There's technicalities involved, but all we'll really need from it is that the measure of an interval with endpoints $$a<b$$ is $$(b-a)$$.

Lebesgue Criterion (for Riemann integrability): A bounded function on a compact interval is Riemann-integrable if and only if its set of discontinuities has measure zero. See this wikipedia link.

This criterion characterizes how 'small' a function's set of discontinuities needs to be for that function to be Riemann-integrable. It is a standard (though not trivial) result with many proofs lying around; no measure theory is needed!

Cantor and Fat Cantor Sets: The standard, ternary Cantor set has measure zero; see this wikipedia link. There are Cantor sets with positive measure; for instance, the Smith-Volterra-Cantor set.

We can deduce these using lenghts of intervals! Let $$C$$ be the ternary Cantor set.
At the first step, we delete an interval of length $$1/3$$ from $$C_0=[0,1]$$, obtaining $$C_1$$. At the second step, we delete two intervals, each of which has length $$1/9$$, from $$C_1$$, obtaining $$C_2$$. More generally, at the $$n$$-th step we delete $$2^{n-1}$$ intervals, each of which has length $$3^{-n}$$, from $$C_{n-1}$$, obtaining $$C_n$$.
Thus, the total length deleted this way is 

$$

\sum_{n=1}^{\infty}\frac{1}{2}{\left(\frac{2}{3}\right)}^n=\frac{1}{2}\frac{\frac23}{1-\frac23}=1

$$


which is the length of $$[0,1]$$, the interval we began with. It follows that the ternary Cantor set $$C$$ -- what remains after all deletions -- has measure zero.
Calculations for the Smith-Volterra-Cantor set $$S$$ are similar. At the $$n$$-th step, $$2^{n-1}$$ intervals, each of which has length $$2^{-2n}$$, are deleted from $$S_{n-1}$$, obtaining $$S_n$$. Therefore, the total length deleted this way is 

$$

\sum_{n=1}^{\infty}\frac{1}{2}\frac{2^n}{2^{2n}}=\frac{1}{2}\sum_{n=1}^{\infty}\frac{1}{2^n}=\frac{1}{2}\frac{\frac12}{1-\frac12}=\frac12

$$


The measure of $$S$$ is simply $$1$$ (the measure of $$[0,1]$$, the interval we began with) minus $$\frac12$$ (the total measure of what we discarded), that is, $$S$$ has measure $$\frac12$$. In particular, it has positive measure and is not a null set.

Now that we have the prerequisites, let's dive onto the counterexample. First, let $$f:[0,1]\longrightarrow \mathbb{R}$$ be the characteristic function of the ternarcy Cantor set $$C$$, that is:

$$
\begin{equation*}
f(x)=\begin{cases}
1&\text{if} x \in C\\
0&\text{if} x \notin C
\end{cases}
\end{equation*}
$$

Notice that $$f$$ has discontinuities precisely on $$C$$; a good way to see this is to notice that at each step in the construction of $$C$$, $$f$$ is defined to be $$0$$ on the deleted intervals (so it is clearly continuous in their interior) It follows by the Lebesgue Criterion that $$f$$ is Riemann-integrable.

Finally, we will define a monotone increasing function $$g:[0,1] \longrightarrow \mathbb{R}$$ that maps the Smith-Volterra-Cantor set $$S$$ to $$C$$. We will obtain $$g$$ as the limit of a sequence of functions.

Let $$S_0=C_0=[0,1]$$, let $$S_n$$ be what remains in the construction of $$S$$ after $$n$$ steps, and similarly for $$C_n$$. Notice that each of $$S_n$$ and $$C_n$$ is a disjoint union of $$2^n$$ closed non-degenerate intervals; we may describe each of them by its collection of $$2^{n+1}$$ endpoints. For instance, in the obvious notation $$C_0=S_0\sim\{0,1\}$$, $$C_1\sim\left\{0,\frac13,\frac23,1\right\}$$ and $$S_1\sim\left\{0,\frac38,\frac58,1\right\}$$.

Define $$g_n:[0,1]\longrightarrow\mathbb{R}$$ as follows. Let $$S_n\sim\{s_k\}$$, where $$k$$ ranges from $$1$$ to $$2^{n+1}$$ and the $$s_k$$ are increasing. Similarly, let $$C_n\sim \{c_k\}$$. For all $$k=1,\dots,2^{n+1}$$ put $$g_n(s_k)=c_k$$, and extend it to all of $$[0,1]$$ linearly. In other words, $$g_n$$ fits the $$i$$-th interval in $$S_n$$ into the $$i$$-th interval in $$C_n$$, and fills in the blanks with linear pieces. It's easy to see that $$g_n$$ is increasing (and continuous!) for all $$n$$.

It's not too hard to see that $$g_n$$ converges pointwise for all $$x \in [0,1]$$; we define $$g$$ to be this limit function. It follows immediately that $$g$$ is increasing and maps $$S$$ to $$C$$. (It's a bit of work, but one can show that the convergence $$g_n\to g$$ is actually uniform, so that $$g$$ is indeed continuous!)

At last, the composition $$f\circ g$$ has $$S$$ for its set of discontinuities. Since $$S$$ has positive measure, it follows by the Lebesgue criterion that $$f\circ g$$ is not Riemann-integrable, which concludes the proof.

