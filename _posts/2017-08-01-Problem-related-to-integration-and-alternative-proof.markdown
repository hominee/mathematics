---
layout: post
title: Problem related to integration and alternative proof
tag:
 - integration
 - definite-integrals
 - alternative-proof

description: Problem related to integration and alternative proof

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

we integral $$\int_0^1 \frac{dx}{\sqrt[3]{x(1-x)}(1-x(1-x))}$$

<!–-break-–>



Prove, using elementary methods, that
  
 $$ 
\int_0^1 \frac{dx}{\sqrt[3]{x(1-x)}(1-x(1-x))}=\frac{4\pi}{3\sqrt 3}
 $$ 


we  have seen this integral in the following post, however all answers presented exploits complex analysis or heavy series.
But according to mickep's answer even the indefinite integral possess a primitive in terms of elementary functions. we are  not that insane to try and find that by hand, however it gives me great hope that we can find an elementary approach for the definite integral.

# Answer 


Given the function $$f : (0,\,1) \to \mathbb{R}
$$
 
$$
f(x) := \frac{1}{\sqrt[3]{x\,(1 - x)}\left(1 - x(1 - x)\right)}\,,

 $$ 

we are interested in the calculation of

 $$ 

we  := \int_0^1 f(x)\,\text{d}x\,.

 $$ 

First of all it is good to observe that:

 $$ 

f(1 - x) = f(x), \quad \forall \, x \in (0,\,1)

 $$ 

then:

 $$ 

we  = 2 \int_0^{\frac{1}{2}} f(x)\,\text{d}x\,.

 $$ 

At this point, since:

 $$ 

f\left(\frac{1 - \sqrt{4\,t^3 + 1}}{2}\right) = -\frac{1}{t\left(t^3 + 1\right)}\,, \quad \quad \frac{\text{d}}{\text{d}t}\left(\frac{1 - \sqrt{4\,t^3 + 1}}{2}\right) = -\frac{3\,t^2}{\sqrt{4\,t^3 + 1}}

 $$ 

it follows that:

 $$ 

we  = -6 \int_{-\frac{1}{\sqrt[3]{4}}}^0 \frac{t}{t^3 + 1}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}\,.

 $$ 

Now we can take advantage of the power of Rubi in Wolfram Mathematica:

Paclet  ["install"](https://github.com/RuleBasedwe/integration/Rubi/releases/download/4.16.1.0/Rubi-4.16.1.0.paclet);


$$ 
\int t/((t^3 + 1) \sqrt{4 t^3 + 1}), dt
$$


from which:

 $$ 

we  = 
-6 \int_{-\frac{1}{\sqrt[3]{4}}}^0 \left[
\frac{2\,t - 1}{6\,(t + 1)\,\sqrt{4\,t^3 + 1}} + 
\frac{t^2}{2\left(t^3 + 1\right)\sqrt{4\,t^3 + 1}} - \\
\frac{2\,t^3 - 3\,t^2 - 1}{6\,t\left(t^2 - t + 1\right)\sqrt{4\,t^3 + 1}} -
\frac{1}{6\,t\,\sqrt{4\,t^3 + 1}}
\right]\text{d}t\,.

 $$ 

Hence a primitive in terms of elementary functions is:

 $$ 

we  = 
-6\left[
- \frac{\arctan\left(\frac{\sqrt{3}\,(1 + 2\,t)}{\sqrt{4\,t^3 + 1}}\right)}{3\sqrt{3}} +
\frac{\arctan\left(\frac{\sqrt{4\,t^3 + 1}}{\sqrt{3}}\right)}{3\sqrt{3}} - \\
\frac{1}{3}\,\text{arctanh}\left(\frac{1 - 2\,t}{\sqrt{4\,t^3 + 1}}\right) +
\frac{1}{9}\,\text{arctanh}\left(\sqrt{4\,t^3 + 1}\right)
\right]_{t = -\frac{1}{\sqrt[3]{4}}}^{t = 0}

 $$ 

and therefore as desired:

 $$ 

we  = 
\frac{4\pi}{3\sqrt{3}}\,.

 $$ 


Like any other CAS system, also Rubi follows the rules written by the programmers, so it's always possible to proof by hand how much is executed. Specifically, the theory on which the above rule introduced by Martin Welz is based can be studied in E. GOURSAT Note sur quelques intégrales pseudo-elliptiques (1887). Therefore, based on what is written on page 114, the resolving technique of the integral under consideration can be studied in S. GÜNTHER Sur l’évaluation de certaines intégrales pseudo-elliptiques (1882).
we n this case:

 $$ 

S \equiv \int \frac{t}{t^3 + 1}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

then imposing:

 $$ 

\frac{t}{t^3 + 1} = 
\frac{\alpha\,t^2}{t^3 + 1} +
\frac{\alpha_1\,t^2 + \beta_1\,t + \gamma_1}{t + 1} +
\frac{\alpha_2\,t^2 + \beta_2\,t + \gamma_2}{t^2 - t + 1}

 $$ 

the identification gives the values:

 $$ 

\alpha = \frac{1}{2}\,, \quad
\alpha_1 = 0\,, \quad
\beta_1 = \frac{1}{3}\,, \quad
\gamma_1 = -\frac{1}{6}\,, \quad
\alpha_2 = -\frac{1}{3}\,, \quad
\beta_2 = \frac{1}{3}\,, \quad
\gamma_2 = \frac{1}{6}

 $$ 

ie:

 $$ 

\frac{t}{t^3 + 1} = 
\frac{t^2}{2\left(t^3 + 1\right)} +
\frac{2\,t - 1}{6\left(t + 1\right)} -
\frac{2\,t^2 - 2\,t - 1}{6\left(t^2 - t + 1\right)}

 $$ 

from which:

 $$ 

S = 
\int \frac{t^2}{2\left(t^3 + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}} +
\int \frac{2\,t - 1}{6\left(t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}} +
\int \frac{2\,t^2 - 2\,t - 1}{-6\left(t^2 - t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}} \,.

 $$ 

Now, for the first integral:

 $$ 

S_1 \equiv \int \frac{t^2}{2\left(t^3 + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

according to the method described in the paper:

 $$ 

u = \frac{\alpha\,t^3 + \beta\,t^2 + \gamma\,t + \delta}{\sqrt{4\,t^3 + 1}}

 $$ 

then imposing:

 $$ 

\frac{\text{d}u}{m\,u^2 + n} = \frac{t^2}{2\left(t^3 + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

ie:

 $$ 

\frac{\text{d}u}{\text{d}t}\,\frac{2\left(t + 1/t^2\right)\sqrt{4\,t^3 + 1}}{m\,u^2 + n} = 1

 $$ 

the identification gives the values:

 $$ 

\alpha = 0\,, \quad
\beta = 0\,, \quad
\gamma = 0\,, \quad
\delta = - \frac{1}{3}\,, \quad
m = 27\,, \quad
n = 1

 $$ 

ie:

 $$ 

S_1 
= \int \frac{\text{d}u}{27\,u^2 + 1}
= \frac{\arctan\left(3\sqrt{3}\,u\right)}{3\sqrt{3}} + c_1
= -\frac{\arctan\left(\frac{\sqrt{3}}{\sqrt{4\,t^3 + 1}}\right)}{3\sqrt{3}} + c_1\,.

 $$ 

Similarly, for the second integral:

 $$ 

S_2 \equiv \int \frac{2\,t - 1}{6\left(t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

putting:

 $$ 

u = \frac{\alpha\,t^2 + \beta\,t + \gamma}{\sqrt{4\,t^3 + 1}}

 $$ 

then imposing:

 $$ 

\frac{\text{d}u}{m\,u^2 + n} = \frac{2\,t - 1}{6\left(t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

ie:

 $$ 

\frac{\text{d}u}{\text{d}t}\,\frac{\frac{6\left(t + 1\right)}{2\,t - 1}\sqrt{4\,t^3 + 1}}{m\,u^2 + n} = 1

 $$ 

the identification gives the values:

 $$ 

\alpha = 0\,, \quad
\beta = -\frac{2}{3}\,, \quad
\gamma = -\frac{1}{3}\,, \quad
m = 27\,, \quad
n = 1

 $$ 

ie:

 $$ 

S_2 
= \int \frac{\text{d}u}{27\,u^2 + 1}
= \frac{\arctan\left(3\sqrt{3}\,u\right)}{3\sqrt{3}} + c_2
= -\frac{\arctan\left(\frac{\sqrt{3}\left(2\,t + 1\right)}{\sqrt{4\,t^3 + 1}}\right)}{3\sqrt{3}} + c_2\,.

 $$ 

For the third integral 

 $$ 

S_3 \equiv \int \frac{2\,t^2 - 2\,t - 1}{-6\left(t^2 - t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

this transformation fails and therefore the only hope that remains about the pseudo-ellipticity of the integral consists in further decomposing the rational fraction; in particular, imposing:

 $$ 

\frac{2\,t^2 - 2\,t - 1}{-6\left(t^2 - t + 1\right)}
= \frac{\alpha}{-6\,t} + \frac{\alpha_1\,t^3 + \beta_1\,t^2 + \gamma_1\,t + \delta_1}{-6\,t\left(t^2 - t + 1\right)}

 $$ 

the identification gives the values:

 $$ 

\alpha = 1\,, \quad
\alpha_1 = 2\,, \quad
\beta_1 = -3\,, \quad
\gamma_1 = 0\,, \quad
\delta_1 = -1

 $$ 

ie:

 $$ 

\frac{2\,t^2 - 2\,t - 1}{-6\left(t^2 - t + 1\right)} = 
\frac{1}{-6\,t} + \frac{2\,t^3 - 3\,t^2 - 1}{-6\,t\left(t^2 - t + 1\right)}

 $$ 

from which:

 $$ 

S_3 = 
\int \frac{1}{-6\,t}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}} +
\int \frac{2\,t^3 - 3\,t^2 - 1}{-6\,t\left(t^2 - t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}} \,.

 $$ 

Now, again, for the first integral:

 $$ 

S_{3,1} \equiv \int \frac{1}{-6\,t}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

putting:

 $$ 

u = \frac{\alpha\,t^3 + \beta\,t^2 + \gamma\,t + \delta}{\sqrt{4\,t^3 + 1}}

 $$ 

then imposing:

 $$ 

\frac{\text{d}u}{m\,u^2 + n} = \frac{1}{-6\,t}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

ie:

 $$ 

\frac{\text{d}u}{\text{d}t}\,\frac{-6\,t\,\sqrt{4\,t^3 + 1}}{m\,u^2 + n} = 1

 $$ 

the identification gives the values:

 $$ 

\alpha = 0\,, \quad
\beta = 0\,, \quad
\gamma = 0\,, \quad
\delta = \frac{1}{9}\,, \quad
m = -81\,, \quad
n = 1

 $$ 

ie:

 $$ 

S_{3,1} 
= \int \frac{\text{d}u}{-81\,u^2 + 1}
= \frac{1}{9}\,\text{arctanh}(9\,u) + c_{3,1}
= \frac{1}{9}\,\text{arctanh}\left(\frac{1}{\sqrt{4\,t^3 + 1}}\right) + c_{3,1}\,.

 $$ 

Finally, for the second integral

 $$ 

S_{3,2} \equiv \int \frac{2\,t^3 - 3\,t^2 - 1}{-6\,t\left(t^2 - t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

putting:

 $$ 

u = \frac{\alpha\,t^2 + \beta\,t + \gamma}{\sqrt{4\,t^3 + 1}}

 $$ 

then imposing:

 $$ 

\frac{\text{d}u}{m\,u^2 + n} = \frac{2\,t^3 - 3\,t^2 - 1}{-6\,t\left(t^2 - t + 1\right)}\,\frac{\text{d}t}{\sqrt{4\,t^3 + 1}}

 $$ 

ie:

 $$ 

\frac{\text{d}u}{\text{d}t}\,\frac{\frac{-6\,t\left(t^2-t+1\right)}{2\,t^3-3\,t^2-1}\,\sqrt{4\,t^3 + 1}}{m\,u^2 + n} = 1

 $$ 

the identification gives the values:

 $$ 

\alpha = 0\,, \quad
\beta = \frac{2}{3}\,, \quad
\gamma = -\frac{1}{3}\,, \quad
m = -9\,, \quad
n = 1

 $$ 

ie:

 $$ 

S_{3,2} 
= \int \frac{\text{d}u}{-9\,u^2 + 1}
= \frac{1}{3}\,\text{arctanh}(3\,u) + c_{3,2}
= \frac{1}{3}\,\text{arctanh}\left(\frac{2\,t - 1}{\sqrt{4\,t^3 + 1}}\right) + c_{3,2}\,.

 $$ 

we n conclusion, the searched primitive family is

 $$ 

S = S_1 + S_2 + S_{3,1} + S_{3,2}\,,

 $$ 

which is completely equivalent to that returned by Rubi and therefore evaluating it at the extremes returns what we wanted to prove.
An elementary alternative to avoid the determination of the primitive consists in the parametric method of derivation and integration under the sign of integral (also known as Richard Feynman's trick), but if it isn't possible to identify a winning strategy it's impractical, similar to the method here exposed.

