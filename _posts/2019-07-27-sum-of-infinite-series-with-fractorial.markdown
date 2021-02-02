---
layout: post
title:  "Sum of infinite series with factorial"
date:   2019-07-28 15:31:07 -0700
categories: ""
tag:     infinite series, fractorial
---
# Question

$$
\begin{equation*}
\sum _{n=1} ^{ \infty } \frac{n+2}{n!+(n+1)!+(n+2)!}
\end{equation*}
$$


Have you ever come across the infinite sum such as  

$$ 
\sum _{n=1} ^{ \infty } \frac{1}{(n-1)! (n+1)} \,\, \text{or} \,\, \sum _{n=1} ^{ \infty } \frac{1}{(n-1)! + n! }
$$

the trick lies in that  

$$
\label{trick}
\begin{equation} 
\frac{1}{(n-1)! (n+1)} = \frac{n}{(n+1)!} = \frac{n+1 - 1}{(n+1)!} = (n!)^{-1} - (n+1)!^{-1}
\end{equation}
$$

This question is the extention of formula $$\eqref{trick}$$, since  

$$
\label{trickk}
\begin{equation}
\frac{n+2}{n!+(n+1)!+(n+2)!} = \frac{n+2}{n![1+ n+1 (n+1)(n+2)]} = \frac{1}{n!(n+2)}
\end{equation}
$$

Now we can handle it with ease combing formula $$\eqref{trick}$$ and $$\eqref{trickk}$$. I will leave the rest 
proof to you. (If you get $$\frac{1}{2}$$ congratulations, if not, one more try.)