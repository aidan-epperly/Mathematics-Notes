---
tags:
  - Operator-Algebra
  - Algebra
  - Analysis
  - "#Fundamental-Objects"
  - "#Definition"
aliases:
  - bounded operators
  - bounded operator
  - bounded operators on a Hilbert space
  - bounded operator on a Hilbert space
---
## Definition

Given [[Wiki/Definitions/Algebra/Operator Algebra/Hilbert Space|Hilbert spaces]] $\mathcal{H}_{1}$ and $\mathcal{H}_{2}$, a linear operator $T : \mathcal{H}_{1} \to \mathcal{H}_{2}$ is called *bounded* if 
$$
\lvert\lvert T \rvert\rvert = \mathrm{sup}_{\lvert\lvert x \rvert\rvert \leq 1} \lvert\lvert Tx \rvert\rvert < \infty.
$$
We denote by $\mathcal{B}(\mathcal{H}_{1},\mathcal{H}_{2})$ the space of all such bounded operators. If $\mathcal{H} = \mathcal{H}_{1} = \mathcal{H}_{2}$, we shorten this to $\mathcal{B}(\mathcal{H})$. Note that the above is the uniform norm. The space $\mathcal{B}(\mathcal{H})$ is a Banach algebra under composition and the norm above. In particular, the norm is submultiplicative.

### Bounded Equals Continuous

It is not hard to show that an operator is continuous if and only if it is bounded. Thus, the bounded operators are exactly those that are continuous.