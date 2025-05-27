---
tags:
  - Group-Theory
  - Algebra
  - Definition
  - Fundamental-Objects
aliases:
  - group action
  - action
  - acts
---
## Definition

Given a [[Group|group]] $G$ and a set $S$, a *[[Group]] action* of $G$ on $S$ is a map 
$$
\cdot : G \times S \to S
$$
such that for all $g,h\in G$ and $s \in S$, we have 
$$
\begin{align}
1 \cdot s &= s  \\
(gh)\cdot s &= g \cdot (h\cdot s).
\end{align}
$$
If $(G,S,\cdot)$ is a [[Group]] action, we sometimes say that $G$ *acts on* $S$.

### Transitive Actions

A [[Group]] action $(G,S,\cdot)$ is called *transitive* if there is only one unique [[Group Orbit|orbit]].

## Examples

1. If $G$ is a [[Group|group]], then $G$ acts on itself in three natural ways
	1. $(G,G,\cdot)$ with $g \cdot h = gh$,
	2. $(G,G,\cdot)$ with $g\cdot h = hg^{-1}$,
	3. $(G,G,\cdot)$ with $g \cdot h = ghg^{-1}$.
2. If $H \subseteq G$ is a subgroup of $G$, then $H$ acts on $G$ in the same ways as above.