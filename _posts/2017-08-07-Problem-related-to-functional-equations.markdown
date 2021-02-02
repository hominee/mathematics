---
layout: post
title: Problem related to functional equations
tag:
 - functional-equations

description: Problem related to functional equations

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A function such that $$f(f(n)) = -n$$?

<!–-break-–>


This question from somebody's job interview made me puzzled:
Design a function f, such that:

$$
f(f(n)) = -n
$$

where n is a 32 bit signed integer; 

you can't use complex numbers arithmetic. if you can't design such a function for the whole range of numbers, design it for the largest range possible.

EDIT: we  removed "Real number" from the title, since it just confused readers, but it was meant just to stress that complex numbers are not allowed.

# Answer 


we 'd try to exploit even and odd numbers. You somehow need a two-stage mapping and thus two subsets of integers. For instance, $$f$$ could map odd numbers to even numbers, and even numbers to odd numbers with opposite sign. Like this:

 $$ 
\color{gray}{f(n)=\begin{cases}0 & n= 0\\
2n & n\in\text{odd}\\
-n/2 & n\in\text{even}
\end{cases}}
 $$ 

EDwe T: A major brain leak from my part, $$n/2$$ can stay even, so this doesn't work. However, the idea is sound, and the next one is actually valid.
You can construct a function that doesn't have this problem. we nstead of messing up the entire range, you can select the smallest possible subset that has the property $$f^2(n)=-n$$. The smallest subset is $$4$$ numbers, because $$f^4(n)=n$$. You can for instance do something like this

 $$ 
f: n_{odd}\mapsto (n+1)_{even} \mapsto (-n)_{odd} \mapsto {-(n+1)}_{even}\mapsto n_{odd}
 $$ 

So if you start with even, start at the second stage. Test:
0 -> 0
1 -> 2 -> -1 -> -2
2 -> -1 -> -2 -> 1
3 -> 4 -> -3 -> -4
4 -> -3 -> -4 -> 3

and so on.
Or as a function

 $$ 
f(n)=\begin{cases}0 & n= 0\\
n+1 & n\in\text{odd}^+\\
-n+1 & n\in\text{even}^+\\
n-1 & n\in\text{odd}^-\\
-n-1 & n\in\text{even}^-
\end{cases}
 $$ 

This procedure does overflow, but only for the very last number in the range. However, at the end of the range you have bigger problem ($$-2^{31}$$ exists but $$2^{31}-1$$ is the top of the range so there's a number without its negative). There are $$3$$ problematic numbers: $$-2^{31}$$ without its negative, and $$\pm(2^{31}-1)$$ that can't be a part of a cycle of $$4$$ numbers, because $$0$$ is already taken.
There's actually no way of fixing this last issue, because the problem comes from the size of the set not being a multiple of $$4$$ after you exclude the zero for its special property $$0=-0$$. The solution we  give is therefore optimal.

