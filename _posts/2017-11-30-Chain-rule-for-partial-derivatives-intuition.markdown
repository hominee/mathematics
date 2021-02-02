---
layout: post
title: Chain rule for partial derivatives intuition
tag:
 - multivariable-calculus
 - derivatives

description: Chain rule for partial derivatives intuition

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Chain rule for partial derivatives intuition

<!–-break-–>


Can somebody give me an intuitive explanation for the below equations.
 we are  not sure how they come about and how they can be perceived logically.



$$

\frac{\partial z}{\partial s} =\frac{\partial f}{\partial x}\frac{\partial x}{\partial s}+ \frac{\partial f}{\partial y}\frac{\partial y}{\partial s} \ \ \text{and} \ \ \frac{\partial z}{\partial t} =\frac{\partial f}{\partial x}\frac{\partial x}{\partial t}+ \frac{\partial f}{\partial y}\frac{\partial y}{\partial t} 

$$


.


# Answer 


Suppose for simplicity that $$z = f(x,y)$$ and $$x,y$$ are functions of $$s$$. The partial derivatives of $$z$$ given a first-order approximation for $$z$$:


$$

 f(x+\Delta x,y+\Delta y) \approx f(x,y) + \frac{\partial f}{\partial x}(x,y) \Delta x + \frac{\partial f}{\partial y}(x,y) \Delta y. 

$$


The error in this approximation should be "small", say $$o(\Delta x+\Delta y)$$ (if you don't know what this means, it's not important). Similarly,


$$


x(s+\Delta s) \approx x(s) + \frac{\partial x}{\partial s}(s) \Delta s, \quad
y(s+\Delta s) \approx y(s) + \frac{\partial y}{\partial s}(s) \Delta s.


$$


Finally, $$\frac{\partial f}{\partial s}$$ satisfies


$$


f(x(s+\Delta s),y(s+\Delta s)) \approx f(x(s),y(s)) + \frac{\partial f(x,y)}{\partial s}(s) \Delta s.


$$


We can now prove the formula:


$$


\begin{align*}
f(x(s+\Delta s),y(s+\Delta s)) &\approx
f(x(s) + \frac{\partial x}{\partial s}(s) \Delta s, y(s) + \frac{\partial y}{\partial s}(s) \Delta s) \\ &\approx
f(x(s),y(s)) + \frac{\partial f}{\partial x}(x,y) \frac{\partial x}{\partial s}(s) \Delta s + \frac{\partial f}{\partial y}(x,y) \frac{\partial y}{\partial s}(s) \Delta s.
\end{align*}


$$



