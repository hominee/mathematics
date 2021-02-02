---
layout: post
title: Operator whose spectrum is given compact set
tag:
 - functional-analysis

description: Operator whose spectrum is given compact set

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Operator whose spectrum is given compact set

<!–-break-–>


Let $$A\subset \mathbb{C}$$ be a compact subset.
 
Since $$A$$ is compact and metric space, it is separable, say $$\overline{\lbrace a_n\rbrace_{n=1}^\infty}=A$$.
 
Let $$\mathcal{l}^2(\mathbb{Z})$$ be the Hilbert space consisting of $$L^2$$-summable sequences and $$\lbrace e_n\rbrace_{n=1}^\infty$$ be the canonical basis of $$\mathcal{l}^2(\mathbb{Z})$$.

Define an operator $$T\colon\mathcal{l}^2(\mathbb{Z})\to\mathcal{l}^2(\mathbb{Z})$$ by sending $$e_n$$ to $$a_ne_n$$.
 we want to prove that $$A=\sigma(T)$$, where $$\sigma(T)$$ is the spectrum of $$T$$.
 
What we can prove is that $$A=\overline{\lbrace a_n\rbrace_{n=1}^\infty}\subset \sigma(T)$$ because each $$a_n$$ is an eigenvalue of $$T$$ and $$\sigma(T)$$ is closed.
 How can we prove the other inclusion, namely $$\sigma(T)\subset A$$?
.


# Answer 


Hint: If $$\lambda$$ in not is $$A$$, then there is $$\epsilon>0$$ with $$\lvert\lambda-a_n\rvert>\epsilon$$ for all $$n$$. Use this to write down a bounded inverse for $$T-\lambda\cdot\mathrm{Id}$$.

