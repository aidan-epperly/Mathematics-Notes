---
tags:
  - Algebra
  - Module-Theory
  - Fundamental-Result
  - Result
aliases:
  - Ext is independent of resolution
---
# Results

## Ext is Independent of Resolution

In the definition of [[Ext Group|Ext]], the choice of projective resolution is arbitrary, which is to say that if $P,Q \to M$ are [[Projective Resolution|projective resolutions]], then 
$$
H_{i}(\mathrm{Hom}(P,N)) \cong H_{i}(\mathrm{Hom}(Q,N)).
$$

### Proof

Let $f': M\to M$ be the identity. Then by the [[Comparison Theorem]] we obtain a chain map $f : P \to Q$.  Similarly, taking $g' : M\to M$ identity, we get $g : Q \to P$ a chain map. Then $gf$ extends the identity map from $P\to P$.

Thus, there is a chain homotopy $s : P_{i} \to P_{i+1}$ with 
$$
gf - 1 = sd + ds.
$$
Applying $\mathrm{Hom}(\cdot,N)$ above we get 
$$
f^{*}g^{*} - 1 = s ^{*}d^{*} + d ^{*} s ^{*}.
$$
So $f^{*}g^{*}$ is chain homotopic to the identity and $f^{*}g^{*}$ and $1$ induce the same map on $H_{i}(\mathrm{Hom}(P,N))$.

So $f^{*}$ is an isomorphism between $H_{i}(\mathrm{Hom}(P,N))$ and $H_{i}(\mathrm{Hom}(Q,N))$.

## Zeroth [[Ext Group]] is $\mathrm{Hom}(M,N)$

The zeroth [[Ext Group|Ext group]] $\mathrm{Ext}^{0}(M,N)$ is equal to  $\mathrm{Hom}(M,N)$.

### Proof

This is a corollary of [[Properties of Hom Functor|Hom is left exact]].