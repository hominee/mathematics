---
layout: post
title: Does convexity of a 'norm' imply the triangle inequality
tag:
 - functional-analysis
 - analysis
 - vector-spaces
 - convex-analysis
 - norm

description: Does convexity of a 'norm' imply the triangle inequality

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Does convexity of a 'norm' imply the triangle inequality?

<!–-break-–>


Given a vector space $$V$$ (for convenience, defined over $$\mathbb{r}$$), we call $$d:V\rightarrow\mathbb{R}$$ a norm for $$V$$ if $$\forall \mathbf{u}, \mathbf{v} \in V$$ and $$\forall r \in \mathbb{R}$$ we have:

$$d(r \mathbf{v}) = \|r\|d(\mathbf{v})$$,
$$d(\mathbf{v})\ge 0$$, with equality iff $$\mathbf{v} = 0$$, and
$$d(\mathbf{u})+d(\mathbf{v}) \ge d(\mathbf{u}+\mathbf{v})$$ (triangle inequality)

we have  read in a few places that an important property of a norm is that it is convex; that is, given $$\mathbf{u},\mathbf{v} \in V$$, and $$p \in (0,1)$$, we have $$d(p \mathbf{u} + (1-p) \mathbf{v}) \le p d(\mathbf{u}) + (1-p) d(\mathbf{v})$$.
  This clearly follows from the triangle inequality.

My question is: Does the reverse also hold?  i.
e.
 does a function satisfying (1) and (2) above which is convex necessarily satisfy the triangle inequality?  If not, what is an instructive counterexample?
Thanks! (btw: please feel free to suggest better tags / improvements to the question; we are  new to this!)
.


# Answer 


Resolved in comments.
Setting $$p=\frac12$$ in the definition of convexity, we have


$$


d\Big( \frac{\mathbf u + \mathbf v}{2} \Big) \leqslant \frac12 d(\mathbf u) + \frac12 d(\mathbf v).


$$


By the scaling or homogeneity, the left hand side is simply $$\frac12 d(\mathbf u + \mathbf v)$$; plugging in this and simplifying, we get the triangle inequality. 

