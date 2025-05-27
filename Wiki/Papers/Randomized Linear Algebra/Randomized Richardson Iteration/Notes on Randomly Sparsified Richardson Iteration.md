---
tags:
  - Algorithm
  - Numerical-Analysis
  - Paper-Notes
---
# Notes on the Talk

## Background

Monte Carlo methods can be pushed even further, but first their limitations need to be addressed.

## Extreme Eigenvalues Problems

Due to the combinatorial explosion arising from quantum physics, dense algorithms do not work.

## Classical Solvers

Classical iterative eigensolvers include power method, subspace iteration, Lanczos, Jacobi-Davidson. The simplest method is the power method which converges if the eigenvalues are sufficiently gapped.

We can apply the power method to the matrix $A = I - \epsilon H$ for small $\epsilon>0$ to find the ground state for small systems, but each iteration gives you a denser and denser vector.

## Full Configuration Interaction Quantum Monte Carlo

FCIQMC approximate $x_{t+1} = Ax_{t}$ in the sense that 
$$
\mathbb{E}[x_{t+1}] = Ax_{t}.
$$
This method is Markovian. We expect that these types of systems with converge to a stationary measure $\mu$. This has alluded proof.

## Fast Randomized Interaction

Introduce a random compression operator $\phi : \mathbb{R}^{d} \to \mathbb{R}^{d}$ such that $\phi(x)$ has at most $m$ nonzero entries and $\mathbb{E}[\phi(x)] = x$.