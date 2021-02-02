---
layout: post
title: Problem related to functional analysis and lp spaces
tag:
 - functional-analysis
 - measure-theory
 - lp-spaces

description: Problem related to functional analysis and lp spaces

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

If $$f \in L^{\infty}$$ and $$\exists r < \infty$$ so that $$\|f\|_r < \infty$$, show $$\lim_{p \rightarrow \infty} \|f\|_p = \|f\|_{\infty}$$ 

<!–-break-–>


Let $$(X,\mu)$$ be a possibly infinite measure space. Assume $$\exists r < \infty$$ with $$\|f\|_r < \infty$$ and that $$\|f \|_{\infty} < \infty$$. Show that $$\lim_{p \rightarrow \infty} \|f_p\| = \|f\|_{\infty}$$. 
This is from Real and Complex by Rudin, chapter 3 exercise 14.
Progress:
we have shown that $$\|f\|_{\infty} \le \lim_{p \rightarrow \infty} \|f\|_p$$ as follows,
Fix $$\epsilon > 0$$. Let $$E = \{x : |f(x)| > \|f\|_{\infty} - \epsilon \}$$. Then observe


$$

 \|f\|_p \ge \left( \int_{E} |f|^p d\mu \right)^{1/p} > \left( \int_{E}(\| f \|_{\infty} - \epsilon)^{p} d\mu \right)^{1/p} = \left( \|f\|_{\infty} - \epsilon \right) \mu(E)^{1/p}, 

$$


thus, $$\lim_{p \rightarrow \infty} \|f\|_p \ge \|f\|_{\infty} - \epsilon$$ since $$\mu(E) < \infty$$. 
we attempted something similar for the other direction, but could not say the measure of a set was finite like (we think) we need for this argument to work. Here is what we tried:
Since $$\|f\|_r < \infty, \exists R$$ so that 
$$|x| > R \implies f(x) < \frac{1}{2}$$. Let $$A = \{ x : |x| \le R \}$$ and $$B = \{x : |x| > R \}$$. Then,


$$

\|f\|_{p} \le \left( \int_{A} |f|^p d \mu + \int_{B} \frac{1}{2^p} d\mu\right)^{1/p} = \left( \int_{A} |f|^p d\mu + \frac{1}{2^p} \mu( B ) \right)^{1/p}.

$$


If $$\mu(B) < \infty$$ this can easily show the desired result. Moreover, if we could show that there is a family of sets $$\{B_p\}$$ that act similarly so that $$\mu(B_p)$$ grows slower than $$e^p$$, then we can also complete the proof.
Thoughts?
.

# Answer 


For the first part you have to use $$\liminf$$, as you don't still know that the limit exists. 
For the second part, you are thinking as if $$X$$ was $$\mathbb R^n$$, which it might not be. One way of attacking the problem along your line of thought  would be to assume $$\|f\|_\infty=1$$ (i.e., work with $$f/\|f\|_\infty$$). Then, for $$p>r$$,


$$


\left(\int_X|f|^pd\mu\right)^{1/p}\leq\left(\int_X|f|^rd\mu\right)^{1/p}=\|f\|_r^{r/p}


$$


Then 


$$


\limsup_{p\to\infty}\|f\|_p\leq1.


$$


Now you can scale back with $$\|f\|_\infty$$ to get 


$$


\limsup_{p\to\infty}\|f\|_p\leq\|f\|_\infty.


$$


Another way of doing this second part is to use Hölder's inequality:


$$


\|f\|_p^p=\int_X|f|^pd\mu=\int_X|f|^r|f|^{p-r}d\mu\leq \|f\|_\infty^{p-r}\,\|f\|_r^r.


$$


So


$$


\limsup_{p\to\infty}\|f\|_p\leq\limsup_{p\to\infty}\|f\|_\infty^{(p-r)/p}\,\|f\|_r^{r/p}=\|f\|_\infty.


$$



