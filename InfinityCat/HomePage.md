---
layout: default
title: Practices in of _Introduction to Infinity-Categories_ by M. Land (Updating)
---
(v.1.1)

### Exercises

#### Exercise 1

Let $h(CW)$ be the homotopy category of CW-complexes. Show that this category does not have all pushouts. More concretely, show that the diagram
\\[
*\xleftarrow S^1\xrightarrow{\times 2} S^1
\\]
does not admit a pushout (great example).

_proof:_

In point set $CW$, the pushout is just $*$, as $\times 2$ is surjective. However, the diagram is also equivalent to
\\[
D^1\xleftarrow S^1\xrightarrow{\times 2} S^1
\\] 
With pushout in point set $\mathbb{R}P^2$.

#### Exercise 2
Verifying simplicial identities (skipped)

#### Exercise 3

Show that every map in $\Delta$ can be uniquely factored as a composition of $s\_i $’s followed by a composition of $d\_j $’s. Therefore, a simplicial set is equivalently described by a sequence of sets $X\_n$ equipped with face and degeneracy maps satisfying the simplicial identities.

_proof:_

Let $f:\[n\]\to \[m\]$ be a map of ordered set. We have that the map factors through $im (f)$, a composition of surjective order preserving map, and injective order preserving map. For the surjective side, we may obtain the map through a list of composition of $s\_i$'s that combine the adjacent two elements. For the injective side, we may introduce more element in between two elements. 

#### Exercise 4

 Give examples of simplicial sets where the relation of Definition 1.1.9 (i.e. $x ~ y \in X_0$ if there is $H\in X_1$ such that $d_0(H)=x$ and $d_1(H)=y$), leading to $\pi\_0^\Delta (X)$, is not symmetric and not transitive.

 _proof:_

Let $X=\Lambda^2\_1$. $0~1$ but there is no $1$-simplice such that $1~0$, so not symmetric. $0~ 1$ and $1~2$, but there is no $1$ -simplice such that $0~2$, so not transitive. 

#### Exercise 5

Show that every simplex $x \in X\_m$ is of the form $\alpha\_*(y)$ for a surjection $\alpha : \[m\] \to \[n\]$ and a non-degenerate $n$-simplex $y$, and show that the pair $(\alpha, y)$ is uniquely determined by $x$ (another classic result).

_proof:_

First of all, if there is no such $y$ for $n< m$, then $x$ is nondegenerate. So it remains to show the uniqueness.

Suppose we have another $(\beta, y')$ for some $\beta:\[m\]\to \[n'\]$ surjection. Suppose that $n'\geq n$, then there is a surjection $f: \[n'\]\to\[n\]$ such that $f\circ \beta =\alpha$. There is another map $g:\[n'\]\to \[m\]$ such that $\beta\circ g= id$. Hence 
\\[
X(f)(y)=X(g)X(\alpha)(y)=X(g)(x)=X(g)X(\beta)(y')=y'
\\] Hence $y'$ is either nondegenerate, or $n'=n$, but this implies $f=id$.

#### Exercise 6

Show that the category $Set$ is bicomplete (skipped, too well known).

#### Exercise 7

Let $F : I \to C$ be a functor. Show that a colimit of $F$ can equivalently be described as an initial cocone over $F$, and that a limit of $F$ can be equivalently described as a terminal cone over $F$.

_proof:_

Showing the colimit case suffices. Suppose $F^{\triangleright}$ be the initial cocone, then any other cocone $G$, such that $G\|\_{I}=F$, there exists an unique morphism $F^{\triangleright}\to G$, which corresponds to an unique map that determines the universal property of colimit.

#### Exercise 8

Calculate the limit and colimit of a simplicial set $X : \Delta^{op}\to Set$.

_proof:_

The computation using equalizer and coequalizer come in handy. We have that the limit will be the elements that are equal in $X_0$ under all morphisms, hence $X\_0$. The colimits is the equivalent classes of elements that share vertices, hence the connected components.





