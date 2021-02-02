---
layout: post
title: Problem related to real analysis
tag:
 - real-analysis

description: Problem related to real analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to construct a bijection from $$(0, 1)$$ to $$[0, 1]$$? [duplicate]

<!–-break-–>



Possible Duplicate:
Bijection between an open and a closed interval
How do we  define a bijection between $$(0,1)$$ and $$(0,1]$$? 

we  wonder if we  can cut the interval $$(0,1)$$ into three pieces:
$$(0, \frac{1}{3})\cup(\frac{1}{3},\frac{2}{3})\cup(\frac{2}{3},1)$$, in which we are  able to map point $$\frac{1}{3}$$ and $$\frac{2}{3}$$ to $$0$$ and $$1$$ respectively.
Now the question remained is how to build a bijection mapping from those three intervels to $$(0,1)$$.
Or, my method just goes in a wrong direction. Any correct approaches?
.

# Answer 


Consider the sequence 

 $$ 

\frac 12, \frac 13, \frac 14, \frac 15, \dots, \frac 1n, \dots

 $$ 

Map every other point $$f : (0,1) \to [0,1]$$ that is not in this sequence to itself, and then map the above sequence to the corresponding points in this one : 

 $$ 

0, 1, \frac 12, \frac 13, \frac 14, \dots.

 $$ 

we n other words, map $$\frac 12$$ to $$0$$, $$\frac 13$$ to $$1$$, and then map $$\frac 1n$$ to $$\frac 1{n-2}$$ for $$n \ge 4$$.
The reason why you can map some set into some bigger set bijectively is precisely because they are infinite, so you must exploit this fact. we f you don't, you have no chance.
Now to answer your actual question, the trick you try to use doesn't feel relevant to me ; we are  not saying there is absolutely no way it could work, because we  actually know there is, since your set (the union of the three intervals) and the interval $$(0,1)$$ have the same cardinality. The problem with your idea is that we  don't think a construction will naturally come out of it. we n general, to map bijectively a set into a bigger one you must be "moving things around", so we  expect any fairly understandable construction involving your idea to be similar to the one we 've shown you.
Hope that helps,

