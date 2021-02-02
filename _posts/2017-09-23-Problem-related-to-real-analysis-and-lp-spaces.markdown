---
layout: post
title: Problem related to real analysis and lp spaces
tag:
 - real-analysis
 - functional-analysis
 - measure-theory
 - lp-spaces

description: Problem related to real analysis and lp spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Limit of $$L^p$$ norm

<!–-break-–>



# Answer 


Fix $$\delta>0$$ and let 
$$S_\delta:=\{x,|f(x)|\geqslant \lVert f\rVert_\infty-\delta\}$$ 
for $$\delta<\lVert f\rVert_\infty$$. We have 


$$

\lVert f\rVert_p\geqslant \left(\int_{S_\delta}(\lVert f\rVert_\infty-\delta)^pd\mu\right)^{1/p}=(\lVert f\rVert_\infty-\delta)\mu(S_\delta)^{1/p},

$$


since $$\mu(S_\delta)$$ is finite and positive. 
 This gives 


$$

\liminf_{p\to +\infty}\lVert f\rVert_p\geqslant\lVert f\rVert_\infty.

$$


As 
$$|f(x)|\leqslant\lVert f\rVert_\infty$$ for almost every $$x$$, we have for $$p>q$$, 

$$


\lVert f\rVert_p\leqslant\left(\int_X|f(x)|^{p-q}|f(x)|^qd\mu\right)^{1/p}\leqslant \lVert f\rVert_\infty^{\frac{p-q}p}\lVert f\rVert_q^{q/p},

$$


giving the reverse inequality.

