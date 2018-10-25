---
title: Connectedness
author: Colton Grainger (Topology MATH 6210)
date: 2018-10-05
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

\setcounter{section}{4}

## Assignment due 2018-10-24

### [@Mu00, number 26.1]

Let $\sT$ and $\sT'$ be two topologies on the set $X$; suppose that $\sT \supset \sT$. 

(a) What does compactness of $X$ under one of these topologies imply about compactness under the other?

(b) If $X$ is compact Hausdorff under both $\sT$ and $\sT'$, then either $\sT$ and $\sT'$ are equal or they are not comparable.

### [@Mu00, number 26.5]

Let $A$ and $B$ be disjoint compact subspaces of the Hausdorff space $X$. There exist disjoint open sets $U$ and $V$ containing $A$ and $B$, respectively.

### [@Mu00, number 26.7]

If $Y$ is compact, then the projection $\pi_1 \colon X \times Y \to X$ is a closed map.

### [@Mu00, number 26.11]

Let $X$ be a compact Hausdorff space. Let $\sA$ be a collection of closed connected subsets of $X$ that is simply ordered by proper inclusion. Then $$Y = \bigcap_{A \in \sA} A$$ is connected. 

**Lemma.** In the setup above, if $C \cup D$ is a separation of $Y$, we can choose disjoint open sets $U$ and $V$ of $X$ containing $C$ and $D$, respectively, where $$\bigcap_{A\in \sA}\left(A \setminus (U \cup V)\right) \neq \emptyset.$$

### [@Mu00, number 26.12]

Let $p \colon X \to Y$ be a closed continuous surjective map such that $p^{-1}(\{y\})$ is compact, for each $y \in Y$ (such a map is called a *perfect map*). If $Y$ is compact, then $X$ is compact.

**Lemma.** In the setup above, if $U$ is an open set containing $p^{-1}(\{y\})$, there is a neighborhood $W$ of $y$ such that $p^{-1}(W)$ is contained in $U$.

### [@Mu00, number 27.3]

In $\RR_K$, the $K$-topology on the real line:

(a) $[0,1]$ is not compact.
(b) $\RR_K$ is connected. (Consider $(-\infty, 0)$ and $(0, \infty)$ with their usual topologies.)
(c) $\RR_K$ is not path connected.

### [@Mu00, number 27.4]

A metric space having more than one point is uncountable.

### [@Mu00, number 27.5]

This is a special case of the *Baire category theorem*. Let $X$ be a compact Hausdorff space, let $\{A_n\}$ be a countable collection of closed sets of $X$. If each $A_n$ has empty interior in $X$, then the union $\cup A_n$ has empty interior in $X$. 

**Theorem.** Let $X$ be a nonempty compact Hausdorff space. If $X$ has no isolated points, then $X$ is uncountable. [@Mu00, p. 176]

### [@Mu00, number 28.2]

$[0,1]$ is not limit point compact as a subspace of $\RR_\ell$.

### [@Mu00, number 28.3]

Let $X$ be limit point compact. 

(a) If $f \colon X \to Y$ is continuous, does it follow that $f(X)$ is limit point compact?
(b) If $A$ is a closed subset of $X$, does it follow that $A$ is limit point compact?
(c) If $X$ is a subspace of the Hausdorff space $Z$, does it follow that $X$ is closed in $Z$?

Note: it's not in general true that the product of two limit point compact spaces in limit point compact, even if the Hausdorff condition is assumed.

## References
