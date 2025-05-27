---
tags:
  - Definition
  - Algebra
  - Group-Theory
  - Fundamental-Objects
aliases:
  - group
---
## Definition

A *group* $(G, \cdot)$ is a set $G$ equipped with an [[Associative Map|associative]] map $\cdot: G \times G \to G$ such that there is some element $1 \in G$ such that $$
1 \cdot g = g\cdot 1,
$$and if $g \in G$ then there is an element $h \in G$ such that 
$$
g\cdot h = h\cdot g = 1.
$$

### Uniqueness of the Inverse

By the [[Uniqueness of Group Inverses]], a given element $g$ has exactly one inverse element. Therefore, we may denote the inverse $g^{-1}$ without loss of specificity.
## Group Homomorphisms

A *group homomorphism* is a map $\varphi : G \to H$ groups such that 
$$
\varphi(g h) = \varphi (g) \varphi(h).
$$
### Properties of Group Homomorphisms

By the [[Properties of Group Homomorphisms]], the following results hold.
1. Group homomorphisms map the identity to the identity.
2. Group homomorphisms commute with the inverse operation.