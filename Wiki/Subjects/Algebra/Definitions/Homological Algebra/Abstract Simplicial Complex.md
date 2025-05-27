---
tags:
  - Algebra
  - Homology
  - Fundamental-Objects
  - Definition
aliases:
  - ASC
---
## Definition

An *abstract simplicial complex* $(S, K)$ is composed of a set $S$ together with a collection $K$ of finite, nonempty subsets 
$$
\sigma = \left\{ x_{0}, x_{1}, \dots, x_{n} \right\} \subseteq S
$$
such that if $\sigma \in K$ then all nonempty subsets $\sigma' \subseteq \sigma$ are also in $K$. When the ambient set $S$ is clear, we will simply denote the ASC by $K$. Let $K_{n}$ denote 

### Geometric Realization

The *geometric realization* of $K$, which we denote by $|K|$, is a simplicial complex 
$$
|K| = \left\{ (a_{1},\dots,a_{n}) \; \mid \; a_{i} \geq 0 ,\; \sum_{i}a_{i} = 1, \; (*) \right\}
$$
where $(*)$ is the extra condition that if $J = \left\{ i \; \mid \; a_{i} > 0 \right\}$ then $J \in K$.

### Ordering

Suppose that $(S, >)$ is a total ordering on $S$. 