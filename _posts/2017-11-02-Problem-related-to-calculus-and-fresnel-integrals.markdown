---
layout: post
title: Problem related to calculus and fresnel integrals
tag:
 - calculus
 - integration
 - complex-analysis
 - analysis
 - fresnel-integrals

description: Problem related to calculus and fresnel integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proof only by transformation that : $$ \int_0^\infty \cos(x^2) dx = \int_0^\infty \sin(x^2) dx $$

<!–-break-–>


This was a  question in our exam and we did not know which change of variables or trick to apply 
How to show  by inspection ( change of variables or whatever trick  ) that 


$$

 \int_0^\infty \cos(x^2) dx = \int_0^\infty \sin(x^2) dx \tag{I} 

$$


Computing the values of these integrals are known routine.
 Further from their values the equality holds.
 But can we show the equality beforehand?



**Note**: we are  not asking for computation since it can be found here 
  and we have as well that, 
  

$$

 \int_0^\infty \cos(x^2) dx = \int_0^\infty \sin(x^2) dx =\sqrt{\frac{\pi}{8}}

$$


  and the result can be recover here, Evaluating $$\int_0^\infty \sin x^2\, dx$$ with real methods?.


Is there any trick to prove the equality in (I) without computing the exact values of these integrals beforehand?
.


# Answer 


Employing the change of variables $$2u =x^2$$ We get 

$$

I=\int_0^\infty \cos(x^2) dx =\frac{1}{\sqrt{2}}\int^\infty_0\frac{\cos(2x)}{\sqrt{x}}\,dx

$$

 

$$

 J=\int_0^\infty \sin(x^2) dx=\frac{1}{\sqrt{2}}\int^\infty_0\frac{\sin(2x)}{\sqrt{x}}\,dx 

$$



Summary: We will prove that  $$J\ge 0$$ and $$I\ge 0$$  so that, proving that $$I=J$$ is equivalent to  

$$

 \color{blue}{0= (I+J)(I-J)=I^2 -J^2 =\lim_{t \to 0}I_t^2-J^2_t}

$$


  Where, 

$$

I_t = \int_0^\infty e^{-tx^2}\cos(x^2) dx~~~~\text{and}~~~ J_t = \int_0^\infty e^{-tx^2}\sin(x^2) dx

$$


  $$t\mapsto I_t$$ and $$t\mapsto J_t$$ are clearly continuous due to the present of the integrand factor $$e^{-tx^2}$$.

However, By Fubini we have,
\begin{split}
I_t^2-J^2_t&=& \left(\int_0^\infty e^{-tx^2}\cos(x^2) dx\right)  \left(\int_0^\infty e^{-ty^2}\cos(y^2) dy\right) \\&-&  \left(\int_0^\infty e^{-tx^2}\sin(x^2) dx\right)  \left(\int_0^\infty e^{-ty^2}\sin(y^2) dy\right) \\
&=& \int_0^\infty \int_0^\infty e^{-t(x^2+y^2)}\cos(x^2+y^2)dxdy\\
&=&\int_0^{\frac\pi2}\int_0^\infty re^{-tr^2}\cos r^2 drd\theta\\&=&\frac\pi4 Re\left( \int_0^\infty \left[\frac{1}{i-t}e^{(i-t)r^2}\right]' dr\right)\\
&=&\color{blue}{\frac\pi4\frac{t}{1+t^2}\to 0~~as ~~~t\to 0}
\end{split}
To end the proof: Let us show that $$I> 0$$ and $$J> 0$$. Performing an integration by part we obtain


$$

J = \frac{1}{\sqrt{2}} \int^\infty_0\frac{\sin(2x)}{x^{1/2}}\,dx=\frac{1}{\sqrt{2}}\underbrace{\left[\frac{\sin^2 x}{x^{1/2}}\right]_0^\infty}_{=0} +\frac{1}{2\sqrt{2}} \int^\infty_0\frac{\sin^2 x}{x^{3/2}}\,dx\color{red}{>0}

$$


Given that $$\color{red}{\sin 2x= 2\sin x\cos x =(\sin^2x)'}$$. Similarly we have,


$$

we =  \frac{1}{\sqrt{2}}\int^\infty_0\frac{\cos(2x)}{\sqrt{x}}\,dx=\frac{1}{2\sqrt{2}}\underbrace{\left[\frac{\sin 2 x}{x^{1/2}}\right]_0^\infty}_{=0} +\frac{1}{4\sqrt{2}} \int^\infty_0\frac{\sin 2 x}{x^{3/2}}\,dx\\=
 \frac{1}{4\sqrt{2}}\underbrace{\left[\frac{\sin^2 x}{x^{1/2}}\right]_0^\infty}_{=0} +\frac{3}{8\sqrt{2}} \int^\infty_0\frac{\sin^2 x}{x^{5/2}}\,dx\color{red}{>0}

$$



Conclusion:  $$~~~I^2-J^2 =0$$, $$I>0$$ and $$J>0$$ impliy $$I=J$$. 

**Note** that we did not attempt to compute neither the value of $$~~I$$ nor $$J$$.

Extra-to-the answer However using similar technique in above prove one can easily arrives at the following 

$$

\color{blue}{I_tJ_t = \frac\pi8\frac{1}{t^2+1}}

$$

 from which one get the following  explicit value of 

$$

\color{red}{I^2=J^2= IJ = \lim_{t\to 0}I_tJ_t =\frac{\pi}{8}}

$$



