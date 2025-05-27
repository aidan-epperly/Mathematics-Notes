---
tags:
  - Quantum
  - Free-Convex-Geometry
  - Quantum-Information-Theory
  - Definition
aliases:
  - TPCP
  - CPTP
---
## Definition

Let $\mathcal{A}$ and $\mathcal{B}$ be [[von Neumann Algebra|von Neumann algebras]]. A linear map 
$$
\mathcal{E} : \mathcal{A} ^{\triangle} \to \mathcal{B} ^{\triangle}
$$
is *trace preserving and completely positive* if it is [[Trace Preserving Maps|trace preserving]] and [[Completely Positive Map|completely positive]].

## Kraus Representation Theorem

Suppose $\mathcal{E} : \mathcal{B}(\mathcal{H}_{1})^{\triangle} \to \mathcal{B}(\mathcal{H}_{2})^{\triangle}$ is TPCP. Then there are operators $V_{k} : \mathcal{B}(\mathcal{H}_{1}) \to \mathcal{B}(\mathcal{H}_{2})$ such that 
$$
\mathcal{E} (\rho) = \sum_{k} V_{k}\rho V_{k}^{\dagger}, \quad  \sum_{k} V_{k}^{\dagger}V_{k}  = I.
$$
These $V_{k}$ are called a Kraus representation of $\mathcal{E}$.

### Connection to [[Free Semialgebraic Geometry]]

While there are many good reasons to accept TPCPs as quantum maps, the Kraus representation is particularly compelling. Classical maps in probability are stochastic, meaning that they act on vectors by taking entrywise convex combinations. The Kraus representation does exactly this, but instead of using classical [[Convex Combination|convex combinations]] we use [[Free Convex Combination|free convex combinations]].