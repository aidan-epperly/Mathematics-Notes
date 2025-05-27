---
tags:
  - Algebra
  - Group-Theory
  - Fundamental-Result
---
## Result

Given a finite [[Group|group]] $G$ and $H \subseteq G$ a subgroup, then $|H|$ divides $|G|$.

### Proof

Consider the left [[Group Action|action]] of $H$ on $G$ by multiplication. Note that if $h \in H$ and $g \in G$ then if $hg = g$, then $h = 1$. So, $H_{g} = \left\{ 1 \right\}$ for all $g \in G$. Thus, each [[Group Orbit|orbit]] of $g \in G$ has order $H$ by [[Orbit Stabilizer Theorem|orbit stabilizer]]. Since the [[Group Orbit|orbits]] define an equivalence relation on $G$, we must have that $|H|$ divides $|G|$.