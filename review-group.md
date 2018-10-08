---
title: Topology review group
author: Colton Grainger
date: 2018-10-05
revised:
---

## Overview

### First meeting

- 1:00p--2:00p Tues 2018-10-09
- at Daniel Moritz' office, in the MARC, MATH 175
- Everyone enrolled in MATH 6210 is welcome

## Reading material

By way of an example, Jonathan Wise ran the pillar course for Topology in 2012: <http://math.colorado.edu/~jonathan.wise/teaching/math6210-fall-2012/>.

### Outlines

From least to most verbose

- <http://www.math.uchicago.edu/~may/MISC/Topology.pdf> (J.P. May)
- <https://terrytao.wordpress.com/2009/01/30/254a-notes-8-a-quick-review-of-point-set-topology/> (Terry Tao)
- <https://pi.math.cornell.edu/~hatcher/Top/Topdownloads.html> (Allen Hatcher)
- <http://www.pdmi.ras.ru/~olegviro/topoman/> (Oleg Viro)
- <http://users.metu.edu.tr/serge/courses/422-2014/supplementary/TGeometric.pdf> (Terry Lawson)

## Topology prelim syllabus

### Point-set topology

- topological spaces
    - subspaces
    - products (and box)
    - quotients
- countability axioms
- properties of spaces
    - $T$-separation axioms
    - compact
    - connected
- canonical examples
    - spheres
    - projective spaces
    - homogeneous spaces
    - CW-complexes

### Basic algebraic topology

- foundations
    - homotopy
- canonical examples
    - simply connected spaces
    - circles and $n$-spheres
    - compact surfaces
- fundamental groups
    - functorial properties
    - deformation retractions
- Seifert-van Kampen theorem
- applications
    - Brouwer fixed-point theorem
    - fundamental theorem of algebra
    - Hairy Ball theorem
- covering spaces
    - universal covering spaces
    - lifting lemma
    - covering homotopy
    - group actions
- homology
    - singular homology
    - the Eilenberg-Steenrod axioms
    - homology group of spheres
    - the degree of a map between spheres
    - homology calculations via CW complexes
    - proof of homotopy invariance
    - proof of excision
    - universal coefficient 
    - Kunneth Theorem

## Motivation

Why have a review group? From [Goerss, Paul G. The American Mathematical Monthly 113, no. 4 (2006): 374-77. doi:10.2307/27641941.]:

> Let me explain what I mean by example. One of our basic geometric facts is that any connected, compact, orientable surface is homeomorphic to a g-holed torus and that a g-holed torus and an h-holed torus are homeomorphic if and only if g = h. Let's look back at that sentence to see exactly what we're saying. On the one hand, it's a statement you can explain in a coffeehouse, shouting over the music and the crowd, with a few simple pictures on a napkin. On the other hand, if we build up the language to make it completely precise, we need to define homeomorphic (I used the word twice), connected, compact, surface, orientable (a basic, but very tricky concept, especially in the continuous setting), and the genus of a surface (perhaps using the Euler characteristic). Then we have to prove the statement. One way is by using a triangulation (as in Massey's book), but then we'd have to develop some theory of triangulations and prove that every topological surface has a triangulation. Another way is by using handlebodies (as in Lawson's book), but now one has to develop that theory, including the quotient topology. In the end, to prove this result we need a great deal of the language and tools of basic topology.
>
>  I should point out immediately that the introductory topology course I took (which was at Tulane University, although not taught by Terry Lawson) did not prove the classification of surfaces. The course was taught from Munkres's classic text [4], and many topology books proceed along the same lines. We began with the definitions of a topology and a continuous function, went through the various types of connectedness and compactness, and then began marching through the various separation axioms. The big theorems were Urysohn's lemma and the Tychonoff theorem for an arbitrary product of compact spaces. Examples abounded, but they tended to be artificial and bizarre. Steen and Seebach's book of counterexamples became a necessary resource for late nights. As the course progressed, it became more and more abstract, developing a logical flavor. This is essentially the course that we at Northwestern have offered our undergraduates, and, upon reflection, I see why there's no riot when it gets canceled. While this is a beautiful subject---and point-set topology is a vibrant field---when compared with number theory, chaos theory, or financial mathematics, it's going to seem a bit ethereal. It lacks zip. In short, it's a tough sell. 
>
> By contrast, a compact surface is not ethereal. You can draw it. You can hold it in your hand; indeed, if you're holding a coffee cup or a donut (or a whiskey glass, for that matter) as you read this, you're holding an orientable, compact three-manifold with a connected, compact surface for boundary. If your coffee's in a styrofoam cup (you eco-criminal, you) and you set it next to a hot burner and it starts to deform, there's a homeomorphism?or maybe a homotopy equivalence if you don't get back in time. So an alternative approach to undergraduate topology presents itself: focus on geometric topology, or algebraic topology, or geometric group theory (these are all related), and let the questions from these fields drive your course. How do you classify surfaces, and why are three-manifolds so much harder? What is the fundamental group, and how do you compute with it? What's a covering space, where do they come from, and how do you classify them? (Explain the connections with Galois theory while you're at it, if you're students will sit still for it.) Why is any subgroup of a free group free? Which surfaces have nonvanishing vector fields? Which spheres? Grasp the nettle and really and truly define orientation, and talk about nonorientable surfaces and manifolds. Why can't you compute the flux across the Möbius band, even though you can build one and drag it through a bucket of soapy water? Discuss the Euler characteristic and all its implications. Compared with the Tychonoff theorem, the Lefschetz fixed point theorem is an easy theorem to sell: to the extent that any theorem can shock, this is my candidate. Who'd have thought such a crude invariant as an alternating sum of traces could tell you whether a self-map of a finite simplicial complex must have a fixed point?
>
> Now, most of us don't have a classroom full of students whom we could take from the definitions in topology to the Lefschetz fixed point theorem in a semester?in a year, maybe, but not a semester. So we'd have to scale back the ambitions, but the point remains the same: let geometry drive the topology course. We'd have to do connectedness, compactness, and much of the rest of it, but the rationale would be different and, with luck, more immediately accessible. And while we're at it, let's put together some projects for the students, send them to the board once a week, make them put it together for each other.
