---
tags:
  - Algebra
  - Group-Theory
  - Fact
---
## Result

Let $G,H$ be groups and $\varphi : G \to H$ a group homomorphism between them. The following hold:
1. $\varphi$ fixes the identity so that $\varphi(1) = 1$.
2. $\varphi$ commutes with the inverse operation. In particular,
$$
\varphi(g^{-1}) = \varphi(g)^{-1}.
$$

### Proof

1. Let $g \in G$. Then 
$$
\varphi(g) = \varphi(1g) = \varphi(1)\varphi(g).
$$
applying $\varphi(g)$ inverse to both sides yields $\varphi(1) = 1$.
2. Let $g \in G$. Then 
$$
\varphi(g^{-1})\varphi(g) = \varphi(g^{-1}g) =1 = \varphi(g g^{-1}) = \varphi(g) \varphi(g^{-1}).
$$
so, $\varphi(g^{-1}) = \varphi(g)^{-1}$.