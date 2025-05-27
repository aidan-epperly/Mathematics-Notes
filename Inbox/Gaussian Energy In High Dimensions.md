How symmetrical should we expect the solution of an optimization problem to be?

Toy example: a Steiner tree connecting the vertices of a square. What is the minimal-length connecting path?

Each solution preserves *some* symmetries of the original sets and breaks others.

Which optimization problems have remarkably symmetrical answer? How can we understand why? (Error correcting codes are sometimes highly symmetric and sometimes quite random)

## Problem

Given a collection of particles interacting according to some potential function, what do they do? The simplest question is: what is the ground state? This comes up in real physical systems all of the time.

How to these particles arrange themselves under a repulsive force? You can easily guess the answers in one and two dimensions, but proving this is actually really difficult (there is no proof except in $8$ and $24$) dimensions. 

We assume that these particles are classical and we have some potential function $p$. The energy of a particle $x \in C$ is 
$$
E_{p,x}(C) = \sum_{y \neq x} p(\lvert\lvert y - x \rvert\rvert ).
$$

$C$ in $\mathbb{R}^{d}$ of density $\delta$ is a ground state if no other configuration has lower energy under potential $p$. Sometimes the ground state is a periodic lattice and sometimes it is not.

## Universal Optimality

When is a ground state independent of the potential function? Which potential functions are reasonable to consider. A function $p$ is completely monotonic if it is $C^{\infty}$ and $(-1)^{k}p^{(k)}\geq 0$. The Gaussians generate this as a cone.

A configuration $C$ is universally optimal if it is optimal for all Gaussian potentials.

Theorem: $\mathbb{Z}$ is universally optimal in $\mathbb{R}$.

Theorem: In $\mathbb{R}^{8}$ and $\mathbb{R}^{24}$ the $E_{8}$ root lattice and the Leech lattice are universally optimal.

