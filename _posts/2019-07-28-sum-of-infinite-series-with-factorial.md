---
layout: post
title: Sum of infinite series with factorial
tags:
  - infinite series
  - fractorial
description: >
  #Howdy! This is an example blog post that shows several types of HTML content
  #supported in this theme.
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---

# Question

$$
\begin{equation*}
\sum _{n=1} ^{ \infty } \frac{n+2}{n!+(n+1)!+(n+2)!}
\end{equation*}
$$

<!–-break-–>

Have you ever come across the infinite sum such as  

$$ \sum _{n=1} ^{ \infty } \frac{1}{(n-1)! (n+1)} \,\, \text{or} \,\, \sum _{n=1} ^{ \infty } \frac{1}{(n-1)! + n! }$$

the trick lies in that  

$$
\label{trick}  
\begin{equation}
\frac{1}{(n-1)! (n+1)} = \frac{n}{(n+1)!} = \frac{n+1 - 1}{(n+1)!} = (n!)^{-1} - (n+1)!^{-1}
\end{equation}
$$

This question is the extention of formula $$\ref{trick}$$, since  

$$

\label{trick0} 
\begin{equation}
\frac{ n+2 }{ n!+(n+1)!+(n+2)! } = \frac{n+2}{n!( 1+ n+1 (n+1) (n+2) ) } = \frac{1}{n!(n+2)}   
\end{equation}
$$


Now we can handle it with ease combing formula $$\ref{trick}$$ and $$\ref{trick0}$$. I will leave the rest 
proof to you. (If you get $$\frac{1}{2}$$ congratulations, if not, one more try.)
