---
layout: post
title: Problem related to complex analysis and integration
tag:
 - complex-analysis
 - integration

description: Problem related to complex analysis and integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Some way to integrate $$\sin(x^2)$$? 

<!–-break-–>


Knowing that $$\int_{-\infty}^{\infty}\exp{(-x^2)} \, dx = \sqrt \pi$$ one can feel that this value has to be somehow "divided" over the entire complex plane, so that every quadrant gets some part of $$\sqrt \pi$$.
 This would give the desired result of $$\sqrt \frac{\pi}{2} - i \sqrt \frac{\pi}{2} $$
Is there a way this could be proved or justified? 
.


# Answer 


Check out this answer for a real method to evaluate this integral.
First note that


$$


\int_0^\infty e^{-x^2}\,\mathrm{d}x=\frac{\sqrt\pi}2\tag{1}


$$


The integral


$$


\int_\gamma e^{-z^2}\,\mathrm{d}z=0\tag{2}


$$


over the curve $$\gamma$$ consisting of the line from $$0$$ to $$R$$ then counterclockwise along the circular arc from $$R$$ to $$Re^{i\pi/4}$$ then back along the line from $$Re^{i\pi/4}$$ to $$0$$ must be $$0$$ since $$e^{-z^2}$$ has no singularities inside $$\gamma$$.
Next note that $$\int_\gamma e^{-z^2}\,\mathrm{d}z$$ along the line from $$0$$ to $$R$$ as $$R\to\infty$$ tends to $$(1)$$.
Next note that $$\int_\gamma e^{-z^2}\,\mathrm{d}z$$ along the arc of the circle of radius $$R$$ from $$R$$ to $$Re^{i\pi/4}$$ as $$R\to\infty$$ goes to zero.
Finally, note that $$\int_\gamma e^{-z^2}\,\mathrm{d}z$$ along the line from $$Re^{i\pi/4}$$ to $$0$$ is


$$


-e^{i\pi/4}\int_0^\infty e^{-ix^2}\,\mathrm{d}x\tag{3}


$$


Therefore, $$(1)$$ plus $$(3)$$ is $$0$$, so we get


$$


\int_0^\infty e^{-ix^2}\,\mathrm{d}x=\frac{1-i}{\sqrt2}\frac{\sqrt\pi}2\tag{4}


$$


Taking the imaginary part of $$(4)$$ yields that


$$


\int_0^\infty\sin(x^2)\,\mathrm{d}x=\sqrt{\frac\pi8}\tag{5}


$$


or


$$


\int_{-\infty}^\infty\sin(x^2)\,\mathrm{d}x=\sqrt{\frac\pi2}\tag{6}


$$



