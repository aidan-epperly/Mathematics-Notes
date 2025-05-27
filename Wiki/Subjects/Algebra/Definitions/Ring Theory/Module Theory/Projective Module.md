---
tags:
  - Algebra
  - Module-Theory
  - Fundamental-Objects
  - Definition
aliases:
  - projective
  - projective module
---
## Definition

An $R$-module $P$ is projective if 
```tikz
\usepackage{tikz-cd}
\usepackage{array}
\begin{document}
\begin{tikzcd}
& P \arrow[ld,dashed,"g"] \arrow[d,"f"] \\
M \arrow[r,"r"] & N \arrow[r, "0"] & 0
\end{tikzcd}
\end{document}
```
holds for $M\to N\to 0$ exact.