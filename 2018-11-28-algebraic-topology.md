---
title: Intro to Algebraic Topology
author: Colton Grainger (Topology MATH 6210)
date: 2018-11-28
bibliography: /home/colton/coltongrainger.bib
macros: true
---

\setcounter{section}{6}

## Assignment due 2018-11-30

### [@Mun00, number 53.4]

\gvn Let $q \colon X \to Y$ and $r \colon Y \to Z$ be covering maps. Let $p = r \circ q$. Suppose $r^{-1}(z)$ is finite for each $z \in Z$. 

\wts $p$ is a covering map.

\pf Let $z \in Z$ and $r^{-1}(z) = \{y_i\}_{i=1}^n$. There's a neighborhood of $z$ evenly covered by (a finite collection) $\{U_i\}$, each open in $Y$ and indexed by $y_i \in U_i$. 

For each $i \in \{1, \ldots, n\}$ there's a neighborhood $O_i$ of $y_i$ such that $O_i \cap U_i$ can be evenly covered by (an arbitrary collection) $\{V_{\alpha_i}\}$ indexed by $x_{\alpha_i} \in V_{\alpha_i}$ where $q^{-1}(y_i) = \{x_{\alpha_i}\}$. Since $r$ is an open map, $\cap_{i=1}^n r(O_i \cap U_i)$ is a neighborhood of $z$. 

Because $q$ and $r$ are both single valued,
$$p^{-1}(z)= \sqcup_{i=1}^n\sqcup_{\alpha_i} x_{\alpha_i}.$$

I claim $z$ is evenly covered under $p = r \circ q$ by 
$$\sqcup_{i=1}^n\sqcup_{\alpha_i} V_{\alpha_i},$$
observing that 

- $V_{\alpha_i}$ is homeomorphic by a restriction of $q$ to $O_i \cap U_i$ that is homeomorphic to $r(O_i \cap U_i)$ containing $z$.
- The $V_{\alpha_i}$ are disjoint because both 
    - for each $i$, $V_{\alpha_i} \cap V_{\beta_i} = \emptyset$ for all indices $\alpha_i \neq \beta_i$ 
    - for each $i \neq j$, if $V_{\beta_i}$ met $V_{\beta_j}$ nontrivially, then $q\mid_{V_{\beta_i} \cap V_{\beta_j}}$ would be multivalued, which is absurd.

We've shown that $p = r \circ q$ is a covering map $p \colon X \to Z$. \qedsymbol


### [@Mun00, number 53.6]

\gvn Let $p \colon E \to B$ be a covering map.

\wts 
- If $B$ is Hausdorff,
- If $B$ is regular, then so is $E$.
- If $B$ is completely regular, then so is $E$.
- If $B$ is locally compact Hausdorff, then so is $E$.
- If $B$ is compact and $p^{-1}(b)$ is finite for each $b \in B$, then $E$ is compact.

\pf We state the hypothesized topological property assumed for the base space $B$, and prove that it holds for the total space $E$.

**Fréchet separation ($T_1$).** Suppose singletons are closed in $B$. For any $x \in E$, $\{p(x)\}$ is closed in $B$. There's a neighborhood $U_{p(x)}$ of $p(x)$ with pullback $p^{-1}(U)$ that's partitioned into slices $V_\alpha$. Check $x \in p^{-1}(x) \cap V_{\alpha'}$ for a unique index $\alpha'$. Since $\{p(x)\}$ is closed in $B$, $\{x\} = p^{-1}(x) \cap V_{\alpha'}$ is closed in $E$.

**Hausdorff separation ($T_2$).** Say $x \neq y$ in $E$. If $p(x) = p(y)$, there's a neighborhood $U$ of $p(x)$ such that $p^{-1}(U)$ is the disjoint union of slices $V_\alpha$ and $x \in V_\beta$ and $y \in V_\gamma$ is a (unique) separation of $x$ and $y$ into disjoint open sets. Else if $p(x) \neq p(y)$, then because $B$ is Hausdorff, there exist disjoint neighborhoods $U_{p(x)}$ and $U_{p(y)}$. Because $B$ is the base of a total cover, there also exist neighborhoods $O_{p(x)}$ and $O_{p(y)}$ with slices $\{V_{\alpha_x}\}$ and $\{V_{\alpha_y}\}$. We obtain a separation of $x$ and $y$ in $E$ with
$$x \in p^{-1}(U_{p(x)} \cap (\sqcup V_{\alpha_x}) \quad \text{ and } \quad y \in  p^{-1}(U_{p(y)} \cap (\sqcup V_{\alpha_y}).$$

**Lemma.** Suppose $b \in B$ and $U$ is a neighborhood of $b$ such that $\{V_\alpha\}$ is a partition of $p^{-1}(U)$ into slices. Let $C$ be a closed set of $B$ such that $C \subset U$. Then $p^{-1}(C)$ is closed. Moreover, $p^{-1}(C) \cap V_\alpha$ contains its limit points, and is closed as well.

**Regular separation ($T_3$).** Let $w \in E$ and $W$ a neighborhood of $w$. Then $p(w) \in p(W)$ is open in $B$. There's a neighborhood $O$ of $p(w)$ evenly covered by $p$. Let $U = p(W) \cap O$. Since $B$ is regular, there's a neighborhood $A$ of $p(w)$ such that 
$$p(w) \in \mathrm{Cl}(A) \subset U.$$

Say $p^{-1}(U)$ has slices $\{V_\alpha\}$. Then $w \in V_{\alpha'} \cap p^{-1}(A) \subset V_{\alpha'} \cap p^{-1}(\mathrm{Cl}(A)) \subset V_{\alpha'}$, by the lemma. We conclude $E$ is regular.

**Completely regular separation ($T_{3\frac12}$).** Let $K \subset E$ be closed and take $x \in E \setminus K$. Then $p(E\setminus K)$ is open in $B$, with obviously $p(x) \in p(E \setminus K)$. There's a neighborhood $U$ of $p(x)$ contained in $p(E\setminus K)$ (intersecting two open sets if necessary to construct $U$) such that $p^{-1}(U)$ is partitioned into slices $\{V_\alpha\}$. Now $B \setminus U$ is closed and disjoint from $p(x)$. Because $B$ is completely regular, there exists a map $f \colon B \to I$ such that $f(B \setminus U) = \{0\}$ and $f(p(x)) = 1$. Since $p\mid_{V_{\alpha'}}$ is a homeomorphism onto $U$ from the unique $V_{\alpha'}$ containing $x$, we may define a map $g \colon E \to I$ as follows:
$$ g(z) = \begin{cases} 0 & \text{ if } z \in E\setminus V_{\alpha'}\\
\left(f \circ p\mid_{V_{\alpha'}}\right)(z) & \text{ if } z \in V_{\alpha'}.\end{cases}$$

I claim $g$ can be defined as two piecewise continuous maps (verify) that evaluate to $0$ on the closed set $\partial V_{\alpha'}$. By the piecing lemma for maps, $g$ is continuous on $E$. As desired, $g(x) = 1$. Moreover, because $$V_{\alpha'} \subset p^{-1}(U) \subset E \setminus K \quad \text{ and } \quad U \subset p(E \setminus K),$$ we have $K \subset E \setminus V_{\alpha'}$. Thus $g(K) = \{0\}$. So $E$ is completely regular.

**Locally compact Hausdorff.** Suppose $B$ is locally compact and Hausdorff. We've shown $E$ is Hausdorff. Now let $x \in E$ and $p(x) \in B$ with $U$ a neighborhood of $p(x)$ evenly covered by $\{V_\alpha\}$. $B$ is locally compact so there's a neighborhood $W$ of $p(x)$ such that $\mathrm{Cl}(W)$ is compact and $p(x) \in \mathrm{Cl}(W) \subset U$. Let $V_{\alpha'}$ be the slice over $U$ containing $x$. Then $p\mid_{V_{\alpha'}}$ is a homeomorphism from $V_{\alpha'}$ to $U$. As $\mathrm{Cl}(W)$ is a compact subspace of $U$, so too $p\mid_{V_{\alpha'}}^{-1}(\mathrm{Cl}(W))$ is a compact subspace of $V_{\alpha'}$ containing $x$. So $E$ is locally compact. 

**Compact with finite fibers.** Suppose $B$ is compact and $p \colon E \to B$ has finite fibers for each $b \in B$. Let $\sW$ be an open cover of $E$. For each $b \in B$, there are finitely many $W_i$ in $\sW$ such that the fiber $f^{-1}(b) \in \cup_{i=1}^n W_i$. For each $b \in B$, define $U_b$ to be $\cup_1^{n_b} W_i$ containing the fiber over $b$. Observe $p(E \setminus U_b)$ is closed in $B$ and doesn't contain $b$. So $\{(p(E \setminus U_b))^c\}_{b \in B}$ is an open cover of compact $B$. There then exist finitely many $b_j$ such that 
$$(p(E \setminus U_{b_1}))^c \cup \cdots \cup (p(E \setminus U_{b_m}))^c = B.$$ 
Equivalently, 
\begin{align*}
\emptyset & = \cap_1^m p (E \setminus U_{b_j})\\
    & \supset p(\cap_1^m (E \setminus U_{b_j}))\\
    & = p(E \setminus ( \cup_1^m U_{b_j} )).
\end{align*}
So $$E = \bigcup_{j=1}^m U_{b_j} = \bigcup_{j=1}^m \bigcup_{i=1}^{n_{b_j}} W_i,$$ which demonstrates $\sW$ has a finite subcover. We conclude the total space $E$ is compact. \qedsymbol

### [@Mun00, number 54.3]

\gvn Let $p \colon E \to B$ be a covering map, let $\alpha$ and $\beta$ be paths in $B$ with $\alpha(1) = \beta(0)$, and let $\tilde{\alpha}$ and $\tilde{\beta}$ be liftings of them such that $\tilde{\alpha}(1) = \tilde\beta(0)$.

\wts $\tilde\alpha * \tilde\beta$ is a lifting of $\alpha * \beta$.

\pf To verify that the paths $\alpha * \beta = p \circ (\tilde{\alpha} * \tilde{\beta})$, clearly both have the same domain $I$ and codomain $B$. Moreover, they have the same graph as evinced by
$$(\alpha * \beta)(t) = \begin{cases}
\alpha(t), & t \in [0,\frac12]\\
\beta(t), & t \in [\frac12, 1];\end{cases}$$
$$p \circ (\tilde\alpha * \tilde\beta)(t) = \begin{cases}
(p \circ \tilde\alpha)(t), & t \in [0,\frac12]\\
(p \circ \tilde\beta)(t), & t \in [\frac12, 1].\end{cases}$$
We've shown one lift of concatenated paths is the concatenation of the lifts of the individual segments. \qedsymbol

\newpage

### [@Mun00, number 54.4]

\gvn Let $p \colon \RR \times \RR_+ \to \RR^2 \setminus \mathbf{0}$ be defined $$p\colon (\theta,r) \mapsto r\exp(2\pi i \theta).$$

*To demonstrate.* We parametrize and sketch the lifts of the paths $t \in [0,1]$

- $f(t) = (2-t, 0)$
- $g(t) = ((1+t)\cos 2 \pi t, (1+t)\sin 2 \pi t)$
- $h(t) = f * g$.

\newpage

### [@Mun00, number 54.5]

\newcommand{\pmat}[1]{\begin{pmatrix} #1 \end{pmatrix}}

\gvn Let $p \colon \RR^2 \to \TT^2$ be a covering map defined by $$p \colon \pmat{x\\y} \mapsto \pmat{\exp(2\pi i x)\\ \exp(2\pi i y)}.$$ Consider the path $$f(t) = \pmat{\exp(2\pi i t)\\ \exp(4 \pi i t)}.$$

*To demonstrate.* 

- Sketch $f$ when $\TT^2$ is identified with the doughnut surface $D$. 
- Find a lifting $\bar{f}$ of $f$ to $\RR^2$.
- Sketch $\bar f$.

\newpage 

### [@Mun00, number 54.7]

\gvn The torus $\TT^2$.

\wts Without Seifert van Kampen's theorem, $\pi_1(\TT^2) \cong \ZZ^2$.

\pf (Adapted from JP May [@May99, chapter 1].) Consider $\TT^2$ as $S^1 \times S^1 \subset \CC$. For each $\pmat{m\\n} \in \ZZ^2$, define a loop $f_{m,n}$ in $\TT^2$ by 
$$f_{m,n}(s) = \pmat{\exp{2\pi i sm}\\\exp{2\pi i sn}}.$$ It is easy to check $[f_{m,n}][f_{k,\ell}] = [f_{m+k,n+\ell}]$. Define a group homomorphism $i \colon \ZZ^2 \to \pi_1\left(\TT^2, \pmat{1\\1}\right)$ by $i\pmat{m\\n} = [f_{m,n}]$. Now to argue $i$ is an isomorphism of groups.

- Consider the cover $p \colon \RR^2 \to \TT^2$ defined by $p\pmat{x\\y} = \pmat{\exp{2\pi i x}\\\exp{2\pi i y}}$.
- For each representative $f_{m,n}$ in each loop class $[f_{m,n}] \in i(\ZZ^2) \subset \pi_1\left(\TT^2, \pmat{1\\1}\right)$, there's a unique lift $\tilde{f}_{m,n}(s) = \pmat{sm\\sn}$ such that $\tilde{f}_{m,n}(0) = \pmat{0\\0}$. (Apply the path lifting lemma.)
- Define $j \colon\pi_1\left(\TT^2, \pmat{1\\1}\right) \to \ZZ^2$ by $j[f] = \tilde{f}(1)$, a vector in $\ZZ^2$ as $p(\tilde{f}(1)) = \pmat{1\\1}$.
- $j[f]$ is independent of representative from $[f]$ as if $g$ is path homotopic to $f$, then $\tilde{g}(1) = \tilde{f}(1)$. (Apply the homotopy lifting lemma.)
- $j[f_{m,n}] = \pmat{m \\n}$ from explicit definition of $$\tilde{f}_{m,n}(s) = \pmat{sm\\sn},$$ so $j \circ i \colon \ZZ^2 \to \ZZ^2$ is the identity.
- If suffices to check that $j$ is one-to-one for then $i$ is a bijective homomorphism of groups.
    - Suppose $j[f] = j[g]$. Then $\tilde{f}(1) = \tilde{g}(1)$. Thus $\tilde{g}^{-1}*\tilde{f}$ is a loop at $\vec{0}$ in $\RR^2$. Now $\RR^2$ is contractible, therefore $[\tilde{g}^{-1} * \tilde{f}] = [c_{\vec{0}}]$.
    - Applying the induced group homomorphism $p_*$, $[g^{-1}][f] = [g^{-1} * f] = [c_{\vec{1}}],$ the identity in $\pi_1\left(\TT^2, \pmat{1\\1}\right)$.
    - Therefore $[g] = [f]$, and $j$ is one-to-one. \qedsymbol

### [@Mun00, number 54.8] 

\gvn Let $p \colon E \to B$ be a covering map, with $E$ path connected. Suppose $B$ is simply connected.

\wts $p$ is a homeomorphism.

For each $b \in B$, let $p(e) = b$. As $B$ is simply connected, $\pi_1(B, b_0) = \{1\}$. As $E$ is path connected, the induced isomorphism of sets $$\Phi \colon \pi_1(B, b_0)/p_*(\pi_1(E, e_0)) \to p^{-1}(b)$$ shows that the fiber over $b$ is the singleton $\{e\}$. Letting $b$ run through $B$, we see the fibers of $p$ over each $b$ are all singletons. Thus $p$ is injective. We already knew $p$ was an open surjection as a covering map, and thus we conclude $p$ is a homeomorphism. \qedsymbol

### [ @Mun00, number 71.3] 

\gvn $X \cong S^1$ and $Y \cong S^2$. 

\wts $\pi_1(X \vee Y) = \ZZ$. (As $\ZZ$ is abelian, we'll have a canonical isomorphism between any two based fundamental groups on $X \vee Y$.)

\pf Let $X \cap Y= \{x\}$. Now $\pi_1( X \cap Y, x)$ and $\pi(Y, x)$ are trivial (both spaces $X \cap Y$ and $Y$ are simply connected). By Seifert van Kampen, $$\pi_1(X \vee Y, x) \cong \frac{\pi_1(X, x) * \pi_1(Y, x)}{\{e\}} \cong \pi_1(X, x) \cong \pi_1(S_1, 1) \cong \ZZ,$$
noting homotopy groups are preserved under homeomorphism. \qedsymbol

<!---
\setcounter{section}{-1}

## Additional problems from Assignment 6

### [@Mun00, number 51.3]

Let $[X,Y]$ denote the set of homotopy classes of maps of $X$ into $Y$. A space $X$ is said to be *contractible* if the identity map $i_X \colon X \to X$ is nulhomotopic.

(a) The interval $I$ and the real line $\RR$ are both contractible.
(b) A contractible space is path connected.
(c) If $Y$ is contractible, then for any $X$, the set $[X,Y]$ has a single element.
(d) If $X$ is contractible and $Y$ is path connected, then $[X,Y]$ has a single element.


### [@Mun00, number 52.4]

Let $A \subset X$; suppose $r \colon X \to A$ is a continuous map such that $r(a) = a$ for each $a \in A$. The map $r$ is called a retraction of $X$ onto $A$. If $a_0 \in A$, then $r_* \colon \pi_1(X, a_0) \to \pi_1(A, a_0)$ is surjective.

--->
## References
