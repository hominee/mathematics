---
layout: post
title: Problem related to real analysis and lp spaces
tag:
 - real-analysis
 - sequences-and-series
 - functional-analysis
 - norm
 - lp-spaces

description: Problem related to real analysis and lp spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

The $$ l^{\infty} $$-norm is equal to the limit of the $$ l^{p} $$-norms.

<!–-break-–>


The $$ l^{\infty} $$-norm of $$ \mathbf{x} $$ is $$ \displaystyle \sup_{i \in \mathbb{N}} |x_{i}| $$.
Prove that the limit of the $$ l^{p} $$-norms is the $$ l^{\infty} $$-norm.
we saw an answer for $$ L^{p} $$-spaces, but we need one for $$ l^{p} $$-spaces. Besides, we didn’t really understand the $$ L^{p} $$-answer either.

# Answer 


Let me state the result properly:

Let $$x=(x_n)_{n \in \mathbb{N}} \in \ell^q$$ for some $$q \geq 1$$. Then 

$$

\|x\|_{\infty} = \lim_{p \to \infty} \|x\|_p. \tag{1}

$$





**Note** that $$(1)$$ fails, in general, not hold if $$x=(x_n)_{n \in \mathbb{N}} \notin \ell^q$$ for all $$q \geq 1$$ (consider for instance $$x_n := 1$$ for all $$n \in \mathbb{N}$$.)
Proof of the result: Since 

$$

|x_k| \leq \left(\sum_{j=1}^{\infty} |x_j|^p \right)^{\frac{1}{p}}=\|x\|_p

$$

 for all $$k \in \mathbb{N}$$, $$p \geq 1$$, we have $$\|x\|_{\infty} \leq \|x\|_p$$. Thus, in particular 

$$

\|x\|_{\infty} \leq \liminf_{p \to \infty} \|x\|_p. \tag{1}

$$


On the other hand, we know that 

$$

\|x\|_p = \left( \sum_{j=1}^{\infty} |x_j|^{p-q} \cdot |x_j|^q \right)^{\frac{1}{p}} \leq \|x\|_{\infty}^{\frac{p-q}{p}} \cdot \left( \sum_{j=1}^{\infty} |x_j|^q \right)^{\frac{1}{p}} = \|x\|_{\infty}^{1-\frac{q}{p}} \cdot \|x\|_q^{\frac{q}{p}}

$$

 for all $$q<p$$ where we used 
$$|x_j| \leq \|x\|_{\infty}$$ for all $$j \in \mathbb{N}$$. Therefore, we arrive at


$$

 \limsup_{p \to \infty} \|x\|_p \leq \limsup_{p \to \infty} \left( \|x\|_{\infty}^{1-\frac{q}{p}} \cdot \|x\|_q^{\frac{q}{p}}\right) = \|x\|_{\infty} \cdot 1. \tag{2}

$$


Hence, 

$$

\limsup_{p \to \infty} \|x\|_p \leq \|x\|_{\infty} \leq \liminf_{p \to \infty} \|x\|_p.

$$

 This shows that $$\lim_{p \to \infty} \|x\|_p$$ exists and equals $$\|x\|_{\infty}$$.

