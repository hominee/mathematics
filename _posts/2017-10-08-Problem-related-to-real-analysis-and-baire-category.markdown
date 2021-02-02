---
layout: post
title: Problem related to real analysis and baire category
tag:
 - real-analysis
 - general-topology
 - analysis
 - baire-category

description: Problem related to real analysis and baire category

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is $$[0,1]$$ a countable disjoint union of closed sets?

<!–-break-–>


Can you express $$[0,1]$$ as a countable disjoint union of closed sets, other than the trivial way of doing this?
.

# Answer 


The answer is no. In fact, as Steve D said, we have a theorem that holds for a wide class of spaces, which includes closed intervals, circles, balls and cubes. It was proved by Sierpiński in $$1918$$ $$[1]$$. You can find the proof in the book "General Topology" by Ryszard Engelking, but I'll post here since it's not easy to find it online. First a definition: a topological space is called a continuum if it is a compact connected Hausdorff space. The precise statement is the following:
Theorem (Sierpiński). If a continuum $$X$$ has a countable cover $$\{X_i\}_{i=1}^{\infty}$$ by pairwise disjoint closed subsets, then at most one of the sets $$X_i$$ is non-empty.
In order to prove this we'll need the following lemmas:

**Lemma** $$1$$. Let $$X$$ be a continuum. If $$F$$ is a non-trivial closed subset of $$X$$, then for every component $$C$$ of $$F$$ we have that $$\text{Bd}(F) \cap C$$ is non-empty.

**Proof.** Let $$x_0$$ be in $$C$$. Since $$X$$ is Hausdorff compact, quasicomponents coincide with components, so $$C$$ is the intersection of all open-closed sets in $$F$$ which contain $$x_0$$. Suppose that $$C$$ is disjoint from $$\text{Bd}(F)$$. Then, by compactness of $$\text{Bd}(F)$$, there is one open-closed set $$A$$ in $$F$$ containing $$x_0$$ and disjoint from $$\text{Bd}(F)$$. Take an open set $$U$$ such that $$A = U \cap F$$. Thus the equality $$A \cap \text{Bd}(F) = \emptyset$$ implies that $$A = U \cap \text{Int}(F)$$, so $$A$$ is open in $$X$$. But $$A$$ is also closed in $$X$$, and contains $$x_0$$, so $$A=X$$. But then $$\text{Bd}(F) = \emptyset$$, which is not possible since $$F$$ would be non-trivial open-closed in $$X$$. $$\bullet$$

**Lemma** $$2$$. If a continuum $$X$$ is covered by pairwise disjoint closed sets $$X_1, X_2, \ldots$$ of which at least two are non-empty, then for every $$i$$ there exists a continuum $$C \subseteq X$$ such that $$ C \cap X_i = \emptyset$$ and at least two sets in the sequence $$C \cap X_1, C \cap X_2, \ldots$$ are non-empty.

**Proof**. If $$X_i$$ is empty then we can take $$C = X$$; thus we can assume that $$X_i$$ is non-empty. Take $$j \ne i$$ such that $$X_j \ne \emptyset$$. Since $$X$$ is Hausdorff compact, there are disjoint open sets $$U,V \subseteq X$$ satisfying $$X_i \subseteq U$$ and $$X_j \subseteq V$$. Let $$x$$ be a point of $$X_j$$ and $$C$$ the component of $$x$$ in the subspace $$\overline{V}$$. Clearly, $$C$$ is a continuum, $$ C \cap X_i = \emptyset$$ and $$ C \cap X_j \ne \emptyset$$. By the previous lemma, $$C \cap \text{Bd}( \overline{V}) \ne \emptyset$$ and since $$X_j \subseteq \text{Int}(\overline{V})$$, there exist a $$k \ne j$$ such that $$C \cap X_k \ne \emptyset$$. $$\bullet$$

Now we can prove the theorem:

**Proof**. Assume that at least two of the sets $$X_i$$ are non-empty. From lemma $$2$$ it follows that there exists a decreasing sequence $$C_1 \supseteq C_2 \ \supseteq \ldots$$ of continua contained in $$X$$ such that $$C_i \cap X_i = \emptyset$$ and $$C_i \ne \emptyset$$ for $$i=1,2, \ldots$$ The first part implies that $$\bigcap_{i=1}^{\infty} C_i = \emptyset$$ and from the second part and compactness of $$X$$ it follows that $$\bigcap_{i=1}^{\infty} C_i \ne \emptyset$$. $$\bullet$$
The Hausdorff hypothesis is fundamental. For example, consider $$X$$ a countable infinite set with the cofinite topology. Then $$X$$ is compact, connected and a $$T_1$$-space. However, we can write $$X$$ as a disjoint union of countable singletons, which are closed.

$$[1]$$ Sierpiński, W: Un théorème sur les continus, Tôhoku Math. J. 13 (1918), 300–305.

