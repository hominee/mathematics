---
layout: post
title: Problem related to real analysis and isometry
tag:
 - real-analysis
 - general-topology
 - analysis
 - contest-math
 - isometry

description: Problem related to real analysis and isometry

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Let, $$A\subset\mathbb{R}^2$$. Show that $$A$$ can contain at most one point $$p$$ such that $$A$$ is isometric to $$A \setminus \{p\}$$.

<!–-break-–>


A challenge problem from Sally's Fundamentals of Mathematical Analysis.


Problem reads: Suppose $$A$$ is a subset of $$\mathbb{R}^2$$.
 Show that $$A$$ can contain at most one point $$p$$ such that $$A$$ is isometric to $$A \setminus \{p\}$$ with the usual metric.


we are  really not sure where to begin.
 we have  found a fairly trivial example of a set for which this is true: let $$A$$, for example, be $$\{(n,0) : n \in \{0\} \cup \mathbb{Z}^+\}$$.
 Then we may remove the point $$(0,0)$$ and construct the isometry $$f(n,0) = (n+1, 0)$$.
 This is clearly an isometry because $$d((n,0),(m,0)) = d((n+1,0),(m+1,0))$$, in other words, we are just shifting to the right.
 But now suppose we remove some $$(p,0) \neq (0,0)$$.
 Then we must have $$d((m,0), (m+1,0)) = 1$$ for all points $$(m,0), (m+1,0)$$, but since $$(p,0)$$ was removed we will always have a "jump" point where the distance between two successive points is $$2$$.

But we are  not sure where to proceed.
 Isometries are equivalence relations, so maybe we can show that if $$A \setminus \{p\}$$ is isometric to $$A \setminus \{q\}$$, then $$p = q$$? 
we will say that given how often Sally's errant in his book and that some of the other challenge problems are open problems, this might not have a reasonable solution (if it's even true).
 
Any ideas?

To avoid any confusion, the problem isn't asking a proof for the set not being isometric to itself minus two points at the same time.
 It's asking for a proof that there is at most one unique point that you can remove from the set and then create an isometry.
 This was something we misinterpreted for a while.




**Edit**: This is still stumping me.
 we are  beginning to wonder whether it's even true at all.
 Well, we have  put a bounty on it, which hopefully serves as bit more incentive to try this problem out!
.


# Answer 


This is not a formal answer to question. But just to let future readers and the OP know that a brilliant and detailed  solution to this problem can be found Here in mathobverflow.
This was prosed by @Ycor.

