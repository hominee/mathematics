---
layout: post
title: Problem related to real analysis
tag:
 - real-analysis

description: Problem related to real analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Show that $$f$$ has at most one fixed point

<!–-break-–>


Let $$f\colon\mathbb{R}\to\mathbb{R}$$ be a differentiable function.
 $$x\in\mathbb{R}$$ is a fixed point of $$f$$ if $$f(x)=x$$.
 Show that if $$f'(t)\neq 1\;\forall\;t\in\mathbb{R}$$, then $$f$$ has at most one fixed point.

My biggest problem  with this is that it doesn't seem to be true.
 For example, consider $$f(x)=x^2$$.
 Then certainly $$f(0)=0$$ and $$f(1)=1 \Rightarrow 0$$ and $$1$$ are fixed points.
 But $$f'(x)=2x\neq 1 \;\forall\;x\in\mathbb{R}$$.
 Is there some sort of formulation that makes this statement correct? Am we missing something obvious? This is a problem from an old exam, so we are  assuming that maybe there's some sort of typo or missing condition.


# Answer 


This problem is straight out of baby Rudin.
Assume by contradiction that $$f$$ has more than one fixed point. Select any two distinct fixed points, say, $$x$$ and $$y$$.
Then, $$f(x) = x$$ and $$f(y) = y$$. By the Mean Value Theorem, there exists some $$\alpha \in (x,y)$$ such that $$f'(\alpha) = \frac{f(x)-f(y)}{x-y} = \frac{x-y}{x-y} = 1$$, contradicting the hypothesis.

