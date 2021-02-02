---
layout: post
title:  Basel problem 1
tags:
  - sum
  - closed-form
  - real-analysis
  - Basel-problem
  - Golden-ratio
  - zeta-function
  
description:  
  Basel problem 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Show that :

$$

5\sum_{k=1}^{\infty}{\phi^k-1\over \phi^{2k}}\cdot{1\over k^2}=\zeta(2)

$$



<!–-break-–>
 
Golden ratio:$$\phi$$

$$
5\sum_{k=1}^{\infty}{\phi^k-1\over \phi^{2k}}\cdot{1\over k^2}=\zeta(2)\tag1
$$


We'll known Basel's problem


$$
\sum_{k=1}^{\infty}{1\over k^2}=\zeta(2)\tag2
$$


How do I transform $$(1)$$ to $$(2)?$$

Extra information:


$$
\sum_{k=1}^{\infty}{\phi^k-1\over \phi^{2k}}=1\tag3
$$



# Answer

 to show that

$$
5\sum_{k=1}^{\infty}{\phi^k-1\over \phi^{2k}}\cdot{1\over k^2}
=\zeta(2)
$$

The function you need
is the dilogarithm,
defined by

$$
L_2(z)
=\sum_{k=1}^{\infty}\dfrac{z^k}{k^2}
$$

There is much useful info here:

https://en.wikipedia.org/wiki/Spence's_function

So you want to show that

$$
5(L_2(\phi^{-1})-L_2(\phi^{-2}))
=\zeta(2)
$$

Since

$$
\phi=\dfrac{1+\sqrt{5}}{2}
$$

$$
\phi-1=\dfrac{\sqrt{5}-1}{2}
$$

$$
1-\phi
=\dfrac{1-\sqrt{5}}{2}
=\dfrac{-1}{\phi}
$$

and

$$
\dfrac{1}{\phi^2}
=\dfrac{(1-\sqrt{5})^2}{4}
=\dfrac{1-2\sqrt{5}+5}{4}
=\dfrac{3-\sqrt{5}}{2}
$$

this is equivalent to

$$
5(L_2(\dfrac{\sqrt{5}-1}{2})-L_2(\dfrac{3-\sqrt{5}}{2}))
=\zeta(2)
$$

According to the Wikipedia page above,

$$
L_2(\dfrac{\sqrt{5}-1}{2}) =\dfrac{\pi^2}{10}-\ln^2(\dfrac{\sqrt{5}-1}{2})
$$

and

$$
L_2(\dfrac{3-\sqrt{5}}{2}))=\dfrac{\pi^2}{15}-\ln^2(\dfrac{\sqrt{5}-1}{2})
$$

Subtracting these,
the $$\ln^2$$ terms cancel out
and we get

$$
\begin{array}\\
L_2(\dfrac{\sqrt{5}-1}{2})-L_2(\dfrac{3-\sqrt{5}}{2}))
&=\dfrac{\pi^2}{10}-\dfrac{\pi^2}{15}\\
&=\dfrac{\pi^2}{30}\\

\text{so} \\

5(L_2(\dfrac{\sqrt{5}-1}{2})-L_2(\dfrac{3-\sqrt{5}}{2})))
&=\dfrac{\pi^2}{6}\\
&=\zeta(2)\\
\end{array}
$$

