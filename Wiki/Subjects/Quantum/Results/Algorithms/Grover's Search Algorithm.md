---
tags:
  - Quantum
  - Algorithm
  - Fundamental-Result
  - Result
aliases:
  - Grover search
---
## Result

Let $f : \mathbb{Z}_{2}^{n} \to \mathbb{Z}_{2}$ be a binary function (say in $\mathrm{P}$) with a single $x_{*} \in \mathbb{Z}_{2}^{n}$ such that $f(x) = 1$. Then, we can solve for $x_{*}$ in quantum time $\tilde{O}(2^{n/2})$ or in query complexity $O(2^{n/2})$. This attains optimal query complexity and beats the optimal classical complexity $O(2^{n})$.

If, instead, the search space is size $N$ and there are $K$ solutions, then this generalizes to 
$$
\Theta\left( \sqrt{ \frac{N}{K} } \right)
$$
queries to find one solution.

### Algorithm

1. Initialize $n$ qubits in the $\ket{x} =\ket{+}$ state;
2. For $i = 1, k$ do:
	1. $\ket{x} \gets (-1)^{f(x)}\ket{x}$;
	2. $\ket{x} \gets (1 - 2\ket{+}\bra{+})\ket{x}$;
3. Measure $\ket{x}$ in c.b.;