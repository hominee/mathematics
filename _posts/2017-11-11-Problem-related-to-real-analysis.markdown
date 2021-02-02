---
layout: post
title: Problem related to real analysis
tag:
 - real-analysis

description: Problem related to real analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is the set of discontinuity of $$f$$ countable?

<!–-break-–>


Suppose $$f:[0,1]\rightarrow\mathbb{R}$$ is a bounded function satisfying: for each $$c\in [0,1]$$ there exist the limits $$\lim_{x\rightarrow c^+}f(x)$$ and $$\lim_{x\rightarrow c^-}f(x)$$.
 Is true that the set of discontinuity of $$f$$ is countable?
.


# Answer 


Hopefully this more tedious proof is more illustrative...
In light of the assumptions on $$f$$, there are two ways that $$f$$ can fail to be continuous: (1) the left and right hand limits differ, or (2) the limits are equal, but the function value differs from the limit (thanks to @GEdgar for pointing this out).
Let $$\epsilon>0$$ and $$\Delta_\epsilon = \{ x \|\, \|\lim_{y \downarrow x}f(y) - \lim_{y \uparrow x}f(y)\| \geq \epsilon \}$$. If $$\Delta_\epsilon$$ is not finite, then since $$[0,1]$$ is compact, there exists an accumulation point $$\hat{x} \in [0,1]$$. Let $$c_+ = \lim_{y \downarrow \hat{x}}f(y), c_- = \lim_{y \uparrow \hat{x}}f(y)$$. (

**Note** that it is possible that $$c_- = c_+$$.) By assumption, there exists some $$\delta>0$$ such that for $$y \in (\hat{x}-\delta,\hat{x})$$, $$\|f(y)-c_-\| < \frac{\epsilon}{4}$$ and for $$y \in (\hat{x}, \hat{x}+\delta)$$, $$\|f(y)-c_+\| < \frac{\epsilon}{4}$$. However, this implies that $$\hat{x}$$ is an isolated point of $$\Delta_\epsilon$$, which is a contradiction. Hence $$\Delta_\epsilon$$ is finite.
If we let $$\Delta = \cup_n \Delta_{\frac{1}{n}}$$, we see that $$\Delta $$ is at most countable.
@GEdgar has pointed out an omission in my proof: It is possible that the two limits coincide at a point, but the function is still discontinuous at that point, ie, $$\Delta$$ is not the entire set of discontinuities.
Let $$\Gamma_\epsilon = \{ x \|\, \lim_{y \downarrow x}f(y) = \lim_{y \uparrow x}f(y), \ \|\lim_{y \downarrow x}f(y)-f(x) \| \geq \epsilon \}$$. Suppose, as above, that $$\Gamma_\epsilon$$ is not finite, and let $$\hat{x}$$ be an accumulation point. Let $$c_+, c_-$$ be the limits as above. Again, there exists a $$\delta>0$$ such that if $$y \in (\hat{x}-\delta,\hat{x})$$, $$\|f(y)-c_-\| < \frac{\epsilon}{4}$$, and similarly, if $$y \in (\hat{x}, \hat{x}+\delta)$$, $$\|f(y)-c_+\| < \frac{\epsilon}{4}$$. Consequently, $$\hat{x}$$ is isolated, hence a contradiction, and $$\Gamma_\epsilon$$ is finite.
If we let $$\Gamma= \cup_n \Gamma_{\frac{1}{n}}$$, we see that $$\Gamma$$ is at most countable.
Since the set of discontinuities is $$\Delta \cup \Gamma$$, we see that the set of discontinuities is at most countable.

