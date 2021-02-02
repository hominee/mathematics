---
layout: post
title: Direct approach to the Closed Graph Theorem
tag:
 - functional-analysis
 - banach-spaces
 - alternative-proof

description: Direct approach to the Closed Graph Theorem

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Direct approach to the Closed Graph Theorem

<!–-break-–>


In the context of Banach spaces, the Closed Graph Theorem
and the Open Mapping Theorem are equivalent.

It seems that usually one proves the Open Mapping Theorem using the
Baire Category Theorem, and then, from this theorem, proves the
Closed Graph Theorem.

we was wondering about a more direct approach to the
Closed Graph Theorem.

What we want to show, possibly using the Baire Category Theorem,
but without the Closed Graph Theorem or any of its equivalent
theorems, that if $$T: X \to Y$$ is not continuous, then,
there is a convergent sequence $$x_n \rightarrow x$$ such that
$$T x_n \rightarrow y \neq Tx$$.

Of course, $$X$$ and $$Y$$ are Banach Spaces.

Because $$T$$ is not bounded, we know that there is a sequence $$a_n$$ of
unitary vectors such that $$T a_n \rightarrow \infty$$.

Now, taking $$b_n = \frac{a_n}{\|T a_n\|}$$, we have that
$$b_n \rightarrow 0$$, and $$\|T b_n\| = 1$$.

we wonder, if there is a simple argument for constructing a
$$x_n \rightarrow x$$, based on $$a_n$$ or $$b_n$$, such that
$$T x_n$$ is a Cauchy Sequence, but such that
$$\|T x_n\|$$ is "far from" $$\|T x\|$$.

Of course, $$x_n$$'s construction would have to use the fact that
$$X$$ is complete.

For example, $$x$$ could be the limit of an absolutely convergent sequence,
pretty much in the same fashion as the construction in the proof of the
Open Mapping Theorem.


# Answer 


Zabreiko's lemma (from P. P. Zabreiko, A theorem for semiadditive functionals, Functional analysis and its applications 3 (1), 1969, 70–72) is not as well known as it deserves to be and we think it fits the bill to some extent, so let me state that result first:

Lemma (Zabreiko, 1969) Let $$X$$ be a Banach space and let $$p: X \to [0,\infty)$$ be a seminorm. If for all absolutely convergent series $$\sum_{n=0}^\infty x_n$$ in $$X$$ we have 
  

$$


p\left(\sum_{n=0}^\infty x_n\right) \leq \sum_{n=0}^\infty p(x_n) \in [0,\infty]


$$


  then $$p$$ is continuous. That is to say, there exists a constant $$C \geq 0$$ such that $$p(x) \leq C\|x\|$$ for all $$x \in X$$.

Assuming this lemma, let $$T: X \to Y$$ be a discontinuous linear map between Banach spaces, consider the seminorm $$p(x) = \|Tx\|$$ and observe that there must exist an absolutely summable sequence $$(x_n)_{n=0}^\infty$$ and $$\varepsilon \gt 0$$ such that


$$


p\left(\sum_{n=0}^\infty x_n\right) \geq \sum_{n=0}^\infty p(x_n) + \varepsilon.


$$


Since the left hand side is finite, both $$a_{N} = \sum_{n=1}^N x_n$$ and $$b_N = Ta_N$$ are Cauchy sequences with limits $$a$$ and $$b$$, respectively. We have  $$\|b_N\| \leq \|T(a)\| - \varepsilon$$, so $$\|T(a) - b_N\| \geq \varepsilon$$ for all $$N$$ and thus $$\|T(a) - b\| \geq \varepsilon$$. In other words $$(a_N,T(a_N)) \to (a,b)$$ but $$b \neq T(a)$$, so the graph of $$T$$ is not closed.

Of course, we should make the disclaimer that Zabreiko's lemma is actually stronger than the usual consequences of the Baire category theorem in basic functional analysis and thus it does not answer the question as asked. As you mention in your question, as soon as the closed graph theorem is established, the inverse mapping theorem and the open mapping theorem follow easily, as we also explain in this thread. Moreover, the uniform boundedness principle is a straightforward consequence, too: 
Exercises:
Use Zabreiko's lemma to prove:

the uniform boundedness principle;
Hint: set $$p(x) = \sup_{n \in \mathbb{N}} \|T_n x\|$$.
the inverse mapping theorem.
Hint: set $$p(x) = \|T^{-1}x\|$$.


The proof of Zabreiko's lemma is very similar to the usual proof by Banach–Schauder of the open mapping theorem:
Proof. Let $$A_n = \{x \in X\,:\,p(x) \leq n\}$$ and $$F_n = \overline{A_n}$$. 

**Note** that $$A_n$$ and $$F_n$$ are symmetric and convex because $$p$$ is a seminorm. We have $$X = \bigcup_{n=1}^\infty F_n$$ and Baire's theorem implies that there is $$N$$ such that the interior of $$F_N$$ is nonempty. 
Therefore there are $$x_0 \in X$$ and $$R \gt 0$$ such that $$B_R(x_0) \subset F_N$$. By symmetry of $$F_N$$ we have $$B_{R}(-x_0) = -B_{R}(x_0) \subset F_n$$, too. If $$\|x\| \lt R$$ then $$x+x_0 \in B_{R}(x_0)$$ and $$x-x_0 \in B_{R}(-x_0)$$, so $$x \pm x_0 \in F_{N}$$. By convexity of $$F_N$$ it follows that 


$$


x = \frac{1}{2}(x-x_0) + \frac{1}{2}(x+x_0) \in F_N, 


$$


so $$B_R(0) \subset F_N$$.
Our goal is to establish that 


$$


\begin{equation*}\tag{*}
B_{R}(0) \subset A_N
\end{equation*}


$$


because then for $$x \neq 0$$ we have with $$\lambda = \frac{R}{\|x\|(1+\varepsilon)}$$ that $$\lambda x \in B_{R}(0) \subset A_N$$, so $$p(\lambda x) \leq N$$ and thus $$p(x) \leq \frac{N(1+\varepsilon)}{R} \|x\|$$, as desired.
Proof of $$(\ast)$$. Suppose $$\|x\| \lt R$$ and choose $$r$$ such that $$\|x\| \lt r \lt R$$. Fix $$0 \lt q \lt 1-\frac{r}{R}$$, so $$\frac{1}{1-q} \frac{r}{R} \lt 1$$. Then
$$y = \frac{R}{r}x \in B_{R}(0) \subset F_N = \overline{A_N}$$, 
so there is $$y_{0} \in A_N$$ such that $$\|y-y_0\| \lt qR$$, 
so $$q^{-1}(y-y_0) \in B_R$$. 
Now choose $$y_1 \in A_N$$ 
with $$\|q^{-1}(y-y_0) - y_1\| \lt q R$$,
so $$\|(y-y_0 - qy_1)\| \lt q^2 R$$. By induction we obtain a sequence $$(y_k)_{k=0}^\infty \subset A_N$$ such that


$$


\left\| y - \sum_{k=0}^n q^k y_k\right\| \lt q^n R \quad \text{for all }n \geq 0,


$$


hence $$y = \sum_{k=0}^\infty q^k y_k$$. Observe that by construction $$\|y_n\| \leq R + qR$$ for all $$n$$, so the series $$y = \sum_{k=0}^\infty q^k y_k$$ is absolutely convergent. But then the countable subadditivity hypothesis on $$p$$ implies that


$$


p(y) = p\left(\sum_{k=0}^\infty q^k y_k\right) \leq \sum_{k=0}^\infty q^k p(y_k) \leq \frac{1}{1-q} N


$$


and thus $$p(x) \leq \frac{r}{R} \frac{1}{1-q} N \lt N$$ which means $$x \in A_N$$, as we wanted.

Added: A version of this answer appeared on the Mathematics Community Blog. Thanks to Norbert and others for their efforts.

