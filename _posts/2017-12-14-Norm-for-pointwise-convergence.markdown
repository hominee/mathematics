---
layout: post
title: Norm for pointwise convergence
tag:
 - real-analysis
 - functional-analysis
 - banach-spaces

description: Norm for pointwise convergence

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Norm for pointwise convergence

<!–-break-–>


Does there exist a norm on the space of all real-valued functions on the real line (or on an open set? a compact set?) such that convergence in this norm is equivalent to pointwise convergence?
.


# Answer 


No. First note that if $$X$$ is any set, the space of all functions $$f: X \to \mathbb{R}$$ with the topology of pointwise convergence is simply the space $$\prod_{X} \mathbb{R}$$ with the product topology. It is well-known that this space is metrizable if and only if $$X$$ is at most countable, see e.g. J. Dugundji, Topology, IX.7.1, p.189. However, if $$X$$ is countably infinite, then it is an easy exercise to show that there is no norm inducing the topology of pointwise convergence (see e.g. Rudin, Functional analysis, Theorem 1.39, p.28, and also Exercise 7 on p.37).
To sum it all up, the space you're interested in is

(completely) normable if and only if $$X$$ is finite; 
(completely) metrizable if and only if $$X$$ is countable;
not even metrizable in all other situations.

we leave the fact that the norm and metric can be chosen to be complete as an exercise.

