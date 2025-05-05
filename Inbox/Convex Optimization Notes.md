#Theorem (Jensen's Inequality) If $f$ is convex, then 
$$
f(\mathbb{E}z) \leq \mathbb{E}f(z)
$$
for any random variable $z$.

*Proof:* That $f$ is convex is equivalent to 
$$
f(z)= \mathrm{sup}\, a(z)
$$
where $A = \left\{ a(z) \right\}$ is the set of all linear functions that underestimate $f$. Note that 
$$
\mathbb{E}f(z) \geq \mathbb{E}a(z) = a(\mathbb{E}z).
$$
Taking the supremum we get the result.

