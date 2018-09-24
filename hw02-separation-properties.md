---
title: Continuity and Common Spaces
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

*Proof sketch.* (a) implies (c) implies (b) implies (a). I had proved each implication on paper but misplaced my notes. I may revise this proof in a latter assignment.

### Continuity by nested interiors

Consider the same spaces $(X,\sT)$ and $(Y,\sW)$ again with a function $f \colon X \to Y$. The following are also equivalent.

\newcommand{\Int}[1]{\left(#1\right)^\circ}

(a) $f$ is continuous.
(b) $f^{-1}(\Int{B}) \subset \Int{f^{-1}(B)}$ for all sets $B\subset Y$ in the codomain.

*Proof sketch.* (a) implies (b) implies (a). Same case as above.

### Homeomorphic subspaces of the real line [@Mu00, number 18.5]

The subspace $(a,b)$ of $\RR$ is homeomorphic with $(0,1)$.

*Proof.* Let $f \colon (a,b) \to (0,1)$ with $x \mapsto \frac{x-a}{b-a}$. We'll show that $f$ is (i) bijective, (ii) continuous, and (iii) open. Whence $f$ will be a homeomorphism. 

(i) Let $f^{-1}\colon (0,1) \to (a,b)$ be defined by $y \mapsto (b-a)y + a$. Then $f \circ f^{-1} = \text{id}_{(0,1)}$ and $f^{-1} \circ f = \text{id}_{(a,b)}$, so $f$ has a two-sided inverse, and therefore $f$ is a bijection.

(ii) Take an open interval $B_\epsilon(y) \subset (0,1)$. Now $$f^{-1}(B\epsilon(y)) = B_\delta(f^{-1}(y)) \subset (a,b) \text{ for } \delta = (b-a)\epsilon$$ is open too.

(iii) Suppose $B_{\epsilon'}(x)$ is open in $(a,b)$. Then $f(B_{\epsilon'}(x)) = B_\delta(f(x)) \subset (0,1)$ for $\delta' = \frac{\epsilon'}{b-a}$ is open in $(0,1)$. \qedsymbol

Also, the subspace $[a,b]$ (of $\RR$) is homeomorphic with $[0,1]$.

*Proof.* Extend $f$ above defined to $g \colon [0,1] \to [a,b]$ with the same rule of assignment $x \mapsto \frac{x-a}{b-a}$.

(i) $g^{-1}$ exists as the extension of $f^{-1}$ and is the two sided inverse of $g$, whence $g$ is a bijection.

(ii) Suppose $U$ is open in $[0,1]$, then $U = W \cap [0,1]$ for $W$ $\RR_{std}$-open. So $f^{-1}(U) = f^{-1}(W) \cap [a,b]$, which is open in $[a,b]$ iff $f^{-1}(W)$ is open in $\RR_{std}$. Take any open interval $B_\epsilon(y) \subset W$. Then for a radius $\delta = (b-a) \epsilon$ and a point $x = (b-a)y +a$ we have $$f^{-1}(B_\epsilon(y)) = B_\delta(z) \subset f^{-1}(W).$$ Hence $f^{-1}(W)$ is the union of open intervals in $\RR_{std}$ and therefore open itself.

(iii) Suppose $B$ is a basis element of the subspace $[a,b]$, then $B = B_{\epsilon'}(x) \cap [a,b]$ and $f(B) = f(B_{\epsilon'}(x)) \cap f([a,b]) = B_{\delta'}(f(x)) \cap [0,1]$ is open in $[0,1]$ for $\delta' = \frac{\epsilon'}{b-a}$. \qedsymbol

### Continuous at a single point [@Mu00, number 18.6]

The function $f \colon \RR \to \RR$ defined by 
$$f(x) = 
\begin{cases}
x^2 & \text{ if } x \in \QQ,\\
-x^2 & \text{ else}
\end{cases}$$
is continuous at a single point in the domain, namely $0$.

*Proof.* Let $x\neq 0$ be a real number in the domain. The image $f(x)$ is nested in the open interval $B_\epsilon(f(x))$ with $\epsilon = x^2 > 0$. Now consider any open ball $B_\delta(x)$ in the domain. Both $\RR \setminus \QQ$ and $\QQ$ are dense in $\RR$, so there's a point $p \in \QQ$ and $\alpha \in \RR \setminus \QQ$ such that $p, \alpha \in B_\delta(x)$. Whence we have that the open interval $f(B_\delta(x))$ contains both positive and negative points, whereas $B_\epsilon(f(x))$ contains either only positive points, if we choose $x \in \QQ$, or only negative points, if we choose $x \in \RR \setminus \QQ$. Hence $f(B_\delta(x) \not\subset B_\epsilon(f(x))$. Therefore $f$ is not continuous at $x \neq 0$.

If $x = 0$ then for any $\epsilon > 0$ there's a $\delta = \sqrt{\epsilon}$ such that $F(B_\delta(0)) \subset B_\epsilon(0)$, so $f$ is continuous at $x=0$. \qedsymbol

### Left and right continuity [@Mu00, number 18.7]

(a) Suppose that $f \colon \RR \to \RR$ is right continuous[^func-limit] at each point $a \in \RR$. Then $f$ is continuous when consider as a function from $\RR_\ell$ to $\RR$.

[^func-limit]: See discussion from “Definition of limit of function on topological spaces”, <https://math.stackexchange.com/questions/835978>. Mathematics Stack Exchange. Retrieved September 23, 2018.

    > `mle:` Let be $(A,\tau)$,$(C,\zeta)$ two topological spaces, $f \in C^E$, with $E \subseteq A$, and $x_0$ an accumulation point of $E$, a point $l \in C$ is *limit* of $f$ as $x$ approaches $x_0$ if $\forall Y \in \mathcal{U}_{(C,\zeta)}(l) (\exists X \in \mathcal{U}_{(A,\tau)}(x_0)(f((X-\{x_0\} )\cap E) \subseteq Y))$  where $\mathcal{U}_{(A,\tau)}(x_0)$ is neighbourhood system for $x_0$ and $\mathcal{U}_{(C,\zeta)}(l)$ is neighbourhood system for $l$.

    > `Daniel Fischer:` Another way to put the definition is to say that $\tilde{f}\colon E\cup \{x_0\} \to C$ [is continuous when] defined by $$\tilde{f}(x) = \begin{cases} f(x), & x \in E\setminus\{x_0\} \\ l, & x = x_0.\end{cases}$$
    *Proof.* Suppose $f$ is right continuous at all points in its domain. That is, suppose $\lim_{x \to a^+} f(x) = f(a)$ for all $a \in \RR$. Then for any point $a \in \RR$ and any neighborhood $Y$  in the local neighborhood system $\mathcal{U}_{(\RR, \sT_{std})}(f(a))$ about $f(a)$ there's a neighborhood $X$ in the neighborhood system $\mathcal{U}_{(\RR, \sT_\ell)}(a)$ surrounding $a$ (where $\sT_\ell$ denotes the lower limit topology) such that $f(X\setminus \{a\}) \subset Y$. Now since $f(\{a\}) \subset Y$, we know $f(x) = f(X \setminus\{a\} \cup \{a\}) \subset Y$. So $f \colon (\RR, \sT_\ell) \to (\RR, \sT_{std})$ is continuous at every point in its domain, therefore *continuous*.

(b) We exhaustively list the functions 

  - which are continuous from $\RR$ to $\RR_\ell$, also 
  - which are continuous from $\RR_\ell$ to itself.

For (a) note $\RR_\ell$ is finer than $\RR$ (here $\RR_\ell$ denotes the topological space on the real numbers endowed with the lower limit topology), so $C_\RR(\RR_\ell) \subset C_\RR(\RR)$ (where $C_D(Y)$ denotes the set of continuous functions out of some space $D$ into the space $Y$). 

Now I claim $C_\RR(\RR_\ell)$ is the set of constant functions. 

*Proof.* ($\subset$) For suppose $f$ is a constant function. Then for all $\RR_\ell$-open $U$, either $f^{-1}(U) = \emptyset$ or $f^{-1}(U) = \RR$, both open in $\RR$. So $f \in C_\RR(\RR_\ell)$. 

($\supset$) In the other direction, suppose that $f \in C_\RR(\RR_\ell)$ with $f$ not constant. Then WLOG there exist $a < b$ such that $f(a) < f(b)$. Let $$C = \{c \in (a,b) : f(c) \in (f(a),f(b))\}.$$ Since $f \in C_\RR(\RR)$ we have the intermediate value property, therefore $C$ is a non-empty bounded set of real numbers. Now let $c = \inf C$. I claim $f^{-1}([f(c),f(b)))$ is not open in $\RR$. Indeed $c \in f{-1}([f(c),f(b)))$ but for all $\epsilon > 0$ the open interval $B_\epsilon(c) \not\subset f^{-1}([f(c),f(b)))$. Why? Because if $c - \epsilon/2 \in f^{-1}([f(c),f(b)))$, then $$f(c - \epsilon/2) \in [f(c), f(b)) \subset (f(a),f(b))$$ but $c - \epsilon/2 < c = \inf C$, a contradiction. So if $f$ is not constant, then $f$ is not continuous from $\RR \to \RR_\ell$. \qedsymbol

I conjecture (without proof) $f \colon \RR \to \RR_\ell$ is continuous iff $f$ is piecewise defined as $\RR_{std}$ continuous and monotonically increasing on each set of any partition of $\RR$ into countably many half open intervals.

### Maps into the order topology [@Mu00, number 18.8]

Let $Y$ be an ordered set in the order topology. Let $f,g \colon X \to Y$ be continuous maps. 

(a) The set $\{x : f(x) \le g(x)\}$ is closed in $X$.
(b) The function $h\colon X \to Y$ defined by $h(x) = \min\{f(x),g(x)\}$ is continuous.

*Proof.* To show (a) that $K = \{x : f(x) \le g(x)\}$ is closed in $X$, note that if for all $x \in X$ we have that $f(x) \le g(x)$, then $K = X$ and we're done. So suppose that for some $x \in X$ it's the case that $f(x) > g(x)$. Now we'll argue that $K$ contains all of its limit points. 

For contradiction, suppose $K$ has a limit point $k$ such that $k \notin K$ (that is, $f(k) > g(x)$). Since $k$ is a limit point of $K$ for all open sets $V$ in $X$ (including the pullbacks $f^{-1}(U)$ and $f^{-1}(U)$ of some open $U \in Y$) we that $$V \cap (K \setminus \{k\}) \neq \emptyset.$$ Take a $X$ basis element $B \ni f(k)$ such that if $B$ contains no points^[Verify $B$ is nonempty, consider $f(k) \in B$.] $c$ such that $f(c) \leq g(c)$. Then $f^{-1}(B)$ is $X$ open and yet $$f^{-1}(B) \cap (K \setminus \{k\}) \subset \{x : f(x) \in B\} \cap \{x \colon f(x) \le g(x)\} = \emptyset$$ since if $f(x) \in B$ then $f(x) > g(x)$. Therefore if $k$ is a limit point of $K$, we must have that $k \in K$. So $K$ is closed.

To show (b) that $h$ is continuous, take any $a \in X$. We will demonstrate that for all $Y$-open basis sets $B(h(a))$ there's a $X$ open $U$ such that $h(U) \subset B(h(a))$. Note that if $h(a) = f(a) = g(a)$ we are done, as there exist open $U_f\ni a$ and $U_g\ni a$ satisfying $f(U_f) \subset B(h(a))$ and $g(U_g) \subset B(h(a))$, and $a \in U = U_f \cap U_g$ will satisfy $h(U) \subset B(h(a))$. So without loss of generality, suppose that $h(a) = g(a) < f(a)$ and consider $B(h(a)) = B(g(a))$. Now, because $g$ is continuous at $a$, there's an open set $U_g \cap a$ such that $g(U_g) \subset B(g(a))$. Take the open set (its the complement of a set we just proved is closed) $$V =\{x \colon g(x) < f(x)\}$$ and we have the desired open set $U_g \cap B$ such that $$h(U_g \cap V) = g(U_g \cap V) \subset g(U_g) \subset B(g(a))$$ where the first equality is by definition of $h$ and choice of $V$. \qedsymbol

### Maps out of the product topology [@Mu00, number 18.12]

Let $F \colon \RR \times \RR$ be defined by 
$$F(x\times y) = \begin{cases}
\frac{xy}{x^2 + y^2} & \text{ if } x \times y \neq 0 \times 0,\\
0 & \text{ else.}
\end{cases}$$

  (a) $F$ is continuous in each variable separately.
  (b) We compute the restriction $g \colon \RR \to \RR$ defined by $g(x) = F(x \times x)$.
  (c) $F$ is not continuous.

*Demonstration.* Without loss of generality, we'll show that $F$ is continuous in $x$ (since $F$ is symmetric in $x$ and $y$ by relabelling). Fix $y = y_0$ and restrict $F\rvert_{\RR \times \{y_0\}}$ to the horizontal line through $y_0$. That $F\rvert_{\RR \times \{y_0\}}$ is continuous for $(x,y_0) \neq (0,0)$ is clear, for it's an sum, product, and quotient of continuous functions. Now suppose that $(x,y_0) = (0,0)$. Then, consider any $\RR$-basis element $B_\epsilon(0)\ni 0$ for $\epsilon > 0$. The open set $\RR$ maps into $B_\epsilon(0)$ since (with $y_0 = 0$) the restriction $F\rvert_{\RR \times \{0\}}(x) = 0$ for all $x \in \RR$. We've shown (a) that $F$ is continuous in each variable separately.

Now let $g \colon \RR \to \RR$ be defined as the composition $g = F \circ h$ where $$\RR \xrightarrow{h} \RR^2 \xrightarrow{F} \RR$$ and $h\colon x \mapsto (x,x)$. Then $$g(x) = \begin{cases} \frac12, &x \neq 0\\ 0, &x = 0.\end{cases}$$ This shows (b).

Lastly, for (c), given $g$ is *not* continuous from $\RR$ to $\RR$, yet $h$ is continuous, we must have that $F$ is not continuous. \qedsymbol

### Projections and quotient maps [@Mu00, number 22.3]

Let $\pi_1 \colon \RR \times \RR \to \RR$ be the projection on the first coordinate, and consider the subspace $A = \{x\times y : x \ge 0 \text{ or } y = 0 \}$. The restriction $q\colon A \to \RR$ obtained by $q = \pi_1|_A$ is a quotient map that is neither open nor closed.

*Proof.* Let the map $q \colon A \to \RR$ be defined by the composition $q(z) = (\pi_1 \circ \iota)(z)$ where $\pi_1$ is the first coordinate projection of $\RR^2$ onto $\RR$ and $\iota$ is the inclusion map of $A$ into $\RR^2$. 

To show that $q$ is a quotient map, note that $q$ is clearly surjective. Further, if $U$ is open in $\RR$, then $\pi_1^{-1}(U)$ is open in $\RR^2$, whence in $A$ we have the open set $q^{-1}(U) = A \cap \pi^{-1}(U)$. Lastly, suppose that $q^{-1}(U)$ is open in $A$, and consider $$x \in (\pi_1 \circ \iota)(q^{-1}(U)) = U.$$ Now $q^{-1}(x) \subset q^{-1}(U)$, so for all $z \in q^{-1}(x)$ there's an $\epsilon_z > 0$ such that $$q^{-1}(U) \supset B_z = B_{\epsilon_z}(z) \cap A \text{ with } B_{\epsilon_z}(z) \text{ an open set in $\RR^2$}.$$ Assuming^[I'm not convinced. For example, I'll try to show that $\pi_1$ is *not closed* (and therefore, maybe, also not open?) in the next section, so this logic seems a bit circuituous.] is open, we have that $\pi_1(B_{\epsilon_z}(z)) \supset \pi_1(\iota(q^{-1}(U))) = U$ and $\pi_1(B_{\epsilon_z}(z)) \ni x$. So $U$ is open, as desired. Because $q$ is a *strongly continuous*, surjective function, we say that $q$ is a *quotient map.*

Now to show that $q$ is neither open nor closed. To see that $q$ is not open, consider the $A$-open set $U = B_\epsilon(0 \times 1) \cap A$ where $0 < \epsilon < 1$. Then $q(U) = [0,1)$, which is not $\RR$-open. To see that $q$ is not closed, consider the closed set $$K = \left\{ (x,y) : y \le \frac{1}{1-x} \text{ and } 1 < x \le 2\right\}.$$ Its image $q(K) = \pi_1(K) = (1, 2]$ is not closed.

### Equivalence relations and quotient spaces [@Mu00, number 22.4]

(a) Define an equivalence relation $\sim$ on the plane $\RR^2$ by $$x_0 \times y_0 \sim x_1 \times y_1 \text{ iff } x_0 + y_0^2  = x_1 + y_1^2.$$

    I claim the real line $\RR$ is homeomorphic to this equivalence relation's corresponding quotient space $\RR^2/\sim$. 

    That is, the sets in $\RR^2/~$ are exactly the levels curves $x + y^2 = c$, i.e., left opening parabolas where for each $c \in \RR$ the unique parabola on the level curve has the directrix $x = c - \frac12$ and the focus $(c + 1/2, 0) \in \RR^2$. A homeomorphism is apparent---map the level curves satisfying $x + y^2 = c$ to the point $c$ on the real line.

(b) Now redefine the previous equivalence relation $\sim$ (again on the plane) by $$x_0 \times y_0 \sim x_1 \times y_1 \text{ iff } x_0^2 + y_0^2  = x_1^2  + y_1^2.$$
    
    In this case, the sets in the quotient space are the level curves $x^2 + y^2 = c$, that is, circles about the origin of radius $\sqrt{c}$. Now $\RR / \sim$ is homeomorphic to the half open ray $[0,\infty)$, where such a homeomorphic map can be obtained by mapping the level curves of radius $\sqrt{c}$ to $c \in [0, \infty)$.

### Restricting to open maps [@Mu00, number 22.5]

Suppose that $p \colon X \to Y$ is an open map. If $A$ is open in $X$, then the map $q \colon A \to p(A)$ obtained by restricting $p$ is an open map.

*Proof.* We want to show that if $U$ is open in the subspace $A$ then $q(U)$ is open in the subspace $p(A)$. So let $U$ be open in $A$. Then $U = W \cap A$ is open in $X$ (since $W$ is open in $X$ by definition of a subspace and since $A$ is open in $X$ by assumption). Then $p(W \cap A) = p(W) \cap p(A)$ is $Y$-open (its a finite intersection of open sets) and thus $q(U) = p(W \cap A)$ is $Y$-open. \qedsymbol

### Quotienting out $K$ in the $K$-topology [@Mu00, number 22.6]

Let $Y$ be the quotient space obtained from $\RR_K$ by collapsing the set $K$ to point, with $p \colon \RR_K \to Y$ as the corresponding quotient map.

(a) $Y$ is $T_1$ but not Hausdorff.
(b) The map $p \times p \colon \RR_K \times\RR_K \to Y \times Y$ is not a quotient map.^[The diagonal is not closed in $Y \times Y$, but its inverse image is closed in $\RR_K \times \RR_K$.]

*Proof.* TODO.

## References
