---
tags:
  - Quantum
  - Algorithm
  - Result
  - Fundamental-Result
aliases:
  - Shor's algorithm
  - period finding
---
# Result

Let $f : \mathbb{Z} \to X$ be a function in $\mathrm{P}$ which is periodic with unknown period $H$ (here capital letters are big numbers) and otherwise injective.

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\usepackage{array}
\begin{document}
\begin{tikzcd}
\mathbb Z \arrow[rr,"f"] \arrow[rd,two heads]& & X \\
& \mathbb Z / H \arrow[ur,hookrightarrow] &
\end{tikzcd}
\end{document}
```

If $H$ takes $n$ bits to store then we can find it in quantum polynomial time in $n$.

While this algorithm is widely known for being able to factor integers, this is only a special subcase of this algorithm.

## Factoring Integers

Say you want to factor $N \in \mathbb{Z}$ where $N$ is taken to be odd and not a prime power for convenience. Also for convenience, assume that 
$$
\varphi(N) := \lvert (\mathbb{Z} / N)^{\times} \rvert  > \frac{N}{2}.
$$
Choose a residue $r \in (\mathbb{Z} / N)^{\times}$ at random and let $f(x) = r^{x}$ in $\mathbb{Z} / N$. This fits the hypothesis and it is fast!

The period $H = \mathrm{or d}(r)$ provided by Shor's algorithm tells you a lot about $(\mathbb{Z} / N)^{\times}$ as a group, $\mathbb{Z}/N$ as a ring, and factors of $N$. For example, with probability at least $\frac{1}{2}$, $H$ is even and $s = r^{H/2}$ will be an exotic square root--not $\pm 1$. So, GCD gives a factor.

Shor--Kitaev works for 
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\usepackage{array}
\begin{document}
\begin{tikzcd}
\mathbb{Z}^k \arrow[rr, "f"] \arrow[rd, two heads]& & X \\
 & \mathbb{Z}^k / H \arrow[ur, hookrightarrow] & 
\end{tikzcd}
\end{document}
```
where $H$ is a hidden subgroup of $\mathbb{Z}^{k}$ or equivalently a $k$-dimensional sublattice. This is mainly used to compute the discrete log map of an obfuscated Abelian group.