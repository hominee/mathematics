---
layout: post
title: A finite set always has a maximum and a minimum.
tag:
 - real-analysis
 - elementary-set-theory
 - order-theory

description: A finite set always has a maximum and a minimum.

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A finite set always has a maximum and a minimum.

<!–-break-–>


we are  pretty confident that this statement is true. However, we are  not sure how to prove it. Any hints/ideas/answers would be appreciated.

# Answer 


Let $$S = \{s_1, \ldots,s_n\}$$ be a nonempty finite set of size $$n > 0$$. We will show by induction on $$n \in \mathbb N$$ that there exist some $$m,M \in S$$ such that for all $$s \in S$$, we have that $$m \leq s \leq M$$.
Base Case: For $$n=1$$, we have $$S = \{s_1\}$$, so taking $$m = s_1$$ and $$M=s_1$$ trivially satisfies the required condition.
we nduction Hypothesis: Assume that the claim holds for $$n=k$$, where $$k \geq 1$$.
we t remains to prove that the claim holds true for $$n = k+1$$. To this end, choose any set $$S$$ with $$k+1$$ elements, say $$S = \{s_1 ,\ldots,s_k,s_{k+1}\}$$. Now by the induction hypothesis, the subset:

 $$ 

S' = S \setminus \{s_{k+1}\} = \{s_1 ,\ldots,s_k\}

 $$ 

has a minimum element and a maximum element. That is, we know that there exists some $$m',M' \in S'$$ such that for all $$s' \in S'$$, we have that $$m' \leq s' \leq M'$$. Now observe that $$s_{k+1}$$ must fall under $$1$$ of $$3$$ cases:
Case 1: Suppose that $$s_{k+1} < m'$$. Then take $$m = s_{k+1}$$ and $$M=M'$$. To see why this works, observe that any element in $$S$$ is either $$s_{k+1}$$ or some $$s' \in S'$$, and:

 $$ 

m = s_{k+1} < m' \leq s' \leq M' =M

 $$ 

Case 2: Suppose that $$m' \leq s_{k+1} \leq M'$$. Then take $$m = m'$$ and $$M=M'$$. To see why this works, observe that any element in $$S$$ is either $$s_{k+1}$$ or some $$s' \in S'$$, and:

 $$ 

m = m' \leq s_{k+1} \leq M' = M

 $$ 


 $$ 

m = m' \leq s' \leq M' = M

 $$ 

Case 3: Suppose that $$s_{k+1} > M'$$. Then take $$m =m'$$ and $$M=s_{k+1}$$. To see why this works, observe that any element in $$S$$ is either $$s_{k+1}$$ or some $$s' \in S'$$, and:

 $$ 

m = m' \leq s' \leq M' < s_{k+1} = M

 $$ 

Hence, we have shown that $$S$$ has a minimum and maximum element, as desired.

