---
layout: post
title: Problem related to real analysis and lp spaces
tag:
 - real-analysis
 - functional-analysis
 - measure-theory
 - convergence
 - lp-spaces

description: Problem related to real analysis and lp spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

If $$f_k \to f$$ a.e. and the $$L^p$$ norms converge, then $$f_k \to f$$ in $$L^p$$

<!–-break-–>


Let $$1\leq p < \infty$$.
 Suppose that 

$$\{f_k\} \subset L^p$$ (the domain here does not necessarily have to be finite), 
$$f_k \to f$$ almost everywhere, and 
$$\|f_k\|_{L^p} \to \|f\|_{L^p}$$.
 

Why is it the case that 

$$

\|f_k - f\|_{L^p} \to 0?

$$

 
A statement in the other direction (i.
e.
 $$\|f_k - f\|_{L^p} \to 0 \Rightarrow \|f_k\|_{L^p} \to \|f\|_{L^p}$$ ) follows pretty easily and is the one that we have  seen most of the time.
 we are  not how to show the result above though.
 
.


# Answer 


This is a theorem by Riesz.
Observe that


$$

\|f_k - f\|^p \leq 2^p (\|f_k\|^p + \|f\|^p),

$$


Now we can apply Fatou's lemma to


$$

2^p (\|f_k\|^p + \|f\|^p) - \|f_k - f\|^p \geq 0.

$$


If you look well enough you will notice that this implies that


$$

\limsup_{k \to \infty} \int \|f_k - f\|^p \, d\mu = 0.

$$


Hence you can conclude the same for the normal limit.

