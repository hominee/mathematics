---
layout: post
title: A limit and a coordinate trigonometric transformation of the interior points of a square into the interior points of a triangle
tag:
 - calculus
 - trigonometry
 - limits
 - transformation
 - multivariable-calculus

description: A limit and a coordinate trigonometric transformation of the interior points of a square into the interior points of a triangle

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A limit and a coordinate trigonometric transformation of the interior points of a square into the interior points of a triangle

<!–-break-–>


The coordinate transformation (due to Beukers, Calabi and Kolk)


$$

x=\frac{\sin u}{\cos v}

$$




$$

y=\frac{\sin v}{\cos u}

$$


transforms the square domain $$0\lt x\lt 1$$ and $$0\lt y\lt 1$$ into the triangle domain $$u,v>0,u+v<\pi /2$$ (in Proofs from the BOOK by M.
 Aigner and G.
 Ziegler).

Since the invert transformation is


$$

u=\arccos \sqrt{\dfrac{1-x^{2}}{1-x^{2}y^{2}}}

$$




$$

v=\arccos \sqrt{\dfrac{1-y^{2}}{1-x^{2}y^{2}}}

$$


it is easy to see that three of the vertices (although not belonging to the domain) are transformed as follows:


$$

(x,y)=(0,0)\mapsto (0,0)=(u,v),

$$




$$

(x,y)=(1,0)\mapsto (\pi /2,0)=(u,v),

$$

 


$$

(x,y)=(0,1)\mapsto (0,\pi /2)=(u,v).


$$


Question 1 - But how is the fourth vertex $$(x,y)=(1,1)$$ transformed? In the plot below of $$\dfrac{1-x^{2}}{1-x^{2}y^{2}}$$ seems that the following limit does not exist


$$

\underset{(x,y)\rightarrow (1,1)}{\lim }\sqrt{\dfrac{1-x^{2}}{1-x^{2}y^{2}}}.


$$



Question 2 - As a second question we would like to know how can one "discover" a
transformation of a square into a triangle such as this.
 Is there any systematic study of this kind of transformations?
.


# Answer 


Question 1: Setting $$u=\pi/2-v$$ in your first set of formulas gives $$(x,y)=(1,1)$$, so that point corresponds to the whole hypotenuse $$u+v=\pi/2$$.
Question 2: we have no idea. (Luck? Inspiration? Trial and error?)

