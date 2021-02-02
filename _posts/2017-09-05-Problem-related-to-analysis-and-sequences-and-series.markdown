---
layout: post
title: Problem related to analysis and sequences and series
tag:
 - analysis
 - sequences-and-series

description: Problem related to analysis and sequences and series

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Convergence of series involving iterated $$ \sin $$

<!–-break-–>



Possible Duplicate:
Convergence of $$\sqrt{n}x_{n}$$ where $$x_{n+1} = \sin(x_{n})$$ 

Hi all,
we have  been trying to show the convergence or divergence of


$$

 \sum_{n=1}^\infty \frac{\sin^n 1}{n} = \frac{\sin 1}{1} + \frac{\sin \sin 1}{2} + \frac{\sin \sin \sin 1}{3} + \ \cdots 

$$


where the superscript means iteration (not multiplication, so it's not simply less than a geometric series -- we couldn't find the standard notation for this).
In case it's useful, here are some things we have  tried:

Show $$ \sin^n 1 = O(n^{-\epsilon}) $$ and use the p-series.  we are  not sure that's even true.
Computer tests and looking at partial sums.  Unfortunately, $$ \sum 1/n $$ diverges very slowly, which is hard to distinguish from convergence.
Somehow work in the related series


$$

 \sum_{n=1}^\infty \frac{\cos^n 1}{n} = \frac{\cos 1}{1} + \frac{\cos \cos 1}{2} + \frac{\cos \cos \cos 1}{3} + \ \cdots 

$$


which we know diverges since the numerators approach a fixed point.

.

# Answer 


A Google search has turned up an analysis of the asymptotic behavior of the iterates of $$\sin$$ on page 157 of de Bruijn's Asymptotic methods in analysis.  Namely, 


$$

\sin^n(1)=\frac{\sqrt{3}}{\sqrt{n}}\left(1+O\left(\frac{\log(n)}{n}\right)\right),

$$


which implies that your series converges.


**Edit**: Aryabhata has pointed out in a comment that the problem of showing that $$\sqrt{n}\sin^n(1)$$ converges to $$\sqrt{3}$$ already appeared in the question Convergence of $$\sqrt{n}x_{n}$$ where $$x_{n+1} = \sin(x_{n})$$ (asked by Aryabhata in August). we had missed or forgot about it.  David Speyer gave a great self contained answer, and he also referenced de Bruijn's book.  De Bruijn gives a reference to a 1945 work of Pólya and Szegő for this result.

