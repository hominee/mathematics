---
layout: post
title: Baire Category Theorem without Completeness
tag:
 - real-analysis
 - functional-analysis
 - metric-spaces
 - examples-counterexamples
 - baire-category

description: Baire Category Theorem without Completeness

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Baire Category Theorem without Completeness

<!–-break-–>


Let $$(X,d)$$ be a metric space.
 
We say that $$Y \subseteq X$$ is dense in $$X$$ if for any non-empty open set $$U\subseteq X,$$ we have $$U \cap Y \neq \emptyset.
$$
Baire Category Theorem states that 

If $$(X,d)$$ is a complete metric space with $$(U_n)_{n \in \mathbb{N}}$$ being a sequence of open dense sets in $$X,$$ then their intersection $$\bigcap_{n \in \mathbb{N}}U_n$$ is dense in $$X.
$$

If we remove openness in the condition, then the theorem will not hold anymore, simply let $$X = \mathbb{R},$$ $$U_1 = \mathbb{Q}$$ and $$\mathbb{R} \setminus \mathbb{Q}.
$$
Clearly $$X$$ is complete and $$U_1$$ and $$U_2$$ are dense in $$X,$$ but $$U_1 \cap U_2 = \emptyset$$ is not dense in $$X.
$$

Question: Give an example such that $$X$$ is not complete with $$(U_n)_{n \in \mathbb{N}}$$ a sequence of open dense sets but their intersection $$\bigcap_{n \in \mathbb{N}}U_n$$ is not dense in $$X.
$$

we have been trying to come out with an example that satisfies the question above.

Since finite dimensional space is always complete, we have to let $$X$$ be infinite dimensional.
 
One example that comes to my mind is $$C[0,1],$$ the set of continuous functions on $$[0,1].
$$ 
However, we do not know which set is dense in $$C[0,1].
$$
Any hint would be appreciated.


# Answer 


Let $$X$$ be a countable $$T_1$$ space without isolated points.
Then $$D_x = X\setminus \{x\}$$ is open (as $$\{x\}$$ is closed by $$T_1$$-ness), and dense (it's not closed as $$\{x\}$$ is not open, so its closure is $$X$$).
Then $$\emptyset = \cap\{D_x: x \in X\}$$ is a countable intersection of dense open sets of $$X$$, and it's far from dense.
The only metrisable example of such a space is $$\mathbb{Q}$$ (in its metric topology, inherited from $$\mathbb{R}$$).

