---
tags:
  - Affine-Geometry
  - Convex-Geometry
  - Convex-Optimization
  - Geometry
  - Definition
aliases:
  - extreme points
  - extreme point
  - vertex
---
## Definition

A point $x \in C \subseteq V$ in a [[Convex Set|convex set]] $C$ is an extreme point if it does not lie in the interior of any line segment in $C$. Equivalently, $x$ is an extreme point if 
$$
x = \lambda x_{1} + (1 - \lambda)x_{2}
$$
for $\lambda \in (0,1)$ implies that $x_{1} = x_{2} = x$. In other words, $x$ is extreme if it cannot be written as a non-trivial convex combination of points in $C$.