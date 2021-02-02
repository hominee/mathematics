---
layout: post
title: How can I find all solutions to differential equation
tag:
 - ordinary-differential-equations

description: How can I find all solutions to differential equation

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How can we  find all solutions to differential equation?

<!–-break-–>


How one can find all functions $$f$$ that there exists $$f'$$ satisfying $$(f(x))^2+(f'(x))^2=1$$? we  just found solutions $$f(x)=1,-1,\sin x$$.

# Answer 



We are going to obtain in two steps all $$C^1$$ solutions of

 $$ 
\tag{0}(f(x))^2+(f'(x))^2=1.
 $$ 

Step 1: Let us follow a method similar to that given either by @David Quinn for example or @we an Eerland or @Battani, with some supplementary precision on the intervals of validity.
Let $$f$$ be a solution to $$(0)$$. 
Let us consider a point $$x_0$$. Either

case 1: 
$$|f(x_0)|=1$$ or 

case 2: 
$$|f(x_0)|<1$$, which implies $$|f'(x_0)|>0$$. 

Let us detail case 2. 
By continuity of $$f$$, there exist $$\epsilon_1>0$$ such that on $$we _1:=(x_0-\epsilon_1,x_0+\epsilon_1)$$ we have $$|f(x)|<1$$.
By continuity of $$f'$$, there exist $$\epsilon_2>0$$ such that on $$we _2:=(x_0-\epsilon_2,x_0+\epsilon_2)$$ we have $$|f'(x)|>0$$.
Let us transform $$(0)$$ into 

 $$ 
\tag{1}\dfrac{y'}{\sqrt{1-y^2}}=s
 $$ 

Differential equation (1) needs to be considered for values of variable $$x$$ in $$we :=we _1 \cap we _2$$ in order that the ratio is well defined and that the sign $$s=\pm1$$ doesn't change throughout this interval $$we $$.
Taking a primitive function on $$we $$ of both sides of (1):

 $$ 
\arcsin(y)=s x+\varphi \ \ \ \text{for some constant} \ \varphi.
 $$ 

Thus $$y=f(x)=\sin(s x+ \varphi)$$ on interval $$we $$ with either $$s=1$$ or $$s=-1$$.
This solution can be presented under the simpler form: $$f(x)=\sin(x+ \varphi)$$ (one finds back case $$s=-1$$ through replacement of  $$\varphi$$  by $$\varphi+\pi$$).
Conclusion of step 1: a solution $$f$$ and a particular point $$x_0$$ being given, there are two cases:
\begin{cases} (a) \ \text{Either} \ f(x_0) = \pm1 \ \text{or}\\ (b) \ \text{There exist an interval} \ J \ \text{containing} \ x_0 \ \text{
such that,} \forall x \in J, \ f(x)=\sin(x+\varphi) \ \end{cases}
for a certain $$\varphi$$ ($$J$$ being any interval of validity of solution $$f$$, including interval $$we $$ as defined before).
Step 2: We are going to obtain these intervals $$J$$ by using a topological argument (A recall about topology can be found there). From (0), we know that the values taken by $$f(x)$$ are in the closed interval $$[-1,1]$$. Now consider the set of values of $$x$$ such that their image is in the open interval $$(-1,1)$$:

 $$ 
S:=\{x \ | -1<f(x)<1 \}=f^{-1}((0,1)). 
 
$$
S$$ is an open set, being the preimage of an open set by a continuous function; as such, it can be written as a countable union of open intervals $$S=\bigcup_k (a_k,b_{k})$$ (see this). in this way ;
(b) will be valid on open intervals $$(a_k,b_k)$$
(a) will be valid on closed intervals $$[b_k,a_{k+1}]$$.
At junction point  $$b_k$$, the only possible way to preserve $$C^1$$ continuity is by taking, according to the value of $$\lim_{x\rightarrow b_k} f(x)$$ value $$1$$ or $$-1$$ for the whole closed interval $$[b_k,a_{k+1}]$$. Same procedure at the initial junction point $$a_k$$.
Let the curve of $$y=sin(x)$$ restricted 

to $$[0,\pi/2]$$ (increasing) be called an $$s_+$$ arc.
to $$[\pi/2,\pi]$$ (decreasing) be called an $$s_-$$ arc.

Let a line segment of any positive length with equation $$y=1$$ (resp. $$y=-1$$) be called a $$1_+$$ (resp a $$1_-$$).
Thus one can describe the possible $$C^1$$ integral curves of (0) by a $$C^1$$ "glueing" of curves as a (finite or infinite) repetition of the following "motives":

 $$ 
\cases{1_+^*[s_-1_-^*s_+1_+^*]^*\\(1_-)^*[s_+1_+^*s_-1_+^*]^*}
 $$ 

(mathematical "grammars" notations, where exponant * means 0 or more times). See figure.

intervals where the solution is constant may have any length.  
"Phase shifts" $$\varphi_k$$ of the sine curves are specific  to each interval.
it is to be noted that closed intervals $$[b_k,a_{k+1}]$$ can be reduced to a point. 

Appendix : we  had, at first, obtained a certain family of solutions by 
differentiating both sides of $$(0)$$:

 $$ 
2f'(x)(f(x)+f''(x))=0.
 $$ 

After a certain number of hours spent on this method, which assumes $$f \in C^2$$, we  realized that it is impossible to go back to the initial equation dealing with $$C^1$$ solutions. 
Added on August 30th: this differential geometry question gives an application of (0).

