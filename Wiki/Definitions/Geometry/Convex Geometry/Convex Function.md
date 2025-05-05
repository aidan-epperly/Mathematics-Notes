---
tags:
  - Convex-Geometry
  - Convex-Optimization
  - Definition
  - Fundamental-Objects
aliases:
  - convex function
---
## Definition

A function $f : C \to \mathbb{R}$ is *convex* if for all $x,y \in C$ a [[Convex Set|convex set]] we have
$$
f(\lambda x + (1-\lambda)y) \leq \lambda f(x) + (1- \lambda) f(y)
$$
with $\lambda \in [0,1]$.