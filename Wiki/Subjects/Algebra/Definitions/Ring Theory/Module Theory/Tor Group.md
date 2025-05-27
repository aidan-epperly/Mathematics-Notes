---
tags:
  - Algebra
  - Module-Theory
  - Definition
aliases:
  - Tor
---
# Definition

Constructing the *Tor group* is an identical construction to that of the [[Ext Group|Ext group]], but $\_{} \otimes N$ takes the place of $\mathrm{Hom}(\_, N)$.

In particular, given an $R$-module $M$, pick a [[Projective Resolution|projective resolution]] 
$$
P \to M \to 0.
$$
Define 
$$
\mathrm{Tor}_{i}(M,N) = H_{i}(P \otimes N \to 0).
$$
By the [[Comparison Theorem]], the choice of resolution does not matter.