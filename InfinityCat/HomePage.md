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

#### Exercise 7

Let $F : I \to C$ be a functor. Show that a colimit of $F$ can equivalently be described as an initial cocone over $F$, and that a limit of $F$ can be equivalently described as a terminal cone over $F$.

_proof:_

Showing the colimit case suffices. Suppose $F^{\triangleright}$ be the initial cocone, then any other cocone $G$, such that $G\|\_{I}=F$, there exists an unique morphism $F^{\triangleright}\to G$, which corresponds to an unique map that determines the universal property of colimit.

#### Exercise 8

Calculate the limit and colimit of a simplicial set $X : \Delta^{op}\to Set$.

_proof:_

The computation using equalizer and coequalizer come in handy. We have that the limit will be the elements that are equal in $X_0$ under all morphisms, hence $X\_0$. The colimits is the equivalent classes of elements that share vertices, hence the connected components.


### Exercise 9

Show that the datum of an adjunction in the sense of Definition 1.1.17(natural isomorphism $\alpha: \Hom(F(-), -)\to \Hom(-,G(-))$) is equivalent to the datum of a pair of functors $(F,G)$ together with natural transformations $\epsilon : F \circ G \to id$ and $\eta : id \to G\circ F $ satisfying the triangle identities, i.e., the obvious composites
\\[
F\xrightarrow{F\eta } FGF\xrightarrow{\epsilon F} F
\\]
\\]
G\xrightarrow{\eta G} GFG\xrightarrow{G\epsilon } G
\\] are the identities

_proof:_

Suppose we have the natural transformations, then 
\\[
\Hom(F(-),-)\xrightarrow{G} \Hom(GF(-), G(-))\xrightarrow{\eta^{\*}}\Hom(-,G(-))
\\] and
\\[
\Hom(-,G(-))\xrightarrow{F} \Hom(F(-), FG(-))\xrightarrow{\epsilon\_{\*}}\Hom(F(-),-)
\\]
are inverses to each other.


$\alpha$ determines than natural isomorphisms,
\\[
\alpha\_{FG}: \Hom(FG(-), -)\to \Hom(G(-),G(-))
\\] and 
\\[
\alpha\_{GF}: \Hom(F(-), F(-))\to \Hom(-,GF(-))
\\]
Therefore, we have the identity of $F$ and $G$ resp. determines natural transformation $\epsilon : F \circ G \to id$ and $\eta : id \to G\circ F $. 

\\[
 \Hom(F(-), F(-))\xrightarrow{F\alpha\_{GF}} \Hom(F(-),FGF(-))\xrightarrow{\epsilon F\_{\*}} \Hom(F(-), F(-))
 \\] 
 Takes $id:F(X)\to F(X)$ to $\epsilon F\circ F\eta=\epsilon F\circ \alpha\_{GF}(id\_{Fx})=\alpha_{GF}^{-1}(\alpha\_{GF}(id\_{Fx}))=id\_{Fx}$ 
 
 #### Exercise 10
 
 Show that $F:C\to D$ admits a right adjoint iff there is $G: D\to C$ such that for each $y\in D$, we have a morphism $\epsilon\_y: FGy\to y$ such that for any $x\in C$, there is a bijection
 \\[
 \Hom(x, Gy)\xrightarrow{F}\Hom(Fx, FGy)\xrightarrow{\epsilon\_y \circ}\Hom(Fx, y)
 \\]
_proof:_

If $G$ is a right adjoint, then Exercise 9 suffice. So we prove the other way.

We see that the bijection is the same as for any $x\in C$, and map $f:Fx\to y$, then it factors through $FGy$ uniquely via a map $x\to Gy$.

Suppose, $y'\to y$ is a morphism, then $FGy'\to y'\to y$ factors through $FGy$ uniquely with $Gy' \to Gy$, since it is determined by a bijection, it comes from $y'\to y$. 

Hence $\epsilon$ is actually a natural transformation. Then it is just definition of adjunction.

### Exercise 11

Prove that if a simplicial set $X$ has at most $n$-dimensional non-degenerate simplices, and $Y$ has at most $m$-dimensional non-degenerate simplices, then their product $X \times Y$ has at most $(n + m)$-dimensional non-degenerate simplices.
 
 _proof:_
 
 For $(x,y)\in (X\times Y)\_{n+m+1}$, we have $x\in X\_{n+m+1}$ and $y\in Y\_{n+m+1}$. Let $(\alpha, x')$ and $(\beta, y')$ be the uniqe nondegenerate simplice for respectively $x$ and $y$. Since $\|x\|\leq n$ and $\|y\|\leq m$, then there exists $k\leq n+m$, a surjection $\[n+m+1\]\to \[k\]$, and surjection $\alpha':\[k\]\to \[\|x\|\]$ and $\beta'$ such that $\alpha=\alpha'\circ f$ and $\beta=\beta'\circ f$. Hence $(x,y)$ is degenerate.
 
### Exercise 12

Show that for every simplicial set $X$, there is a canonical bijection $\pi\_0^\Delta(X)\cong \pi\_0(\|X\|)$

_proof:_

Define $f:\pi\_0^\Delta(X)\cong \pi\_0(\|X\|)$ from $x\in X\_0$ to $(x,*)\in \|X\|$. 

Since if $x~ y$ in $X\_0$, then there is a $\Delta\[1\]\to X$ connecting $x$ to $y$, so realization of $x$ and $y$ lies on the same connected component, so this is well defined.

We have that for every connected component of $\|X\|$, there is at least one $x\in X\_0$, so $f$ is surjective.

If we have $(x,*)$ and $(y,*)$ lying on the same connected component. Then there exists a zigzag of $\Delta[1]$ connecting them in $X$, so $x~y$.

### Exercise 15
Show there is pushout diagram
\begin{array}{ccc}
\coprod\_{J\_n}\partial \Delta\[n\]& \longrightarrow & \mathrm{sk}\_{n-1}(X)
\end{array}{ccc}
\begin{array}{ccc}
\downarrow && \downarrow
\end{array}{ccc}
\begin{array}{ccc}
\coprod\_{J\_n}\partial \Delta\[n\] & \longrightarrow & \mathrm{sk}\_{n}(X)
\end{array}{ccc}
Where $J\_n$ are the nondegenerate $n$-simplices. Moreover, $\mathrm{colim}\_n\mathrm{sk}\_n(X)\cong X$.
 
 
 




