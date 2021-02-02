---
layout: post
title: Problem related to linear algebra and matrices
tag:
 - linear-algebra
 - matrices

description: Problem related to linear algebra and matrices

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

$$AB-BA$$ is a nilpotent matrix if it commutes with $$A$$

<!–-break-–>


we saw this in a MathOverflow post and am putting it here for posterity.

Problem:
Let $$A$$ and $$B$$ by square matrices and set $$C=AB-BA$$.
 If $$AC=CA$$, prove $$C$$ is nilpotent.


# Answer 


Hint: we use this theorem: If $$\forall i\ge1$$ trac $${C^i}=0$$, then $$C$$ is nilpotent.
You can easily prove by  induction that trac ($${C^i})=0$$ for all $$i\ge1$$. 


**Edit**1: Theorem :$$\forall i\ge1$$ trac $${C^i}=0$$ iff C is nilpotent.
Proof: $$C$$ is a real matrix but you assume $$A$$ is a complex matrix and $$f(x)=(x-a_1)(x-a_2)...(x-a_n)$$ is its characteristic polynomial in the complex field.  You can prove that trac($$C^k$$)=$$\sum_{i=1}^n {a_i^k}$$ by induction, and if  $$\forall k\in\mathbb N$$ trac($$C^k$$)=$$\sum_{i=1}^n {a_i^k}=0$$  then   $$a_i=0$$. Hence, $$f(x)=x^n$$, so $$A^n=0$$ and it is shown that C is nilpotent.

