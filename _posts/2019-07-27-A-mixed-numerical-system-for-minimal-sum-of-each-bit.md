---
layout: post
title: A mixed numerical system for minimal sum of each bit
tags:
  - numerical system
  - minimal sum
  - p-adic

hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---

# Problem statement
The monetary system in Absurdistan is really simple and systematic.
The locals only use coins.The coins come in different values.
The values used are:  

$$  1, 10, 25, 100, 1000, 2500, 10000, 100000, 250000, 1000000, ... $$  

Formally, for each $$k \geq 0$$ there are coins worth $$10 k$$, and coins worth $$25 k$$.
You want to buy a new car. Its price varies.
Assuming you have a sufficient supply of coins of each of the types you will need.

# Question
Output the smallest number of coins necessary to pay exactly the cost of the car.

<!–-break-–>

I came across this problem in a websit called [codechef][codechef] which, personly I think, is a very good 
site. As simple it is the first sight, it may of interest to those who love mathematics and programming including
me, thus this page is born. 

Let's start with the very basic ideal that the numerical denotation of natrual number, for a $$p-$$adic number $$(x)_p $$

$$
\label{basic}
\begin{equation}
(x)_p = \Sigma _{i=0} ^n  a_i p^i.
\end{equation}
$$

where $$ 0 \leq a_i \leq p-1 $$, and $$n$$ is finite.  
With formula $$\eqref{basic}$$ we could assign each number a unique numeric denotation accordingly. Furthermore  

$$
\space$$ 
 
$$ \textbf{Theorem 1} \label{theorem1}$$: $$  \Sigma _{i=0} ^n  a_i$$  reach  its  minimal for $$x$$ in p-adic system.

$$\space$$  

I will leave the proof to you. (Hint: we can proof it by contradiction.)  
So after so much time we spend to what degree the problem relates to it?   
What if we let $$p=100$$ and take $$  1, 10, 25 $$ out as a numerical system that 
  
$$
\begin{equation}
(x)_{100} = \Sigma _{i=0} ^{n'}  b_i 100^i.
\end{equation}
$$

where $$ 0 \leq b_i \leq 99, b_i = u_i 25 + v_i 10 + w_i $$.  
Owing to unique denotation of each number the question will be answered if and only if 

$$
\label{con}
\begin{equation}
\Sigma _{i=1} ^{n'} u_i  + v_i  + w_i
\end{equation}
$$ 

reacher its minimal value. Therefore we got to write an programm to check all the number from 1 to 100, what 
compromises almost work we have to do.  


[codechef]:    https://www.codechef.com/problems/FR11
