---
layout: post
title: Problem related to calculus and improper integrals
tag:
 - calculus
 - integration
 - improper-integrals

description: Problem related to calculus and improper integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Prove: $$\int_0^\infty \sin (x^2) \, dx$$ converges.

<!–-break-–>


$$\sin x^2$$ does not converge as $$x \to \infty$$, yet its integral from $$0$$ to $$\infty$$ does.


# Answer 


$$x\mapsto \sin(x^2)$$ is integrable on $$[0,1]$$, so we have to show that $$\lim_{A\to +\infty}\int_1^A\sin(x^2)dx$$ exists. Make the substitution $$t=x^2$$, then $$x=\sqrt t$$ and $$dx=\frac{dt}{2\sqrt t}$$. We have 

$$

\int_1^A\sin(x^2)dx=\int_1^{A^2}\frac{\sin t}{2\sqrt t}dt=-\frac{\cos A^2}{2\sqrt A}+\frac{\cos 1}2+\frac 12\int_1^{A^2}\cos t\cdot  t^{-3/2}\frac{-1}2dt,

$$


and since $$\lim_{A\to +\infty}-\frac{\cos A^2}{2\sqrt A}+\frac{\cos 1}2=\frac{\cos 1}2$$ and the integral $$\int_1^{+\infty}t^{-3/2}dt$$ exists (is finite), we conclude that $$\int_1^{+\infty}\sin(x^2)dx$$ and so does $$\int_0^{+\infty}\sin(x^2)dx$$. 
This integral is computable thanks to the residues theorem.

