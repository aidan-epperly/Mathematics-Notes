---
tags:
  - Operator-Algebra
  - Algebra
  - Analysis
  - Fundamental-Objects
  - Definition
aliases:
  - Hilbert space
  - Hilbert spaces
  - inner product space
---
## Definition

A *pre-Hilbert space* $\mathcal{H}'$ is a real or complex [[Vector Space|vector space]] equipped with a Hermitian inner product 
$$
\langle \cdot,\cdot \rangle : \mathcal{H} \times \mathcal{H} \to \mathbb{K}
$$
that satisfies
1. $\langle x,y \rangle = \langle y,x \rangle^{*}$,
2. $\langle x,x \rangle \geq 0$ with $\langle x,x \rangle = 0$ if and only if $x = 0$,
3. $\langle x, y + \alpha z \rangle = \langle x,y \rangle + \alpha \langle x,z \rangle$.

The conditions above are sufficient for $\sqrt{ \langle x,x \rangle }$ to be a well-defined norm. A *Hilbert space* $\mathcal{H}$ is the completion of a pre-Hilbert space.