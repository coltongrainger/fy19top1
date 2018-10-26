---
title: Compactness
author: Colton Grainger (Topology MATH 6210)
date: 2018-10-26
bibliography: /home/colton/Downloads/coltongrainger.bib
macros: true
---

\providecommand{\Int}[1]{\mathrm{Int}\left( #1 \right)}
\providecommand{\Cl}[1]{\mathrm{Cl}\left( #1 \right)}
\setcounter{section}{4}

## Assignment due 2018-10-26

### [@Mu00, number 26.1]

Let $\sT$ and $\sT'$ be two topologies on the set $X$; suppose that $\sT \supset \sT'$. 

(a) What does compactness of $X$ under one of these topologies imply about compactness under the other?

    If $(X, \sT)$ is compact, then $(X, \sT')$ is compact. The converse fails to hold generally.

(b) If $X$ is compact Hausdorff under both $\sT$ and $\sT'$, then either $\sT$ and $\sT'$ are equal or they are not comparable.
    
    Suppose $\sT' \subset \sT$ and both spaces are Hausdorff. The identity $(X, \sT') \xrightarrow{\mathrm{id}} (X, \sT)$ is a continuous bijection. Since the domain is Hausdorff and the codomain in compact, it's a homeomorphism. \qedsymbol

### [@Mu00, number 26.5]

Let $A$ and $B$ be disjoint compact subspaces of the Hausdorff space $X$. There exist disjoint open sets $U$ and $V$ containing $A$ and $B$, respectively.

*Proof.* Try to cover one at a time! Fix $a \in A$. As $X$ is Hausdorff, we can find pairs $U_{(a,b)}$ and $V_{(a,b)}$ of open sets to separate the fixed point $a$ from each point $b$ as $b$ varies through $B$.

Now $\{V_{(a,b)}\}$ is an open cover of $B$. There's a finite set of points $\{b_j\}_1^n$ corresponding to the finite subcover of $B$ by $\{V_{(a,b_j)}\}_1^n$. Moreover the corresponding $U_{(a,b_j)}$ satisfy $a \in \cap_1^n U_{(a,b_j)}$.

Since $a$ was fixed, and we need to vary $a$, let's save memory of these open sets for later and denote 
$$U_a =  \bigcap_1^n U_{(a,b_j)} \quad\text{ and }\quad V_a = \bigcup_1^n V_{(a,b_j)}.$$
Now let $a$ run through $A$. We generate an open cover $\{U_a\}$ of $A$ with each set $U_a$ separated from $B$ and $V_a$. There's then a finite subcover $\{U_{a_k}\}_1^m$ with $\{V_{a_k}\}_1^m$ corresponding. A separation of $A$ and $B$ by open sets is given by $$\underbrace{\bigcup_1^m U_{a_i}}_{\text{containing } A} \cap \underbrace{\bigcap_1^m V_{a_i}}_{\text{containing } B} = \emptyset$$
as desired. \qedsymbol

### [@Mu00, number 26.7]

If $Y$ is compact, then the projection $\pi_1 \colon X \times Y \to X$ is a closed map.

*Proof.* Let $K \in X \times Y$ be closed. We want to show that $X \setminus \pi(K)$ is $X$-open. 

Let $z \in X \setminus \pi(K)$. Since $K$ is closed and the slice $\pi^{-1}(z)$ is disjoint from $K$, each point in $\pi^{-1}(z)$ can be separated from $K$ by an open $N_\alpha$ in the product space. Call the union of such $N = \cup N_\alpha$. 

Observe both $N \cap K = \emptyset$ and $N \supset \pi^{-1}(z)$. (Alternatively, the existence of open $N$ follows from the previous exercise, as $\pi^{-1}(z)$ is compact.) By the tube lemma, there's an $X$-open $U \ni x$ such that $\pi^{-1}(U) \subset N$. By construction, $N$ separates $\pi^{-1}(U)$ from $K$, so $$\pi(K) \cap U = \emptyset.$$ 
So each point in $X \setminus \pi(K)$ can be contained in an open set $U \subset X\setminus\pi(K)$. 

We've shown $X \setminus \pi(K)$ is open; therefore $\pi(K)$ is closed. We conclude that $\pi$ is a closed map. \qedsymbol

### [@Mu00, number 26.11]

Let $X$ be a compact Hausdorff space. Let $\sA$ be a collection of closed connected subsets of $X$ that is simply ordered by proper inclusion. Then $$Y = \bigcap_{A \in \sA} A$$ is connected. 

*Proof.*^[See also <https://math.stackexchange.com/questions/1238027>] By way contradiction, suppose $C$ and $D$ separate $\cap_{A \in \sA} A$. Note that $C$ and $D$ are closed in $X$ as closed sets in the closed subspace $\cap A$. Since $X$ is Hausdorff with $C$ and $D$ closed (thus compact), we can find disjoint $X$-open $U \supset C$ and $V \supset D$ separating $C$ and $D$.

Because the collection $\sA$ is a family of compact subsets of the compact space $X$, and $\cap_{A \in \sA} A \subset U \cup V$, we must have
$$\bigcap_{A\in \sA}\left(A \setminus (U \cup V)\right) = \emptyset.$$
Since the collection $\sA$ is linearly ordered, there's a set $B \in \sA$ such that $B \subset U \cup V$. But then $B$ is separated by $U$ and $V$, which is absurd. So the set $\cap A$ is connected. \qedsymbol

### [@Mu00, number 26.12]

Let $p \colon X \to Y$ be a closed continuous surjective map such that $p^{-1}(\{y\})$ is compact, for each $y \in Y$ (such a map is called a *perfect map*). If $Y$ is compact, then $X$ is compact.

*Proof.*^[See also <https://math.stackexchange.com/questions/902472/>.] We lead out with the lemma.

*Lemma.* In the setup above, if $U$ is an open set containing $p^{-1}(\{y\})$, there is a neighborhood $W$ of $y$ such that $p^{-1}(W)$ is contained in $U$.

For each $y \in Y$, take an $X$-open $U_y \supset p^{-1}(\{y\})$. Observe 

- $X\setminus U_y$ is closed in $X$
- $p(X\setminus U_y)$ is closed in $Y$
- $y \in \underbrace{ Y\setminus p(X \setminus U_y) }_{\text{open!}}$ 

Denote the open set $W_y :=  Y\setminus p(X \setminus U_y)$. By construction $y \in W_y$ and $$W_y \text{ is the complement of the image of the complement of } U_y,$$ therefore $p^{-1}(\{y\}) \subset p^{-1}(W_y) \subset U_y$.

Now continuing the proof, let $\{U_\alpha\}$ cover $X$. Since $p^{-1}(\{y\})$ is compact, there's a finite subcover $\{U_j\}_1^n$ such that $$p^{-1}(\{y\}) \subset \bigcup_1^n U_j.$$

For each $y$, obtain an open cover of $Y$ as follows

- Set $U_y = \bigcup_1^{n_y} U_j^y$ as a finite subcover of $p^{-1}(\{y\})$.
- Take the open $W_y$ corresponding to $U_y$ from the lemma.

Since there's an open $W_y$ containing each $y \in Y$, the collection $\{W_y\}$ is a open cover of $Y$. Since $Y$ is compact, there's a finite subcover $\{W_{y_k}\}_1^m$ with 
$$p^{-1}(\{y_k\} \subset p^{-1}(W_{y_k}) \subset \bigcup_1^{n_{y_k}} U_j.$$
Now $X = p^{-1}(Y)$, thus 
$$X = \bigcup_1^m \underbrace{p^{-1}(W_y)}_{\text{all with finite covers}}$$ 
demonstrating any $\{U_\alpha\}$ open cover of $X$ contains a finite subcover. \qedsymbol

### [@Mu00, number 27.3]

In $\RR_K$, the $K$-topology on the real line:

(a) $[0,1]$ is not compact.

    *Recall the previous exercise.* If $(X,\sT)$ and $(X, \sT')$ are both compact Hausdorff and comparable, then $\sT = \sT$. 
    
    Both the standard topology $\mathrm{ST}$ and the $K$-topology induce a subspace topology on $[0,1]$. From analysis, we know that $[0,1]$ is compact Hausdorff in $\mathrm{ST}$. Now $\RR_K$ is strictly finer than $\mathrm{ST}$. By the contrapositive of the previous exercise, either $[0,1]$ must fail to be compact or fail to be Hausdorff. Clearly $[0,1]$ is Hausdorff in $\RR_K$, so $[0,1]$ fails to be compact. \qedsymbol

(b) $\RR_K$ is connected. 

    Consider $(-\infty, 0)$ and $(0, \infty)$ with their usual topologies as subspaces from the real line. Now I claim both sets are induced with the same relative topology from $\RR_K$. We focus on the positive valued interval. The following are equivalent

    - $U$ is $\RR_K$-open in $(0,\infty)$ 
    - $U$ is $(0,\infty) \cap V$ for $V$ $\RR_K$-open in $\RR$
    - $U$ is $(0, \infty) \cap W$ for $W$ open in the standard topology and $W \not\ni 0$.

    Both intervals are connected in the standard topology. Also, the closures

    - $\Cl { (-\infty, 0) } = (\infty, 0]$ 
    - $\Cl { (0, \infty ) } = [0, \infty)$
    
    are connected. Therefore $\RR_K = (-\infty, 0] \cap [0, \infty)$ is connected. \qedsymbol

(c) $\RR_K$ is not path connected.

    We've just seen that $[0,1]$ is not compact in $\RR_K$, so we'll argue for a contradiction. Suppose $p \colon [0,1] \to \RR_K$ is a path from $p(0) = 1$ to $p(1) = 0$ (going down to the origin). But the image of a compact, connected set under a continuous map is compact and connected, and $[0,1]$ is not compact in $\RR_K$. Absurd! \qedsymbol

### [@Mu00, number 27.4]

A *connected* metric space having more than one point is uncountable.

*Proof.* Consider two points $x$ and $y$ in the metric space, with a distance function $d$. Let $t \in (0,1)$ be a parameter to obtain a contradiction.

If there's no $\alpha$ in the metric space such that $d(x, \alpha) = td(x,y)$, then we have a separation of the space into nonempty open sets $\{\beta : d(x, \alpha) < td(x,y)\}$ and $\{\beta : d(x, \alpha) > td(x,y)\}$. \qedsymbol

### [@Mu00, number 27.5]

This is a special case of the *Baire category theorem*. Let $X$ be a compact Hausdorff space, let $\{A_n\}$ be a countable collection of closed sets of $X$. If each $A_n$ has empty interior in $X$, then the union $\cup A_n$ has empty interior in $X$. 

*Given.* $X$ a compact Hausdorff space, $\{A_n\}_\NN$ closed sets with empty interiors.

*To prove.* $\Int{\cup_\NN A_n}$ is empty.

*Proof.* We can find open sets disjoint from closed sets in $X$ like we could find open sets disjoint from points in the proof "if $X$ is a nonempty compact Hausdorff space and $X$ has no isolated points, then $X$ is uncountable."

Explicitly, if $K$ is a closed set in $X$ and $U$ is an open set such that $U\setminus K \neq \emptyset$, then there's an open set $V \subset U$ such that $\Cl V \subset U \setminus K$. See [@Mu00, page 176].

We'll show any open $V$ has a point $x \notin \cup_\NN A_n$. So let $V$ be open. Since $\Int { A_1 }$ is empty, we have by the previous argument $V_1 \subset V \setminus A_1$, with $\Cl V \subset V \setminus A_1$. We'll define now a nested sequence of closed sets $\Cl V_1 \supset \Cl V_2 \supset \cdots$ inductively by finding 
$$V_n \subset V_{n-1} \setminus A_n \quad \text{ with }\quad \Cl { V_n } \subset V_{n-1} \subset \Cl { V_{n-1} }.$$
Now since $X$ is compact, there exists a point 
$$x \in \underbrace{\bigcap_\NN \Cl { V_n }}_{\text{contained in }V} \quad\text{such that}\quad x \notin \bigcup_\NN A_n,$$
which demonstrates the union $\cup A_n$ has trivial interior. \qedsymbol

### [@Mu00, number 28.2]

$[0,1]$ is not limit point compact as a subspace of $\RR_\ell$.

*Demonstration*. Consider the open set $\{1\}$ in $\RR_\ell$. We have a sequence $$\sin\left(\frac{n\pi}{(n+1)2}\right) \xrightarrow{\mathrm{ST}} 1$$ that converges in the standard topology, but fails to converge in the lower limit topology $\RR_\ell$. \qedsymbol

### [@Mu00, number 28.3]

Let $X$ be limit point compact. 

(a) If $f \colon X \to Y$ is continuous, does it follow that $f(X)$ is limit point compact?

    No. Consider the continuous projection of sets in $\NN \times \{0,1\}$ onto $\NN$ (where $\{0,1\}$ is an indiscrete space and $\NN$ discrete).

(b) If $A$ is a closed subset of $X$, does it follow that $A$ is limit point compact?
    
    Yes. Any infinite subset of $A$ has a limit point in $X$ as setup above.

(c) If $X$ is a subspace of the Hausdorff space $Z$, does it follow that $X$ is closed in $Z$?

    No. Consider the minimal uncountable well-ordered set $S_\Omega \subset \overline{S_\Omega}$. 

## References
