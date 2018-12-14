---
title: Diagnostic for final
author: Colton Grainger (MATH 6210)
date: 2018-10-19
bibliography: /home/colton/coltongrainger.bib
macros: true
nonumbering: true
---

### 2018-10-10 Midterm 

#### Question 1A

Recall that the **upper-limit topology** is the topology $\sU$ on $\RR$ with basis
$$\{(a,b] : a,b \in \RR, a \le b\}.$$

i. Determine whether the sets $(a,b)$ and $[a,b)$ are open and/or closed in $(\RR, \sU)$. Explain.
ii. Is $(\RR, \sU)$ connected? Explain.

#### Question 1B

Let $X$ be a nonempty set. Is $X$ with the finite complement topology connected? Is the answer the same for all sets $X \neq \emptyset$, or do you need to distinguish cases that depend on certain properties of $X$? Give proof.

#### Question 2A

Let $\sN = \{1/n : n \in \NN\} \subset \RR$ denote the set of all reciprocals of natural numbers. Let $$\sB = \{(a,b) : a,b \in \RR\} \cup \{(a,b) \setminus \sN : a,b \in \RR\} \cup \{\RR, \emptyset\}.$$ 
Now $\sB$ generates a topology on $\RR$, denote that topology $\sT_\sB$. 

i. What is the closure of $\sN$ in $\sT_\sB$?
ii. Is every closed set of the topological space $(\RR, \sT_\sB)$ closed in the standard topology on $\RR$?

#### Question 2B

Is every closed set of the standard topology on $\RR$ also closed in the finite complement topology on $\RR$?

#### Question 3

For $n,m \in \ZZ_{\ge 0}$, prove that $(Y_n, \sT_n)$ is homeomorphic to $(Y_m, \sT_m)$ iff $n = m$. Let $(Y_n, \sT_n)$ is defined as follows.

- Start with the subspace $X_n \subset \RR^3$ parametrized by 
$$X_n := \{(x,y,z) : (x-(1+4j))^2 + y^2 + z^2 = 1 \text{ for some } j = 1, \ldots, n\}.$$
- Define the equivalence relation $\sim_n$ on $X_n$ where each point is equivalent to itself and 
$$(0,0,0) \sim_n (4,0,0) \sim_n (8,0,0) \sim_n \ldots \sim_n (4n, 0, 0).$$
- Let $(Y_n, \sT_n)$ be the space of equivalence classes $Y_n := X_n /\sim_n$ endowed with the quotient topology.


#### Question 4A

Prove or provide a counter-example: The path connected components of a topological space are always closed sets.

#### Question 4B

Prove or provide a counter-example: The path connected  components of a topological space are always open if the space is locally path connected?

### 2018-11-07 Midterm 

#### Question 1A

Compute the homotopy classes of maps $S^0 \to S^0$.

#### Question 1B

Prove that if the space $(X, \sT)$ is path connected, then $\pi_1(X, x_0) \cong \pi_1(X, x_1)$ for arbitrary $x_0, x_1 \in X$.

#### Question 1C

Prove that the fundamental group of the real line based with the standard topology, based at the origin, is trivial.

#### Question 2A

Let $(X, \sT)$ and $(Y, \sW)$ be two spaces and let $f \colon X \to Y$ be a surjective map. Prove that if $X$ is Lindelöff, or has a countable dense subset, then $Y$ satisfies the same condition.

#### Question 2B

Prove that if a topological space $(X,\sT)$ is compact, then it is also limit point compact.

#### Question 2C

For the real line $\RR$ with the standard topology, a subspace $C \subset \RR$ is compact if and only if it's closed and bounded. Is the same true for the real line $\RR_\ell$ with the lower limit topology?

#### Question 3A

Show that every metrizable topological space $(X, \sT)$ with a countable dense subset $S$ has a countable basis.

#### Question 3B

Give an example of a topological space with a compact subset that is not closed.

### Quotienting

i. Prove that $D^n / S^{n-1}$ is homeomorphic to $S^n$.[@VINK08, number 22.D]
i. Prove that $S^1 \times S^1/[(z,w) \sim (-z, \bar{w})]$ is homeomorphic to the Klein bottle $I^2/[(t,0 \sim (t,1), (0,t) \sim (1, 1-t)]$. [@VINK08, number 22.14]

### Gluing

Recall: if $X$ and $Y$ are topological spaces, $A \subset Y$, and $f \colon A \to X$ is a continuous map, then the *gluing* (or *attaching*) of $Y$ to $X$ via $f$ is the quotient space $$X \cup_f Y = X \sqcup Y / [a \sim f(a) : a \in A].$$

i. Prove that, by attaching the $n$-disk $D^n$ to its copy via the identity map of the boundary sphere $S^{n-1}$, we obtain a space homeomorphic to $S^n$. [@VINK08, number 22.M]

### Real projective space

Recall $\RR\PP^n$ is the quotient space of $S^n$ by the partition into pairs of antipodal points.

i. Show that $\RR\PP^n$ is canonically homeomorphic to the metric space whose points are lines of $\RR^{n+1}$ through the origin, where the angle measure between two lines serves as a metric. Check that angle measure *does* give a metric. (Hint: use homogeneous coordinates $(x_0 : x_1: \cdots : x_n)$ in $\RR\PP^n$.) [@VINK08, number 23.F] 
i. Prove that the natural projection $S^n \to \RR\PP^n$ is a covering.

### Deformation retractions

\providecommand{\id}{\mathrm{id}}
Recall: If $X$ is a space and $A \subset X$, then $\rho \colon X \to A$ is a *retraction* if $\rho$ is continuous and $\rho\mid_A = \id_A$. A retraction $\rho \colon X \to A$ is a *deformation retraction* if its composition $\iota \circ \rho$ with $\iota \colon A \hookrightarrow X$ is homotopic to the identity map $\id_X$ on $X$. Lastly, a continuous map $f \colon X \to Y$ is said to be a *homotopy equivalence* between $X$ and $Y$ if there's a continuous map $g \colon Y \to X$ such that $g \circ f \cong \id_X$ and $f \circ g \cong \id_Y$. Two spaces $X$ and $Y$ are said to be *homotopy equivalent* if there exists a homotopy equivalence between them.

i. Prove that if $A$ is a deformation retraction of $X$, then $A$ and $X$ are homotopy equivalent. [@VINK08, number 39.D]
i. Prove that any two deformation retractions of one and the same space are homotopy equivalent. [@VINK08, number 39.E]
i. Prove that $S^n$ is a deformation retraction of $\RR^{n+1} \setminus \{0\}$. [@VINK08, number 39.G]

### Bouquet of circles

Recall: Given a family of topological space $\{X_\alpha\}$, we may mark a point $x_\alpha$ in each, take the disjoint sum and identify all marked points. The resulting topological space $\vee_\alpha X_\alpha$ is the *bouquet* of $\{X_\alpha\}$. Let $B_q$ denote the *bouquet of $q$ circles*. Let $u_1, \ldots, u_q$ be loops in $B_q$ starting at $c$ and parametrizing the $q$ copies of $S^1$. Denote by $\alpha_i$ the homotopy class of $u_i$.

i. Prove that a plane with $q$ punctures is homotopy equivalent to the bouquet of $q$ circles. [@VINK08, number 39.4].

### Covering maps

i. Prove that $\RR \to S^1 \colon x \mapsto \exp(2\pi i x)$ is a covering. [@VINK08, number 34.C]
i. Prove that $\CC \to \CC \colon z \mapsto \exp(z)$ is a covering. [@VINK08, number 34.F]
i. In what sense are the above coverings the same? Define an appropriate equivalence relation. [@VINK08, number 34.2]

## References
