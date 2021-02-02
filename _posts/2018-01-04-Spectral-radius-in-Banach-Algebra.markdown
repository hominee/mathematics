---
layout: post
title: Spectral radius in Banach Algebra
tag:
 - functional-analysis
 - banach-algebras

description: Spectral radius in Banach Algebra

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Spectral radius in Banach Algebra

<!–-break-–>


Let $$A$$ be a unital Banach algebra and $$a\in A$$ and $$\lambda \in \rho(a)$$.
 we want to prove that 

$$

r(R(a,\lambda))=\frac{1}{d(\lambda,\sigma(a))}.


$$

 where $$R(a,\lambda)=(\lambda 1-a)^{-1}$$ and $$r(.
)$$ is the spectral radius.
we are  giving this hint: prove the result if $$A$$ is commutative then do it for the general case.
 we are  trying to do this but the only thing that we can prove is $$\|R(a,\lambda)\|\ge\frac{1}{d(\lambda,\sigma(a))}$$, but since $$r(.
)\le \|.
\|$$ things don't add up.
 and when dealing with the general case a'm not sure how to go from the commutative case to the general case we have a feeling that this has to do with $$r(.
)$$ being upper semi continuous.


# Answer 


There is no need to assume $$A$$ commutative.
Consider the holomorphic function 


$$


f(z)=\frac{1}{\lambda -z}


$$


on $$\mathbb{C}\setminus\{\lambda\}$$, which is an open neighborhood of the spectrum $$\sigma(a)$$ of $$a$$.
The holomorphic functional calculus makes sense of


$$


f(a)=(\lambda 1-a)^{-1}.


$$


and yields, by spectral mapping:


$$


\sigma(f(a))=f(\sigma(a)).


$$


Therefore


$$


r(f(a))=\max_{\beta\in \sigma(f(a))}\|\beta\|=\max_{\alpha \in \sigma(a)}\|f(\alpha)\|=\max_{\alpha\in\sigma(a)}\frac{1}{\|\lambda-\alpha\| }=\frac{1}{\min_{\alpha\in \sigma(a)}\|\lambda-\alpha\|}=\frac{1}{d(\lambda,\sigma(a))}


$$


where $$d(\lambda,\sigma(a))=\inf_{\alpha\in \sigma(a)} \|\lambda -\alpha\|=\min_{\alpha\in \sigma(a)} \|\lambda -\alpha\|$$ by compactness of the spectrum.

