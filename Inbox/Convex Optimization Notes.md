## Cutting Plane Methods

Suppose we want to minimize a convex function $f$ over a convex set $\mathcal{X}$. We will suppose that $\mathcal{X}$ is compact and that there are inner and outer balls of radius $r,R$ resp. Suppose we have access to a *separation oracle* that given $y \notin \mathcal{X}$ produces a separating hyperplane between $\mathcal{X}$ and $y$.

## Subgradient Methods

### Centroid Method
1. Compute the centroid $x_{t}$ of $\mathcal{X_{t}}$.
2. Compute a hyperplane $H_{t}$ via the subgradient of $f$ at $x_{t}$.
3. Take $\mathcal{X}_{t + 1}$ to be 
$$
\mathcal{X} _{t+1} = H_{-}\cap \mathcal{X} _{t}.
$$

#Theorem The centroid method satisfies 
$$
f(x_{t})-\min f(x) \leq 2B \left( 1 - \frac{1}{e} \right)^{t/n}.
$$
*Proof:* Grunbaum's lemma.

### Ellipsoid Method
