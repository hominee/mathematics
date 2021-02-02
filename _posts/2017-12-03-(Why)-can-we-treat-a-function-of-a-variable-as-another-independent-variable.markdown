---
layout: post
title: (Why) can we treat a function of a variable as another independent variable
tag:
 - multivariable-calculus
 - derivatives
 - numerical-methods
 - jacobian
 - numerical-calculus

description: (Why) can we treat a function of a variable as another independent variable

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

(Why) can we treat a function of a variable as another independent variable?

<!–-break-–>


we are  currently reading my numerical analysis textbook and something's bugging me.
 To get into it, let's take a look at the following differential equation;


$$

u'(x) = f(x, u(x))

$$


In order to determine the stability of the equation, one may calculate the Jacobian,


$$

J(x, u(x)) = \frac{\partial f}{\partial u}\|_{(x, u(x))}

$$


Here is a specific differential equation:


$$

u'(x) = -\alpha(u(x) - sin(x)) + cos(x)

$$


For which the Jacobian is


$$

J(x, u(x)) = -\alpha

$$


Basically, we treated both $$sin(x)$$ and $$cos(x)$$ as constants with respect to $$u$$, but we don't really understand why.
 Most of the time, when we take a derivative the variables are independant, which is not the case here as they both depend on the same variable $$x$$.


# Answer 


There is a difference between the partial derivative $$\frac{\partial}{\partial x}$$ and the total derivative $$\frac{d}{dx}$$. For example, if we have variables $$(u,x)$$ and the equation $$f=f(x,u(x))=x^2+u^3$$ and we take the partial derivative we get $$\frac{\partial f}{\partial x}=2x$$ but if we take the total derivative we get $$\frac{d f}{dx}=2x+3u^2\frac{\partial u}{\partial x}$$, applying the chain rule. This distintion is a key point in classical mechanics for example and captures essentially what you are asking.
See: What exactly is the difference between a derivative and a total derivative?

