---
title: Continuity and Commonly Defined Spaces
author: Colton Grainger (MATH 6210 Topology)
date: 2018-09-16
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

\setcounter{section}{1}

## Assignment due 2018-09-24

### Continuity by nested closures

\newcommand{\Cl}[1]{\overline{#1}}

Let $(X,\sT)$ and $(Y,\sW)$ be topological spaces. Consider a function $f \colon X \to Y$. The following are equivalent.

(a) $f$ is continuous.
(b) $f(\Cl{A}) \subset \Cl{f(A)}$ for all sets $A\subset X$ in domain.
(c) $\Cl{f^{-1}(B)} \subset f^{-1}\left(\Cl{B}\right)$ for all sets $B \subset Y$ in the codomain.

### Continuity by nested interiors

Consider the same spaces $(X,\sT)$ and $(Y,\sW)$ again with a function $f \colon X \to Y$. The following are also equivalent.

\newcommand{\Int}[1]{\left(#1\right)^\circ}

(a) $f$ is continuous.
(b) $f^{-1}(\Int{B}) \subset \Int{f^{-1}(B)}$ for all sets $B\subset Y$ in the codomain.

### Homeomorphic subspaces of the real line [@Mu00, number 18.5]

- The subspace $(a,b)$ of $\RR$ is homeomorphic with $(0,1)$.
- Also, the subspace $[a,b]$ (of $\RR$) is homeomorphic with $[0,1]$.

### Continuous at a single point [@Mu00, number 18.6]

The function $f \colon \RR \to \RR$ defined by 
$$f(x) = 
\begin{cases}
x^2 & \text{ if } x \in \QQ,\\
-x^2 & \text{ else}
\end{cases}$$
is continuous at a single point in the domain, namely $0$.

### Left and right continuity [@Mu00, number 18.7]

(a) Suppose that $f \colon \RR \to \RR$ is right continuous at each point $a \in \RR$. Then $f$ is continuous when consider as a function from $\RR_\ell$ to $\RR$.
(b) We exhaustively list the functions 

  - which are continuous from $\RR$ to $\RR_\ell$, also 
  - which are continuous from $\RR_\ell$ to itself.

### Maps into the order topology [@Mu00, number 18.8]

Let $Y$ be an ordered set in the order topology. Let $f,g \colon X \to Y$ be continuous maps. 

(a) The set $\{x : f(x) \le g(x)\}$ is closed in $X$.
(b) The function $h\colon X \to Y$ defined by $h(x) = \min\{f(x),g(x)\}$ is continuous.

### Maps out of the product topology [@Mu00, number 18.12]

Let $F \colon \RR \times \RR$ be defined by 
$$F(x\times y) = \begin{cases}
\frac{xy}{x^2 + y^2} & \text{ if } x \times y \neq 0 \times 0,\\
0 & \text{ else.}
\end{cases}$$

(a) $F$ is continuous in each variable separately.
(b) We compute the restriction $g \colon \RR \to \RR$ defined by $g(x) = F(x \times x)$.
(c) $F$ is not continuous.

### Projections and quotient maps [@Mu00, number 22.3]

Let $\pi_1 \colon \RR \times \RR \to \RR$ be the projection on the first coordinate, and consider the subspace $A = \{x\times y : x \ge 0 \text{ or } y = 0 \}$. The restriction $q\colon A \to \RR$ obtained by $q = \pi_1|_A$ is a quotient map that is neither open nor closed.

### Equivalence relations and quotient spaces [@Mu00, number 22.4]

(a) Define an equivalence relation $\sim$ on the plane $\RR^2$ by $$x_0 \times y_0 \sim x_1 \times y_1 \text{ iff } x_0 + y_0^2  = x_1 + y_1^2.$$

    We describe a space homoemorphic to the equivalence relation's corresponding quotient space $\RR^2/\sim$.

(b) Now redefine the previous equivalence relation $\sim$ (again on the plane) by $$x_0 \times y_0 \sim x_1 \times y_1 \text{ iff } x_0^2 + y_0^2  = x_1^2  + y_1^2.$$

    There's again a familiar space homoemorphic to the equivalence relation's quotient space $\RR^2/\sim$.

### Restricting to open maps [@Mu00, number 22.5]

Suppose that $p \colon X \to Y$ is an open map. If $A$ is open in $X$, then the map $q \colon A \to p(A)$ obtained by restricting $p$ is an open map.

### Quotienting out $K$ in the $K$-topology [@Mu00, number 22.6]

Let $Y$ be the quotient space obtained from $\RR_K$ by collapsing the set $K$ to point, with $p \colon \RR_K \to Y$ as the corresponding quotient map.

(a) $Y$ is $T_1$ but not Hausdorff.
(b) The map $p \times p \colon \RR_K \times\RR_K \to Y \times Y$ is not a quotient map.^[The diagonal is not closed in $Y \times Y$, but its inverse image is closed in $\RR_K \times \RR_K$.]

## References
