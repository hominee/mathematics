---
layout: post
title: Does the open mapping theorem imply the Baire category theorem
tag:
 - functional-analysis
 - set-theory
 - banach-spaces
 - axiom-of-choice
 - baire-category

description: Does the open mapping theorem imply the Baire category theorem

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Does the open mapping theorem imply the Baire category theorem?

<!–-break-–>


A nice observation by C.
E.
 Blair1, 2, 3 shows that the Baire category theorem for complete metric spaces is equivalent to the axiom of (countable) dependent choice.

On the other hand, the three classical consequences of the Baire category theorem in basic functional analysis — the open mapping theorem, the closed graph theorem and the uniform boundedness principle (as well as Zabreiko's lemma) — are equivalent to each other in Zermelo–Fraenkel set theory without choice: that is to say, if one is added as an axiom to ZF then the others follow4.

Each of these results has a more or less direct proof from the Baire category theorem and all the proofs “avoiding Baire” we are  aware of5 involve dependent choice in a way that doesn't seem to be replaceable by weaker forms of choice.

Hence we are  asking about the converse:

Does the open mapping theorem imply the Baire category theorem? 
If not, is it at least true that the open mapping theorem implies the axiom of dependent choice for subsets of the reals?

we imagine that applying any of the above results to a judiciously chosen space and/or operator(s) might yield the desired conclusion, similarly to what happens in Bell's and Fremlin's geometric version of the axiom of choice6.
 Unfortunately, we couldn't find a promising place to start.

Needless to say that we checked numerous things on the web form of Howard and Rubin's book Consequences of the Axiom of Choice, but without much success: The only articles that we found this way are J.
D.
 Maitland Wright's articles7.


Footnotes and References:
1 Charles E.
 Blair, The Baire category theorem implies the principle of dependent choices, Bull.
 Acad.
 Polon.
 Sci.
 Sér.
 Sci.
 Math.
 Astronom.
 Phys.
 25 (1977), no.
 10, 933–934.

2 Since Blair's article is hard to find, the proof can be found in the notes to chapter 9, page 95 of John C.
 Oxtoby, Measure and Category, Springer GTM 2, Second 

**Edit**ion, 1980.

3 Here's the idea of Blair's argument for the implication Baire Category Theorem $$\Rightarrow$$ Dependent Choice: let $$S$$ be a set and let $$R \subset S \times S$$ be a relation such that for all $$s \in S$$ there exists $$t \in S$$ such that $$(s,t) \in R$$.
 Equip $$S^{\mathbb{N}}$$ with the complete metric $$d(f,g) = 2^{-\min\{n\,:\,f(n)\neq g(n)\}}$$, put


$$


U_n = \bigcup_{m = n+1}^{\infty} \bigcup_{(s,t) \in R} \{f \in S^{\mathbb{N}}\,:\,f(n) = s, \,f(m)=t\},


$$


observe that $$U_n$$ is open and dense and use $$f \in \bigcap_{n=1}^\infty U_n$$ and the well-order on $$\mathbb{N}$$ to find a strictly increasing sequence $$k_1 \lt k_2 \lt \cdots$$ such that the sequence $$(x_n)_{n=1}^\infty$$ given by $$x_n = f(k_n)$$ satisfies $$(x_n, x_{n+1}) \in R$$ for all $$n \in \mathbb{N}$$.

4 See e.
g.
 E.
 Schechter, Handbook of Analysis and its foundations, 27.
27, pp.
 734ff.

5 A good example for this is Sokal's A Really Simple Elementary Proof of the Uniform Boundedness Theorem, The American Mathematical Monthly
Vol.
 118, No.
 5 (May 2011), pp.
 450–452, ArXiV Version.
 While admittedly it is beautifully simple and elementary, it involves a plain application of dependent choice in the main argument.

6 Bell and Fremlin, A Geometric Form of the Axiom of Choice, Fund.
 Math.
 vol.
 77 (1972), 167–170.

7 The full list of relevant articles can be obtained with this ZBlatt query two of which appeared in rather obscure proceedings, so we couldn't get my hands on them, yet.
 The third article is J.
 D.
 Maitland Wright, All operators on a Hilbert space are bounded, Bull.
 Amer.
 Math.
 Soc.
 79 (1973), 1247–1250.


# Answer 




**Edit** after more than a year:
At least, the uniform boundedness principle can be proven using only the axiom of countable choice, or $$\mathbf{CC}$$ for short. However, we have been unable to find a proof for the fact that any of the three facts

Every Banach space is barrelled
On a Banach space, a lower semi-continuous seminorm is always continuous
The uniform boundedness principle

implies either the closed graph theorem or the open mapping theorem (however, the two are equivalent in ZF). In particular, the argument in 27.37 of Schechter uses dependent choice, seemingly in an essential way.
Here is the sketch for $$\mathbf{CC} \Rightarrow$$ UBP:
We first note that for a linear operator $$T$$,


$$


\max\{\|T(x - y)\|, \|T(x + y)\|\} \ge 1/2 (\|T(x - y)\| + \|T(x + y)\|) \ge \|T(y)\|


$$


due to the triangle inequality $$\|a - b\| \le \|a\| + \|b\|$$.
Instead of applying the axiom of dependent choice, we first pick a sequence of operators $$\|T_n\| \ge 4^n$$ and


$$


x_n \in \left\{x \in X \middle\| \|x\| \le 1 \text{ and } \|T_n(x)\| \ge 2/3 \|T_n\|\right\} =: S_n


$$


using countable choice. Then, since dependent choice with a function instead of a relation is a theorem of ZF, we define a function which maps $$(y_n, n)$$ to $$(y_{n+1}, n+1)$$ where


$$


y_{n+1} = \begin{cases}
y_n - 3^{-(n+1)} x_{n+1} & \|T_{n+1}(x_{n+1} - 3^{-(n+1)} x_{n+1})\| \ge \frac{2}{3} 3^{-(n+1)} \|T_{n+1}\| \\
y_n + 3^{-(n+1)} x_{n+1} & \text{otherwise}.
\end{cases}


$$


If we set $$y_1 := 1/3 x_1$$, then we may define a sequence from the repeated application of that function. The key lemma of Sokal's ensures that $$\|T_n(y_n)\| \ge \frac{2}{3} 3^{-n} \|T_n\|$$ for all $$n \in \mathbb N$$. From the triangle inequality follows if $$k > n$$


$$


\|y_n - y_k\| \le \sum_{j=n}^\infty \|y_j - y_{j+1}\| \le \sum_{j=n}^\infty \frac{2}{3} 3^{-(j+1)} \le \frac{1}{2} 3^{-n}


$$


Thus, $$(y_l)_{l \in \mathbb N}$$ is Cauchy (with limit $$y$$, say), and it also follows that


$$


\|T_n(y)\| \ge \left\| \|T_n(y_n)\| - \|T_n(y - y_n)\| \right\| \ge 1/6 (4/3)^n.


$$



