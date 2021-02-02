---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - real-analysis
 - integration
 - definite-integrals
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Surely You're Joking, Mr. Feynman! $$\int_0^\infty\frac{\sin^2x}{x^2(1+x^2)}\,dx$$ [duplicate]

<!–-break-–>


And of course, for the sadist with a background in differential
  equations, we invite you to try your luck with the last integral of the
  group.
\begin{equation}\int_0^\infty\frac{\sin^2x}{x^2(1+x^2)}\,dx\end{equation}

Source: Integration: The Feynman Way
.

# Answer 


This integral is readily evaluated using Parseval's theorem for Fourier transforms.  
(we are  certain that Feynman had this theorem in his tool belt.)  
Recall that, for transform pairs $$f(x)$$ and $$F(k)$$, and $$g(x)$$ and $$G(k)$$, the theorem states that


$$

\int_{-\infty}^{\infty} dx \, f(x) g^*(x) = \frac1{2 \pi} \int_{-\infty}^{\infty} dk \, F(k) G^*(k) 

$$


In this case, $$f(x) = \frac{\sin^2{x}}{x^2}$$ and $$g(x) = 1/(1+x^2)$$. Then 
$$F(k) = \pi (1-|k|/2) \theta(2-|k|)$$ 
and
 $$G(k) = \pi \, e^{-|k|}$$. 
 
($$\theta$$ is the Heaviside function, $$1$$ when its argument is positive, $$0$$ when negative.)  
Using the symmetry of the integrand, we may conclude that






$$
\begin{align*}\int_0^{\infty} dx \frac{\sin^2{x}}{x^2 (1+x^2)} &= \frac{\pi}{2} \int_0^{2} dk \, \left ( 1-\frac{k}{2} \right ) e^{-k} \\ &= \frac{\pi}{2} \left (1-\frac1{e^2} \right ) - \frac{\pi}{4} \int_0^{2} dk \, k \, e^{-k} \\ &= \frac{\pi}{2} \left (1-\frac1{e^2} \right ) + \frac{\pi}{2 e^2}  - \frac{\pi}{4} \left (1-\frac1{e^2} \right )\\ &= \frac{\pi}{4} \left (1+\frac1{e^2} \right )\end{align*}


$$ 




