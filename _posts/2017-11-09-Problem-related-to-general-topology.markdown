---
layout: post
title: Problem related to general topology
tag:
 - general-topology

description: Problem related to general topology

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Must every subset of $$\mathbb R$$ contain $$2$$ homeomorphic distinct open sets?

<!–-break-–>


Take $$X\subseteq\mathbb R$$ containing at least $$2$$ points, we want to prove or construct a counterexample to the statement "$$X$$ contains $$2$$ distinct open sets which are homeomorphic" (where $$X$$ is equipped with the induced topology and $$\mathbb R$$ with the standard one).

we are  asking this question because it was posted as a comment to another question on MSE but the comment was deleted shortly afterward and we are  curious about the answer, if you are the person who wrote that comment and figured it out let me know.

Some thoughts: suppose that $$X$$ is a counterexample to this statement, clearly it can contain at most a single isolated point and no intervals, so $$X$$ is totally disconnected.

If $$X$$ contains no isolated points it can't be closed (or better perfect) because it'll either be homeomorphic to the Cantor set if it's also compact or $$X\cap[a,b]$$ will be homeomorphic to the Cantor set for some closed interval such that the intersection isn't empty.

A similar approach works if $$X$$ is closed and has a single isolated point.

So $$X$$ must be neither closed nor open, but we don't know how to conclude, what do totally disconnected, (almost) everywhere dense subset of $$\mathbb R$$ which are neither open nor closed look like? Or is there an entirely different (and maybe more straightforward) approach to this question?
.


# Answer 


Such subsets of the line do exist. This explicitly follows from the proof of Theorem $$2$$ of Brian M. Scott, On the existence of totally inhomogeneous spaces [PDF], Proc. Amer. Math. Soc. $$\mathbf{51}$$ $$(1975)$$, pp. $$489$$-$$493$$, since the space $$[0,1]$$ with the usual topology satisfies the hypotheses of that theorem. Indeed, the proof shows that there is a pairwise disjoint, pairwise non-homeomorphic family of $$\mathfrak{c}=2^\omega$$ such sets, each of which is dense in $$[0,1]$$. They are constructed (very non-constructively!) by transfinite recursion.
Added: In the case $$X=[0,1]$$ the argument in the paper actually produces a family $$\{R_\xi:\xi<2^\omega\}$$ of pairwise disjoint, dense subspaces of $$X$$ such that if $$\xi\le\eta<2^\omega$$, $$U$$ is a non-empty open subset of $$R_\xi$$, and $$V$$ is a non-empty open subset of $$R_\eta$$, then $$U$$ and $$V$$ are not homeomorphic. Here I’ll simplify the argument slightly to produce a single such set.
Let $$\mathscr{C}$$ be the set of continuous partial functions from $$X$$ to $$X$$. Say the $$f\in\mathscr{C}$$ is a displacement if there is an $$A\subseteq\operatorname{dom}f$$ of cardinality $$2^\omega$$ such that $$A\cap f[A]=\varnothing$$. Let 


$$

\mathscr{C}_0=\{f\in\mathscr{C}:f\text{ is a displacement and }\operatorname{dom}f\text{ is a }G_\delta\}\;;

$$


then $$\|\mathscr{C}_0\|=2^\omega$$, since $$X$$ has only $$2^\omega$$ $$G_\delta$$ subsets and is hereditarily separable, so we can index $$\mathscr{C}_0=\{f_\xi:\xi<2^\omega\}$$. By a standard result (e.g., Theorem $$\mathbf{4.3.20}$$ in Engelking’s General Topology) each displacement in $$\mathscr{C}$$ can be extended to an element of $$\mathscr{C}_0$$.
Let $$\mathscr{K}$$ be the family of compact subsets of $$X$$ of cardinality $$2^\omega$$; $$\|\mathscr{K}\|=2^\omega$$, so we can let $$\mathscr{K}=\{K_\xi:\xi<2^\omega\}$$ be an enumeration of $$\mathscr{K}$$. Let $$D=\{d_\xi:\xi<2^\omega\}$$ be an enumeration of $$2^\omega\times2^\omega$$, and let $$\tau=\{U_\xi:\xi<2^\omega\}$$ enumerate the topology $$\tau$$ of $$X$$.
Suppose that $$\eta<2^\omega$$, and points $$p_\xi,q_\xi,z_\xi\in X$$ have been chosen for $$\xi<\eta$$, and let $$d_\eta=\langle\alpha,\beta\rangle$$. Let $$A_\eta=\{p_\xi:\xi<\eta\}\cup\{q_\xi:\xi<\eta\}\cup\{z_\xi:\xi<\eta\}$$. Choose $$p_\eta\in(\operatorname{dom}f_\alpha)\setminus A_\eta$$ such that $$f_\alpha(p_\eta)\ne p_\eta$$, and if possible such that $$p_\eta\in U_\beta$$. Let $$q_\eta=f_\alpha(p_\eta)$$, and let $$z_\eta\in K_\alpha\setminus\{p_\eta,q_\eta\}$$. This is always possible, since $$f_\alpha\in\mathscr{C}_0$$, and $$\|K_\alpha\|=2^\omega$$. Let $$R=\{p_\xi:\xi<2^\omega\}\cup\{z_\xi:\xi<2^\omega\}$$; clearly $$\|R_\eta\|=2^\omega$$. 
Suppose that $$V,W\in\tau$$, $$\varnothing\ne V\cap R\ne W\cap R\ne\varnothing$$; we want to show that $$V\cap R$$ and $$W\cap R$$ are not homeomorphic, so suppose that $$h:V\cap R\to W\cap R$$ is a homeomorphism. Replacing $$h$$ by $$h^{-1}$$ if necessary, we may assume that $$(V\cap R)\setminus(W\cap R)\ne\varnothing$$. Fix $$x\in(V\cap R)\setminus(W\cap R)$$; then $$h(x)\ne x$$, so there are disjoint $$U,G\in\tau$$ such that $$x\in U\subseteq V$$, $$h(x)\in G\subseteq W$$, and $$h[U\cap R]=G\cap R$$. $$\|U\cap R\|=2^\omega$$, so $$h$$ is a displacement, and there is an $$\alpha<2^\omega$$ such that $$h=f_\alpha\upharpoonright(V\cap R)$$. $$U=U_\beta$$ for some $$\beta<2^\omega$$, and there is a $$\xi<2^\omega$$ such that $$d_\xi=\langle\alpha,\beta\rangle$$. But then $$p_\xi\in U_\beta\cap R\subseteq V\cap R$$, so $$h(p_\xi)\in W\cap R$$, but $$h(p_\xi)=f_\alpha(p_\xi)=q_\xi\notin R$$. This contradiction shows that no such homeomorphism $$h$$ can exist.

