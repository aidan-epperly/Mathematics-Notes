---
tags:
  - Algebra
  - Fundamental-Result
  - Result
aliases:
  - orbit stabilizer
---
## Result

Let $(G,S,\cdot)$ be a [[Group Action|group action]]. Then there is a one-to-one correspondence between the left [[Group Coset|cosets]] of the [[Stabilizer Subgroup|stabilizer]] $G_{s}$ and the elements of the orbit $\mathcal{O}_{s}$. 

### Proof

Let $G_{s}$ be the [[Stabilizer Subgroup|stabilizer]] subgroup of $s$ and $\mathcal{O}_{s}$ the [[Group Orbit|orbit]]. Consider the map 
$$
f : G \to S
$$
taking $g \in G$ to $g\cdot s$. Let $t = g\cdot s \in S$ and consider the fiber $f^{-1}(t)$. This would be exactly the set of all $h \in G$ such that 
$$
h \cdot s = g \cdot s \iff g^{-1} \cdot (h \cdot s) = s.
$$
This is exactly the statement that $g^{-1}h \in G_{s}$ or $h \in gG_{s}$. Thus, $f$ induces a bijection between the cosets of $G_{s}$ and the elements $g \cdot s \in \mathcal{O}_{s}$.

## Corollary

If $G$ and $S$ are finite, then $|\mathcal{O}_{s}|$ is equal to the number of left [[Group Coset|cosets]] of $G_{s}$.