---
layout: post
title: Problem related to calculus and trigonometry
tag:
 - calculus
 - integration
 - trigonometry

description: Problem related to calculus and trigonometry

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to prove that $$\int\limits_{-\pi/2}^{\pi/2}\frac{\cos(2x)}{e^x+1}=0$$?

<!–-break-–>


we are  stuck trying to show that $$\displaystyle \int\limits_{-\pi/2}^{\pi/2}\frac{\cos(2x)}{e^x+1}=0$$ 
we have tried using a Squeeze Theorem type approach, but at $$\pi/4$$ any function we choose overlaps and becomes less than or greater than the function depending.
 we are  not sure where to start anymore.


# Answer 


There is a result 
stated as follows

Suppose $$f$$ is continuous and even on $$[-a,a]$$, $$a>0$$ then 
  

$$

\int\limits_{-a}^a \frac{f(x)}{1+e^{x}} \mathrm dx = \int\limits_0^a f(x) \mathrm dx

$$



Using this result, $$\displaystyle \int_{-\pi/2}^{\pi/2}\frac{\cos(2x)}{e^x+1}dx=\int_{0}^{\pi/2}\cos(2x)\,dx=0$$. 

