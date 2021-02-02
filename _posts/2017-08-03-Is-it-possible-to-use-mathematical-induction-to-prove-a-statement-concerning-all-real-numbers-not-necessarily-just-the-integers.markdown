---
layout: post
title: Is it possible to use mathematical induction to prove a statement concerning all real numbers, not necessarily just the integers
tag:
 - induction

description: Is it possible to use mathematical induction to prove a statement concerning all real numbers, not necessarily just the integers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

is it possible to use mathematical induction to prove a statement concerning all real numbers, not necessarily just the integers?

<!–-break-–>



we are  referring to the part of proof by mathematical induction where you show that 
"if it is true for one value $$k$$ then it is true for the value $$k+1$$". Does proof by induction 
work over all real numbers? we  mean by considering any arbitrary change, say "$$\delta-x$$", and
 seeing whether (it is true for the value $$x$$) implies (it is true for the value $$x+"\delta-x"$$);  
 or is this flawed in some way. 
.

# Answer 


Yes. There are forms of induction suited to proving things for all real numbers. For example, if you can prove:

There exists $$a$$ such that $$P(a)$$ is true
Whenever $$P(b)$$ is true, then there exists $$c > b$$ such that $$P(x)$$ is true for all $$x \in (b,c)$$
Whenever $$P(x)$$ is true for all $$x \in (d,e)$$, then $$P(e)$$ is true

then it follows that $$P(x)$$ is true for all $$x \geq a $$.

