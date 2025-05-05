---
tags:
  - Convex-Geometry
  - Convex-Optimization
  - Result
aliases:
  - first-order convexity condition
---
## Result

Let $f : C \to \mathbb{R}$ be a [[Convex Function|convex function]] and let $A = \left\{ a(x) \; \mid \; f(x) \geq a(x) \; \forall f\in C \right\}$ be the set of all linear underestimators of $f$. Then 
$$
f(x) = \mathrm{sup}_{a}\, a(x).
$$

### Proof

Let $g(x) = \mathrm{sup}\,a(x)$. We immediately get
$$
g(x) \leq f(x),
$$
and thus it is sufficient to show that $f(x) \leq g(x)$.