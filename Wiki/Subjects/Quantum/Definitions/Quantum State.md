---
tags:
  - Quantum
  - Quantum-Information-Theory
  - Operator-Algebra
  - Definition
aliases:
  - state
  - states
---
## Definition

Given a [[Unital|unital]] [[von Neumann Algebra]] $\mathcal{M}$, the *state region* $\mathcal{M}^{\triangle} \subseteq \mathcal{M}^{\#}$ is the [[Convex Set|convex set]] of all dual vectors $\rho$ with 
$$
\rho(1) = 1, \quad \rho(x^{\dagger}x) \geq 0.
$$

## Expectation

The *expectation* of an element $x \in \mathcal{M}$ with respect to the state $\rho$ is exactly $\rho(x)$.

### Examples
1. $\rho \in L^{1}[0,1]$ is a state if and only if $\lvert\lvert \rho \rvert\rvert_{1} = 1$. Then, the expectation of $x \in L^{\infty}[0,1]$ is exactly
$$
\int_{0}^{1} x \rho.
$$
which agrees with the classical expectation of a random variable.
2. If $\rho$ is a vector in a Hilbert space $\mathcal{H}$, then we call $\rho$ a *vector state* if $\lvert\lvert \rho \rvert\rvert_{2} = 1$. Then the expectation of the [[Observable|observable]] $H \in \mathcal{B}(\mathcal{H})$ is
$$
\bra{\rho} H \ket{\rho}.
$$