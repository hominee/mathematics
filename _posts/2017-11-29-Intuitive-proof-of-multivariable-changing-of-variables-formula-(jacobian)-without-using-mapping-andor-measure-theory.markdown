---
layout: post
title: Intuitive proof of multivariable changing of variables formula (jacobian) without using mapping andor measure theory
tag:
 - linear-algebra
 - multivariable-calculus
 - intuition

description: Intuitive proof of multivariable changing of variables formula (jacobian) without using mapping andor measure theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Intuitive proof of multivariable changing of variables formula (jacobian) without using mapping and/or measure theory?

<!–-break-–>


What is an intuitive proof of multivariable changing of variables formula (jacobian) without using mapping and/or measure theory?
we was thinking that textbooks over-complicate the proof.

If possible, using linear algebra and calculus to solve it, that way would be simplest for me?
.


# Answer 


The multivariable change of variables formula is nicely intuitive, and it's not too hard to imagine how somebody might have derived the formula from scratch.  However, it seems that proving the theorem rigorously is not as easy as one might hope.
Here's my attempt at explaining the intuition -- how you would derive or discover the formula.
The first thing to understand is that if $$A$$ is an $$N \times N$$ matrix with real entries and $$S \subset \mathbb R^N$$, then $$m(AS) = \|\det A\| \, m(S)$$.  (Technically we should assume that $$S$$ is measurable.)  This is intuitively clear from the SVD of $$A$$:
\begin{equation}
A = U \Sigma V^T
\end{equation}
where $$U$$ and $$V$$ are orthogonal and $$\Sigma$$ is diagonal with nonnegative diagonal entries.  Multiplying by $$V^T$$ doesn't change the measure of $$S$$.  Multiplying by $$\Sigma$$ scales along each axis, so the measure gets multiplied by $$\det \Sigma = \| \det A\|$$.  Multiplying by $$U$$ doesn't change the measure.
Next suppose $$\Omega$$ and $$\Theta$$ are open subsets of $$\mathbb R^N$$ and suppose $$g:\Omega \to \Theta$$ is $$1-1$$ and onto.  We should probably assume $$g$$ and $$g^{-1}$$ are $$C^1$$ just to be safe.  (Since we're just seeking an intuitive derivation of the change of variables formula, we aren't obligated to worry too much about what assumptions we make on $$g$$.)  Suppose also that $$f:\Theta \to \mathbb R$$ is, say, continuous (or whatever conditions we need for the theorem to actually be true).
Partition $$\Theta$$ into tiny subsets $$\Theta_i$$.  For each $$i$$, let $$u_i$$ be a point in $$\Theta_i$$.  Then
\begin{equation}
\int_{\Theta} f(u) \, du \approx \sum_i f(u_i) m(\Theta_i).
\end{equation}
Now let $$\Omega_i = g^{-1}(\Theta_i)$$ and $$x_i = g^{-1}(u_i)$$ for each $$i$$.  The sets $$\Omega_i$$ are tiny and they partition $$\Omega$$.  Then



$$
\begin{align*}
\sum_i f(u_i) m(\Theta_i) &= \sum_i f(g(x_i)) m(g(\Omega_i)) \\
&\approx \sum_i f(g(x_i)) m(g(x_i) + Jg(x_i) (\Omega_i - x_i)) \\
&=  \sum_i f(g(x_i)) m(Jg(x_i) \Omega_i) \\
&\approx \sum_i f(g(x_i)) \|\det Jg(x_i)\| m(\Omega_i) \\
&\approx \int_{\Omega} f(g(x)) \|\det Jg(x)\| \, dx.
\end{align*}


$$

We have discovered that
\begin{equation}
\int_{g(\Omega)} f(u) \, du \approx \int_{\Omega} f(g(x)) \|\det Jg(x)\| \, dx.
\end{equation}
By using even tinier subsets $$\Theta_i$$, the approximation would be even better -- so we see by a limiting argument that we actually have equality.
At a key step in the above argument, we used the approximation
\begin{equation}
g(x) \approx g(x_i) + Jg(x_i)(x - x_i)
\end{equation}
which is a good approximation when $$x$$ is close to $$x_i$$

