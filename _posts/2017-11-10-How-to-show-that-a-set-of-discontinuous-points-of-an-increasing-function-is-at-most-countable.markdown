---
layout: post
title: How to show that a set of discontinuous points of an increasing function is at most countable
tag:
 - real-analysis

description: How to show that a set of discontinuous points of an increasing function is at most countable

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to show that a set of discontinuous points of an increasing function is at most countable

<!–-break-–>


we would like to prove the following:  

Let $$g$$ be a monotone increasing function on $$[0,1]$$.
 Then the set of points where $$g$$ is not continuous is at most countable.
  

My attempt: 
Let $$g(x^-)~,g(x^+)$$ denote the left and right hand limits of $$g$$ respectively.
 Let $$A$$ be the set of points where $$g$$ is not continuous.
 Then for any $$x\in A$$, there is a rational, say, $$f(x)$$ such that $$g(x^-)\lt f(x)\lt g(x^+)$$.
 For $$x_1\lt x_2$$, we have that $$g(x_1^+)\leq g(x_2^-)$$.
 Thus $$f(x_1)\neq f(x_2)$$ if $$x_1\neq x_2$$.
 This shows an injection between $$A$$ and a subset of the rationals.
 Since the rationals are countable, $$A$$ is countable, being a subset of a countable set.
  
Is my work okay? Are there better/cleaner ways of approaching it?  
.


# Answer 


This looks beautiful to me: or, more truthfully, it looks like exactly what we would write.
If anything else can be asked of this argument, maybe it is a justification that monotone functions have discontinuities as you have described.  we happen to have recently written this up in lecture notes for a "Spivak calculus" course: see $$\S 3$$ here.  Although the fact is quite well known, many texts do not treat it explicitly.  we think this may be a mistake: in the the same section of my notes, we explain how this can be used to give a quick proof of the Continuous Inverse Function Theorem.

