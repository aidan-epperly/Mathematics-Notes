---
tags:
  - Algebra
  - Fundamental-Objects
  - Definition
aliases:
  - Ext
  - Ext group
---
# Definition

Suppose $M$ is an $R$-module with projective resolution $P \to M$. Given $N$ an $R$-module, let 
$$
\mathrm{Ext}^{i}(M,N) = H_{i}(\gets \mathrm{Hom}(P_{1},N) \gets \mathrm{Hom}(P_{0},N) \gets 0).
$$

# Examples

Let $R = \mathbb{Z}$, $M = \mathbb{Z} / n$, $N = A$ an [[Abelian Group]]. $M$ has resolution
$$
0 \to \mathbb{Z} \overset{n}{\to} \mathbb{Z} \to \mathbb{Z} / n \to 0.
$$
Then 
$$
\mathrm{Ext}^{i}_{\mathbb{Z}}(M,N) = H_{i}(0 \gets A \overset{n}{\gets} A \gets 0),
$$
so $\mathrm{Ext}^{0}(\mathbb{Z}/n, A) = \left\{ a \; \mid \; na = 0 \right\}$, 
$$
\mathrm{Ext}^{1}(\mathbb{Z} / n, A) = A/ nA,
$$
and $\mathrm{Ext}^{i}(\mathbb{Z} / n, A)$ for $i \geq 2$ is zero.

In general, if $M, N$ are [[Abelian Group|Abelian]], then 
$$
\mathrm{Ext}^{i}_{\mathbb{Z}}(M, N) = 0 \; \forall i > 1.
$$