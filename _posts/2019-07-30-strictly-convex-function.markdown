---
layout: post
title: Strictly convex function
tags:
  - convex function
  - concave function
  - deferential

description: >
  Strictly convex function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Let function $$f$$:

$$ f: (x,y) \to \mathbb{R}$$ 

be continuous differential function, and for $$(x,y) \in \mathbb{R} ^2 $$ there exists only one $$z$$ such that 

$$
\begin{equation*}
\frac{f(x) - f(y)}{x-y} = f'(z)
\end{equation*}
$$

show that $$f(x)$$ is strictly convex function or strictly concave function.

<!–-break-–>

# Answer

This is an application of $$\href{https://en.wikipedia.org/wiki/Rolle%27s_theorem}{Rolle's theorem}$$, we could proof it 
by controdiction, 

If not, there exist at least two points $$z_1 \neq z_2$$ such that 

$$
\frac{f(x_1) - f(y_1)}{x_1-y_1} = f'(z_1), \frac{f(x_2) - f(y_2)}{x_2-y_2} = f'(z_2)
$$

then by Rolle theorem there exists at least a $$z$$ for which 

$$
f''(z)  = \frac{f'(z_1) - f'(z_2)}{z_1 - z_2} =  0
$$

which controdicte the definition that $$f''(x) \neq 0$$.