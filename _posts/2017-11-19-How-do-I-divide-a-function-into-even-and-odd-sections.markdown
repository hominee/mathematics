---
layout: post
title: How do I divide a function into even and odd sections
tag:
 - functions
 - even-and-odd-functions

description: How do I divide a function into even and odd sections

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How do we divide a function into even and odd sections?

<!–-break-–>


While working on a proof showing that all functions limited to the domain of real numbers can be expressed as a sum of their odd and even components, we stumbled into a troublesome roadblock; namely, we had no clue how one divides the function into these even and odd parts.

Looking up a solution for the proof, we found these general formulas for the even and odd parts of a function $$f(n)$$:


$$

\begin{align*}
f_e(n)&\overset{\Delta}{=}\frac{f(n)+f(-n)}{2}\\
f_o(n)&\overset{\Delta}{=}\frac{f(n)-f(-n)}{2}
\end{align*}

$$


While we understand that in an even function $$f(n) = f(-n)$$ and that in an odd function $$f(-n) = -f(n)$$, we still don't get how these general formulas for the even and odd parts were obtained.
 Can someone guide me through the logic?
.


# Answer 


Suppose you could write a function $$f(x)$$ as the sum of an even and an odd function; call them $$E(x)$$ and $$O(x)$$. 
In particular, you would have
\[f(x) = E(x)+O(x)\]
and you would also have
\[f(-x) = E(-x) + O(-x) = E(x) - O(x)\]
with the latter equation because we are assuming $$E$$ is even and $$O$$ is odd, so $$E(x)=E(-x)$$ and $$O(-x) = -O(x)$$.
Adding both equations you get $$f(x)+f(-x) = 2E(x)$$. Subtracting the second equation from the first gives you $$f(x)-f(-x)=2O(x)$$. Now solve for $$E(x)$$ and $$O(x)$$, and you get the formulas you see in the solution. Then you check that the answer does indeed work (that is, you check that the formulas you found do give you an even and an odd function in all cases).
In other words: pretend you already know the answer, and try to deduce conditions that the answer must satisfy (these will be necessary conditions); if things go well, you'll get enough information about what they must be like to figure out what they are.

