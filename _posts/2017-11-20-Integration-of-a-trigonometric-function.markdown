---
layout: post
title: Integration of a trigonometric function
tag:
 - calculus
 - integration

description: Integration of a trigonometric function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Integration of a trigonometric function

<!–-break-–>


How to integrate: 

$$

\int\limits_{\sqrt{\ln{2}}}^{\sqrt{\ln{3}}} \frac{ x \cdot \sin(x^{2})}{\sin(x^{2}) + \sin(\ln{6}-x^{2})} \ \mathrm dx

$$


Any idea of how to solve.
 Tried using substitution, $$x^2=t$$ but didn't succeed.
 :(
.


# Answer 


Here are some hints:

Substituting $$x^{2}=t$$ as you did is correct. After doing this your integral becomes 

$$

we =\frac{1}{2} \cdot \int\limits_{\ln{2}}^{\ln{3}} \frac{ \sin{t}}{\sin{t} + \sin(\:\ln{6}-t)} \ dt \qquad \cdots  (1)

$$


Next, use this formula: 

$$

\int\limits_{a}^{b} f(x) \ dx = \int\limits_{a}^{b} f(a+b-x) \ dx

$$



Also you have 

$$

 we = \frac{1}{2}\int\limits_{\ln{2}}^{\ln{3}} \frac{\sin(\ln{6}-t)}{\sin{t} + \sin(\ln{6}-t)} \ dt \qquad \cdots (2) 

$$


Add $$(1) + (2)$$. 
Now $$\text{you may ask why we are  doing this}$$: Because $$\ln{2} + \ln{3} = \ln{6}$$ which is in the denominator, and gets $$\textbf{cancelled out. }$$

