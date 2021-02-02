---
layout: post
title: sum related to Ramanujan phi function
tags:
  - sum  
  - closed-form
  - real-analysis
  - Ramanujan phi function
  
description:  
  sum related to Ramanujan $$\phi$$ function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :


$$

\sum_{k=1}^{\infty}{k\over [(pk)^2-1][(qk)^2-1]}

$$


Observing Ramanujan [phi-function][1]

Given two examples


$$
{1\over 2}+\sum_{k=1}^{\infty}{1\over (2k)^3-2k}=\ln 2\tag1
$$



$$
1+2\sum_{k=1}^{\infty}{1\over (3k)^3-3k}=\ln 3\tag2
$$


Let the Ramanujan phi-function takes the general form of:


$$
a+b\sum_{k=1}^{\infty}{1\over (pk)^3-pk}=\ln x\tag3
$$



$$
c+d\sum_{k=1}^{\infty}{1\over (qk)^3-qk}=\ln y\tag4
$$


where $$p<q$$ and $$p>1$$


  [1]: http://mathworld.wolfram.com/RamanujanPhi-Function.html



<!–-break-–>


# Answer
Using partial fractions, exactly like you seem to have done. Another way of presenting the result is

Since by partial fractions

$$
{k\over [(pk)^2-1][(qk)^2-1]}=\frac{p}{q^2-p^2}{1\over pk[(pk)^2-1]}-\frac{q}{q^2-p^2}{1\over qk[(qk)^2-1]}
$$


we can sum both sides and later make substitutions using $$\sum_{k=1}^{\infty}{1\over pk[(pk)^2-1]}=\frac{\log x - a}{b}$$ and $$\sum_{k=1}^{\infty}{1\over qk[(qk)^2-1]}=\frac{\log y-c}{d}$$

Thus

$$
\begin{align*} \sum_{k=1}^{\infty}{k\over [(pk)^2-1][(qk)^2-1]}&=\frac{p}{q^2-p^2}\sum_{k=1}^{\infty}{1\over pk[(pk)^2-1]}-\frac{q}{q^2-p^2}\sum_{k=1}^{\infty}{1\over qk[(qk)^2-1]}\\
&=\frac{1}{q^2-p^2} \left( \frac{p(\log x-a)}{b}-\frac{q(\log y-c)}{d}\right)\\
&=\frac{1}{q^2-p^2}\frac{1}{bd}\left( (qcb-pad)+ (pd\log x-qb \log y) \right)
\end{align*}
$$

