---
layout: post
title: Are some indefinite integrals impossible to compute or just don't exist
tag:
 - calculus
 - integration

description: Are some indefinite integrals impossible to compute or just don't exist

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Are some indefinite integrals impossible to compute or just don't exist?

<!–-break-–>


How can you prove that a function has no closed form integral?

we 've just started working with integrals relatively recently and we are  so surprised how much harder they are to compute than derivatives. For example, for something as seemingly simple as $$\int e^{ \cos x} dx $$ is impossible right? we  can't use u-sub since there is no $$-\sin(x)$$ multiplying the function, also integration by parts seems like it wouldn't work, correct? So does this mean this integral is impossible to compute?


# Answer 


The indefinite integral of a continuous function always exists.  we t might not exist in "closed form", i.e. it might not be possible to write it as a finite expression using "well-known" functions.  The concept of "closed form" is 
somewhat vague, since there's no definite list of which functions are "well-known".  A more precise statement is that there are elementary functions whose indefinite integrals are not elementary.  For example, the indefinite integral $$\int e^{x^2}\; dx$$ is not an elementary function, although it can be expressed in terms of a non-elementary special function as $$\frac{\sqrt{\pi}}{2} \text{erfi}(x)$$.
Your example $$\int e^{\cos(x)}\; dx$$ is also non-elementary.  This can be proven using the Risch algorithm.  This one does not seem to have any non-elementary closed form either.

