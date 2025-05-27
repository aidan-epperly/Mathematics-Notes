---
tags:
  - Algebra
  - Module-Theory
  - Result
  - Fundamental-Result
---
# Results

## Every Module has a Free Resolution

Let $M$ be an $R$-module. Then $M$ has a [[Free Resolution|free resolution]].
### Lemma

If $M$ is an $R$-module, then there is a surjective map $F \to M$ for some [[Free Module|free module]] $F$. If $M$ is finitely generated, then $F$ can be chosen to have finite index.

### Proof
 Let $I = M$ (or $G$ the generating set of $M$) and consider $F_{0} = \bigoplus_{i \in I} R_{i}$. Clearly there is a surjection $d_{0}$ from $F_{0}$ to $M$. So 
$$
F_{0} \to M \to 0
$$
is [[Exact Sequence|exact]]. Now let $N_{0} = \mathrm{ker}\, d_{0}$. This is an $R$-module. Now repeat the proof above for $N_{0}$ to get $N_{1}$ and proceed by induction.