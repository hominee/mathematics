---
layout: post
title: Problem related to multivariable calculus and notation
tag:
 - multivariable-calculus
 - notation

description: Problem related to multivariable calculus and notation

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What exactly does $$\frac{\partial(y_1,\dots,y_m)}{\partial(x_1,\dots,x_n)}$$ refer to?

<!–-break-–>


we have been asking a rather few questions of this nature lately, maybe we are  starting to realise math notation isn't as uniform as we initially thought it would be.
.
.

Question: Does this notation


$$

\frac{\partial(y_1,\dots,y_m)}{\partial(x_1,\dots,x_n)}

$$


refer to the Jacobian matrix


$$

 J = \begin{bmatrix} \dfrac{\partial y_1}{\partial x_1} & \cdots & \dfrac{\partial y_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \dfrac{\partial y_m}{\partial x_1} & \cdots & \dfrac{\partial y_m}{\partial x_n}  \end{bmatrix},

$$


or the Jacobian determinant $$\det J$$?
This answer seems to support the latter interpretation, while this (and Wikipedia) both support the former.

we are  aware of the ambiguity of "Jacobian" being used to refer to either the determinant or the matrix itself, is this a similar case? It's really a bit annoying because when we see things like


$$

 \left\| \frac{\partial(y_1,\dots,y_m)}{\partial(x_1,\dots,x_n)} \right\| 

$$


we don't know if it means the absolute value of the Jacobian determinant, or the determinant of the Jacobian matrix.


# Answer 


Every time that we use it and have seen it, we have used it to refer to the matrix itself. we will typically use det J to refer to the determinant, but we admit that we have used the term Jacobian to refer to both the matrix and the determinant.
This is another case where math is precise, but the language of math is often not. we would recommend that you take care to be specific in your usage - use Jacobian matrix and Jacobian determinant so that there is no confusion.

