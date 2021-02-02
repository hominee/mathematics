---
layout: post
title: Problem related to functional analysis and operator theory
tag:
 - functional-analysis
 - operator-theory

description: Problem related to functional analysis and operator theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

$$AB - BA = I$$ in Hilbert Space 

<!–-break-–>

 How can we prove that $$AB - BA = I$$ is not possible ? Probably this is as easy as in the matrices case, but we couldn't prove it.


# Answer 


A more general question has been asked and answered on here before. The bounded operators on a Hilbert space form a Banach Algebra. A beautiful argument of H. Wielandt shows that the equation $$AB-BA = I$$ is not possible in any normed algebra. we won't repeat it here, but it follows by induction that if $$AB -BA = I,$$ we have $$AB^{n}-B^{n}A = nB^{n-1}$$ for all positive integers $$n.$$ This implies that $$2\|A\| \|B \| \geq n$$ for every $$n,$$ a contradiction.

