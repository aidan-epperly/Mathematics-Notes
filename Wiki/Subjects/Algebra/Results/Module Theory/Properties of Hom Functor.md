---
tags:
  - Result
  - Algebra
  - Module-Theory
aliases:
  - Hom is a contravariant functor
  - Hom is additive
  - Hom is left exact
---
# Results

Let $M$ and $N$ be $R$-modules.

## Hom is a Contravariant Functor

The map $\mathrm{Hom}(\cdot, N)$ mapping an $R$-module $M$ to $\mathrm{Hom}(M,N)$ is a contravariant functor. Thus, given $f \in \mathrm{Hom}(A,B)$, the map 
$$
f^{*} = \mathrm{Hom}(\cdot,N)(f): \mathrm{Hom}(B,N) \to \mathrm{Hom}(A,N).
$$

## Hom is Additive

Given an $R$-module $N$, the functor $\mathrm{Hom}(\cdot,N)$ is additive as in 
$$
(f + g)^{*} = f^{*} + g^{*}.
$$
## Hom is Left Exact

The functor $\mathrm{Hom}(\cdot,N)$ is left exact.

### Proof

Suppose $0 \to A \overset{f}{\to} B \overset{g}{\to} C \to 0$ is exact and apply $\mathrm{Hom}(\cdot,N)$. 

#### Claim 1

The map $g^{*} : \mathrm{Hom}(C,N) \to \mathrm{Hom}(B,N)$ is injective. Suppose $\varphi \in \mathrm{Hom}(C,N)$ with $g^{*}\varphi = 0$ or equivalently $\varphi(g(b)) = 0$ for all $b \in B$. The map $g$ is surjective, so $\varphi(c) = 0$ for all $c$ in $C$ and thus $\varphi = 0$.

#### Claim 2

The map $f^{*}: \mathrm{Hom}(B,N) \to \mathrm{Hom}(A,N)$ is surjective. Suppose $\psi \in \mathrm{Hom}(B,N)$. We know that $\psi |_{\mathrm{ker}\,g} = 0$. Thus, by the first isomorphism theorem $\psi = \varphi \circ g$ for some $\varphi$.
