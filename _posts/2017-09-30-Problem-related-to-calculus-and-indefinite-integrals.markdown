---
layout: post
title: Problem related to calculus and indefinite integrals
tag:
 - calculus
 - integration
 - indefinite-integrals

description: Problem related to calculus and indefinite integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Need a hint to evaluate the indefinite integral $$\int\frac{e^x(2-x^2)}{(1-x)\sqrt{1-x^2}}dx$$?

<!–-break-–>


So, the question says we have to perform the indefinite integration


$$

\int\frac{e^x(2-x^2)}{(1-x)\sqrt{1-x^2}}dx

$$


we know that


$$

\int e^x(f(x)+f'(x))dx=e^xf(x)+C

$$


Since any other substitution (using $$x=ln(t)$$ etc.) doesn't work, we expect we have to break the fraction with $$e^x$$ in the above integral to make separate fractions for $$f(x)$$ and $$f'(x)$$ somehow. we separate $$2-x^2=1+(1-x^2)$$, but that doesn't work (leaves $$x$$ in the numerator of derivative which we don't see in the question). Any other tricks?
.

# Answer 


Your trick does work.


$$

e^x\frac{2-x^2}{(1-x)\sqrt{1-x^2}}=e^x\frac1{(1-x)\sqrt{1-x^2}}+e^x\sqrt{\frac{1+x}{1-x}}

$$


And,


$$

\frac{d\sqrt{\frac{1+x}{1-x}}}{dx}=\frac{\sqrt{1-x}}{2\sqrt{1+x}}\frac{2}{(1-x)^2}=\frac1{(1-x)\sqrt{1-x^2}}

$$


So the antiderivative is, 

$$

e^x\sqrt{\frac{1+x}{1-x}}+C

$$



