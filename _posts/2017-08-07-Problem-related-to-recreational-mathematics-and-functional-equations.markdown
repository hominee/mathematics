---
layout: post
title: Problem related to recreational mathematics and functional equations
tag:
 - recreational-mathematics
 - functional-equations

description: Problem related to recreational mathematics and functional equations

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is there a real-valued function $$f$$ such that $$f(f(x)) = -x$$?

<!–-break-–>

# Answer 


There is.
Let $$\{A,B\}$$ be a partition of the positive reals such that $$|A|=|B|=|\mathbb{R}|$$, and let $$\varphi:A\to B$$ be a bijection. Define $$f:\mathbb{R}\to\mathbb{R}$$ as follows: 

 $$ 
f(x)=\begin{cases}
0,&\text{if }x=0\\
\varphi(x),&\text{if }x\in A\\
-\varphi^{-1}(x),&\text{if }x\in B\\
-\varphi(-x),&\text{if }-x\in A\\
\varphi^{-1}(-x),&\text{if }-x\in B\;.
\end{cases}
 $$ 

Then 

 $$ 
\begin{align*}
f(f(x))&=\begin{cases}
0,&\text{if }x=0\\
f(\varphi(x)),&\text{if }x\in A\\
f(-\varphi^{-1}(x)),&\text{if }x\in B\\
f(-\varphi(-x)),&\text{if }-x\in A\\
f(\varphi^{-1}(-x)),&\text{if }-x\in B\;.
\end{cases}\\\\
&=\begin{cases}
0,&\text{if }x=0\\
-\varphi^{-1}(\varphi(x)),&\text{if }x\in A\\
-\varphi(\varphi^{-1}(x)),&\text{if }x\in B\\
\varphi^{-1}(\varphi(-x)),&\text{if }-x\in A\\
\varphi(\varphi^{-1}(-x)),&\text{if }-x\in B
\end{cases}\\\\
&=-x\;.
\end{align*}
 $$ 

The idea is simply that $$f$$ permutes the sets $$A,B,-A$$, and $$-B$$ in the order

 $$ 
A\stackrel{f}\longrightarrow B\stackrel{f}\longrightarrow -A\stackrel{f}\longrightarrow -B\stackrel{f}\longrightarrow A
 $$ 

while leaving $$0$$ fixed. (Here $$-A= \{-a:a\in A\}$$, and similarly for $$-B$$.)
Added: we t is possible, though a bit messy, to define $$A,B$$ and $$\varphi$$ explicitly. We may, for example, set $$A=(0,1]$$ and $$B=(1,\to)$$ and define $$\varphi$$ as follows. First, for $$n\in\omega$$ let $$\varphi(2^{-n})=2^{n+1}$$, so that $$\varphi(1)=2,\varphi(1/2)=4,\varphi(1/4)=8$$, and so on. Then let $$\varphi$$ map the interval $$(2^{-(n+1)},2^{-n})$$ to the interval $$(2^n,2^{n+1})$$ in the obvious way, taking $$x$$ to $$1/x$$.

