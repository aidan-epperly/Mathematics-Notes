## Model Problem

We aim to show that the problem 
$$
\begin{align}
\min \langle C, X \rangle \quad \text{subject to } \quad  \mathrm{\mathcal{A} X = b}, \quad  X \in  \alpha \Delta_{n}.
\end{align}
$$
Where $\alpha \Delta_{n}$ is the set of all trace constrained positive semidefinite matrices.

If $X_{*}$ is the true optimal value of the problem above, we call a matrix $X_{\epsilon}$ satisfying
$$
\lvert\lvert X_{\epsilon} \rvert\rvert \leq \epsilon \quad  \text{and} \quad \langle C, X_{\epsilon} \rangle - \langle C, X_{*} \rangle \leq \epsilon.
$$
*Should this be an absolute value? -Aidan*
This is really all we can ever hope to solve in finite time.

### Low-Rank Solutions

We further relax our desired solution in the following way. In order to store the variable $X$, we generically need $\mathcal{O}(n^2)$ space which is sometimes intractable. Thus, instead we seek a low rank approximation $\hat{X}$ of rank $r$ such that
$$
\lvert\lvert X_{\epsilon} - \hat{X} \rvert\rvert \leq (1 + \zeta) \lvert\lvert X_{\epsilon} - [[X_{\epsilon}]]_{r} \rvert\rvert 
$$
where the latter term is the best low-rank approximation. This low-rank algorithm will be informed by the full-rank algorithm described below.
## CGAL

We can augment the model problem by "adding zero" to the objective function
$$
\min \langle C, X \rangle + \frac{\beta}{2} \lvert\lvert \mathcal{A} X - b \rvert\rvert^2  \quad \text{subject to } \quad  \mathrm{\mathcal{A} X = b}, \quad  X \in  \alpha \Delta_{n}.
$$
Since the term we have added to the objective function is $0$ for all feasible points, the optimal value does not change. However, this does augment the Lagrangian in an interesting way. The Lagrangian is
$$
\mathcal{L}_{\beta}(X,y) = \langle C,X \rangle  + \langle y, \mathcal{A}  X - b \rangle + \frac{\beta}{2} \lvert\lvert \mathcal{A} X - b \rvert\rvert ^{2}
$$
for $X \in \alpha \Delta_n$ and $y \in \mathbb{R}^{d}$.

### Oracles

1. The map $u \mapsto Cu$,
2. The map $(u,z) \mapsto (\mathcal{A}^{*}z)(u)$ where $\mathcal{A}^{*}(z)$ is the linear matrix polynomial form,
3. The map $u \mapsto \mathcal{A}(uu^*)$.
### Ideal Algorithm

An ideal algorithm to solve this augmented Lagrangian would be as follows:
1. Choose $X_{1} \in \alpha \Delta_{n}$ and $y_{1} \in \mathbb{R}^{d}$.
2. $X_{t + 1} = \mathrm{argmin}[\mathcal{L}_{\beta}(X, y_{t}) \; \mid \; X \in \alpha \Delta_{n}]$.
3. $y_{t+1} = y_{t} + \beta(\mathcal{A}X -b)$.

In order to penalize violation of the linear constraints, we can increase the value of $\beta$ every iteration. Unfortunately, in practice, the primal step is intractable.

### CGAL Iteration

Initialize the problem:
1. Pick $\beta_{0} > 0$ an initial smoothing parameter,
2. Pick a (large) $K > 0$ to bound the maximum size of the dual variable.
3. Pick some arbitrary $X_{1}$ symmetric (we don't even enforce positivity), *This seems to be a typo? Looks like they assume X is positive and trace alpha. -Aidan*
4. Set the $y_{1} = 0$.

Primal Step:
1. Set $\beta_{t} = \sqrt{ t + 1 }\beta_{0}$,
2. Compute 
$$
D_{t} = \partial_{X} \mathcal{L} _{\beta_{t}}(X_{t},y_{t}) = C + \mathcal{A} ^{*}(y_{t} + \beta_{t}(\mathcal{A} X_{t} - b)).
$$
3. Compute an update $H_{t} \in \alpha \Delta_{n}$ by solving
$$
H_{t} = \mathrm{argmin} [\langle D_{t}, H \rangle \; \mid \; H \in  \alpha \Delta_{n}],
$$
which is satisfied exactly when $H_{t} = \alpha v_{t}v_{t}^{*}$ for $v_{t}$ a minimum eigenvector of $D_{t}$. In practice, we will use an approximate minimal eigenvector computation described later.
4. Update the primal $X_{t + 1} = (1-\eta_{t})X_{t} + \eta_{t}H_{t}$ where $\eta_{t} = \frac{2}{t + 1}$.

Dual Step:
1. Pick $\gamma_{t}$ to be the largest such that
$$
\gamma_{t} \lvert\lvert \mathcal{A} X_{t+1} - b \rvert\rvert ^{2} \leq \frac{4\alpha^{2} \beta_{0}}{(t + 1)^{3/2}}\lvert\lvert \mathcal{A}  \rvert\rvert ^{2} \quad \text{and} \quad  0 \leq \gamma_{t} \leq \beta_{0}.
$$
2. Update 
$$
y_{t+1} = y_{t} + \gamma_{t}(\mathcal{A} X_{t+1} - b),
$$
omitting this step if $\lvert\lvert y_{t+1} \rvert\rvert > K$.

## Randomized Lanczos for Minimum Eigenvector Computation

We aim to find the minimum eigenvector of the matrix
$$
D_{t} = C + \mathcal{A} ^{*}(w_{t}).
$$
Using only our oracles, we can implement a Krylov subspace method, but traditional methods for this will perform poorly. Instead, we use the following method.

### Randomized Lanczos Method

![[Pasted image 20250505134426.png]]
## Sketchy CGAL - An Syzygy of Mathematical Nonsense Actually Working

Note that in our iteration, the only thing we actually need from $X$ is the vector $\mathcal{A}X - b$. If we let $z_{t} = \mathcal{A}X_{t} - b$, then the eigenvalue computation only depends on $z_{t}$ and the update steps become
$$
z_{t} \gets (1 - \eta) z_{t} + \eta \mathcal{A} ^{*}(\alpha vv^{*}), \; y_{t} \gets y_{t} + \gamma(z_{t} - b).
$$
All we have to do now is track the rank-one updates.