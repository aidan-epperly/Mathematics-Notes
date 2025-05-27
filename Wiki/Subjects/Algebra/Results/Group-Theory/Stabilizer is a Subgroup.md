---
tags:
  - Algebra
  - Fundamental-Result
  - Result
aliases:
---
## Result

Let $(G,S,\cdot)$ be a [[Group Action|group action]] and $T_{s}$ the [[Stabilizer Subgroup|stabilizer]] of some element $s \in S$. Then $G_{s}$ is a subgroup of $G$.

### Proof

Note that $1 \in G_{s}$ as $1 \cdot s = s$. Now, suppose that $g,h \in G_{s}$. By associativity, we have 
$$
(gh) \cdot s = g \cdot (h\cdot s) = g\cdot s= s,
$$
so $gh \in G_{s}$. Moreover, 
$$
g^{-1}\cdot s = (g^{-1}g)\cdot s = 1 \cdot s = s,
$$
so $g^{-1} \in G_{s}$. Thus, $G_{s}$ is a subgroup of $G$.