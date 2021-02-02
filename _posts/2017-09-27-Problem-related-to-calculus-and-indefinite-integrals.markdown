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

Why isn't $$\int \frac{1}{x}~dx = \frac{x^0}{0}$$?

<!–-break-–>


we know that 
$$\int \frac{1}{x}~dx = \ln|x| + C$$ 
and we know the antiderivative method works for all powers of $$x$$ except $$-1$$. 


**Edit**: we do realize dividing by zero is meaningless. That's not the question. Just because dividing by zero is meaningless doesn't mean mathematicians just choose to ignore it and work just make up a new answer. There has to be an explanation, and that's what we are  asking for. The explanation. 
.

# Answer 


Notice that


$$

\left.\int_1^xt^ndt=\frac{t^{n+1}}{n+1}\right|_1^x=\frac{x^{n+1}-1}{n+1}

$$


but at $$n=-1$$, we get division by $$0$$, and clearly this is bad.  However, following this line of logic, we can take the limit as $$n\to-1$$ to get


$$

\int_1^x\frac1tdt\stackrel?=\lim_{n\to-1}\frac{x^{n+1}-1}{n+1}=\lim_{h\to0}\frac{x^h-1}h

$$


You might recognize this better if we remind you of the following limit:


$$

1=\lim_{h\to0}\frac{e^h-1}h

$$


And combine all this, you'll get


$$

\int_1^x\frac1tdt\stackrel?=\ln(x)

$$



