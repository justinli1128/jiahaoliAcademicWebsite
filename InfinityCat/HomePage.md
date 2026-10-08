---
layout: default
title: Practices in of _Introduction to Infinity-Categories_ by M. Land (Updating)
---
(v.1.1)

### Exercises

#### Exercise 1

Let $h(CW)$ be the homotopy category of CW-complexes. Show that this category does not have all pushouts. More concretely, show that the diagram
\\[
*\xleftarrow{} S^1\xrightarrow{\times 2} S^1
\\]
does not admit a pushout (great example).

_proof:_

In point set $CW$, the pushout is just $*$, as $\times 2$ is surjective. However, the diagram is also equivalent to
\\[
D^1\xleftarrow{} S^1\xrightarrow{\times 2} S^1
\\] 
With pushout in point set $\mathbb{R}P^2$.

#### Exercise 3

Show that every map in $\Delta$ can be uniquely factored as a composition of $s\_i $’s followed by a composition of $d\_j $’s. Therefore, a simplicial set is equivalently described by a sequence of sets $X\_n$ equipped with face and degeneracy maps satisfying the simplicial identities.

_proof:_

Let $f:\[n\]\to \[m\]$ be a map of ordered set. We have that the map factors through $im (f)$, a composition of surjective order preserving map, and injective order preserving map. For the surjective side, we may obtain the map through a list of composition of $s\_i$'s that combine the adjacent two elements. For the injective side, we may introduce more element in between two elements. 

#### Exercise 4

 Give examples of simplicial sets where the relation of Definition 1.1.9 (i.e. $x \sim y \in X_0$ if there is $H\in X_1$ such that $d_0(H)=x$ and $d_1(H)=y$), leading to $\pi\_0^\Delta (X)$, is not symmetric and not transitive.

 _proof:_

Let $X=\Lambda^2\_1$. $0\sim 1$ but there is no $1$-simplice such that $1\sim 0$, so not symmetric. $0\sim 1$ and $1\sim 2$, but there is no $1$ -simplice such that $0\sim 2$, so not transitive. 

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

\\[
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

 
### Exercise 10
 
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

Define $f:\pi\_0^\Delta(X)\cong \pi\_0(\|X\|)$ from $x\in X\_0$ to $(x,\*)\in \|X\|$. 

Since if $x\sim y$ in $X\_0$, then there is a $\Delta\[1\]\to X$ connecting $x$ to $y$, so realization of $x$ and $y$ lies on the same connected component, so this is well defined.

We have that for every connected component of $\|X\|$, there is at least one $x\in X\_0$, so $f$ is surjective.

If we have $(x,\*)$ and $(y,\*)$ lying on the same connected component. Then there exists a zigzag of $\Delta\[1\]$ connecting them in $X$, so $x\sim y$.

### Exercise 15
Show there is pushout diagram
\begin{array}{ccc}
\coprod\_{J\_n}\partial \Delta\[n\]& \longrightarrow & \mathrm{sk}\_{n-1}(X)
\end{array}
\begin{array}{ccc}
\downarrow && \downarrow
\end{array}
\begin{array}{ccc}
\coprod\_{J\_n}\partial \Delta\[n\] & \longrightarrow & \mathrm{sk}\_{n}(X)
\end{array}
Where $J\_n$ are the nondegenerate $n$-simplices. Moreover, $\mathrm{colim}\_n\mathrm{sk}\_n(X)\cong X$.

_proof:_

The diagram above is defined through the inclusion $\coprod\_{J\_n}\partial \Delta\[n\] \to \mathrm{sk}\_{n}(X)$ and canonical $\mathrm{sk}\_{n-1}(X)\to \mathrm{sk}\_{n}(X)$. It is obvious that this is a pushout diagram.

There is a sequence $\mathrm{sk}\_n(X)\to \mathrm{sk}\_{n+1}(X)\to...\to X$, where $\mathrm{sk}\_n(X)\to \mathrm{sk}\_{n+1}(X)$ is injection. Suppose we have a $\mathrm{sk}\_n(X)\to \mathrm{sk}\_{n+1}(X)\to ... \xrightarrow{h} Y$. For every, $n$-simplice $x\in X\_n$, there is a large enough $m\geq n$ such that $x\in\mathrm{sk}\_m(X)\_n$. Hence, $h$ determines a simplicial map $f: X\to Y$. Suppose, there are two $f, g:X\to Y$, that factors $h$. Given $x\in X\_n$, $x\in \mathrm{sk}\_m(X)\_n$ for some $m$, and $f\|\_{\mathrm{sk}\_m(X)}=g\|\_{\mathrm{sk}\_m(X)}$, so $f(x)=g(x)$. Hence $f=g$.
 
### Exercise 16
Show that the following simplicial sets are not nerves of categories:

We will use the fact that a simplicial set is a nerve if it has uniques inner horn fillers.
#### i)
$\partial \Delta\[n\]$ for $n\geq 2$.

_proof:_

Obviously, $Lambda^n_j\to \partial \Delta\[n\]$ does not have filler for any $j$, so not a nerve

#### ii)
$\Lambda^n\_i$ for $n= 2$, $j=1$ and $n>2$, $0\leq j\leq n$
_proof:_

For $n=2$, $\Lambda^2\_1=I^2$, we leave this for next one. For $n>3$, there is embedding $\partial \Delta\[n-1\]\to \Lambda^n\_j$ that does not factor through $\Delta\[n-1\]$.


#### iii)

$I^n$ for $n\geq 2$

_proof:_

$I^2=\Lambda^2\_1$ has no filler, and $I^2$ embeds into $I^n$ that does not factor through $\Delta\[2\]$.

### Exercise 17

 Suppose that $X$ is a Kan complex. Show that for all $n \geq 0$, the simplicial set $\mathrm{cosk}\_n(X)$ is again a Kan complex. Prove that the canonical map $X \to \mathrm{cosk}\_n(X)$ induces a bijection
 \\[
\pi\_k(X)\to \pi\_k(\mathrm{cosk}\_n(X))
 \\]
For $k< n$, and $\pi\_k(\mathrm{cosk}\_n(X))=0$ for $k\geq n$

_proof:_

The function 
\\[
\Hom(\Delta\[k\], \mathrm{cosk}\_n(X))\to \Hom(\Lambda^k\_i, \mathrm{cosk}\_n(X))
\\]is isomorphic to 
\\[
\Hom(\mathrm{sk}\_n\Delta\[k\], X)\to \Hom(\mathrm{sk}\_n\Lambda^k\_i, X)
\\]
So we need to show that this is a surjection.

For $k<n-1$, $\mathrm{sk}\_n\Lambda^k\_i\to \mathrm{sk}\_n\Delta\[k\]$ is isomorphism to the horn inclusion $\Lambda^k\_i \to \Delta\[k\]$.

For $k>n-1$, $\mathrm{sk}\_n\Lambda^k\_i\to \mathrm{sk}\_n\Delta\[k\]$, is an isomorphism. 

The only issue is with $k=n-1$, we have the inclusion is actually $\Lambda^k\_i\to \partial \Delta\[k\]$. The fact that $K$ is a Kan complex implies for any $\Lambda^k\_i$, we may determine the $\partial \Delta\[k\]$ filling through the barycentric subdivision. 

Hence $\mathrm{cosk}\_n(X)$ is Kan.

Let $S^k$ be $k$-dimensional simplicial sphere $\Delta\[k\]/\partial \Delta\[k\]$. We have that since $\mathrm{sk}\_n$ is a left adjoint, $\mathrm{sk}\_n S^k=(\mathrm{sk}\_n \Delta\[k\])/(\mathrm{sk}\_n\partial \Delta\[k\])$. If $k<n$, then $\mathrm{sk}\_n S^k\cong S^k$, and $\mathrm{sk}\_n (S^k\times I)\cong S^k\times I$ (this is because all nondegenerate simplices here are dimension at most $k+1\leq n$). Hence, the isomorphism of the homotopy group for $k<n$ is shown.

For $k= n$, $\mathrm{sk}\_n S^k=S^n$ and $\mathrm{sk}\_n (S^k\times I)\cong S^n\cup I \cup S^n$, so $\pi\_n(\mathrm{cosk}\_n X)=0$.

For $k>n$, $\mathrm{sk}\_n S^k=*$ and $\mathrm{sk}\_n (S^k\times I)\cong *$, so $\pi\_k(\mathrm{cosk}\_n X)=0$.

### Exercise 18

Show that a natural transformation between two functors $f, g : C \to D$ induces a homotopy between $N(f ), N(g) : N(C) \to N(D)$. Use this result to show that conjugation with an element determines a self map of $BG$ which is homotopic to the identity. What does conjugation induce on $\pi\_1 (BG)$? Why does this not show that every group is abelian?
_proof:_

A natural transformation $\alpha: f\implies g$ is equivalent to a functor $H: C\times I\to D$, such that $H\|\_{C\times 0}=f$ and $H\|\_{C\times 1}=g$. The nerve is then $N(H): N(C)\times I\to N(D)$, which is a homotopy between $N(f)$ to $N(g)$.


For conjugation by $g\in G$, we have $c\_g$ takes $\*\xrightarrow{h} \*$ to $\*\xrightarrow{ghg^{-1}} \*$. There is an natural transformation, $\alpha: id\implies c\_g$, 
\begin{array}{ccc}
\*& \longrightarrow{g} & \*
\end{array}
\begin{array}{ccc}
\downarrow{h} && \downarrow{ghg^{-1}{}
\end{array}
\begin{array}{ccc}
\* & \longrightarrow{g} & \*
\end{array}
So we have $c\_g$ is homotopic to $id$.

The action of conjugation induces conjugation on $\pi_1$. Why does this not imply every group is abelian? The homotopy we constructed is not a based homotopy.

### Exercise 19
Show that the nerve of a category $C$ is 2-coskeletal, i.e., that the canonical map $N(C) \to \mathrm{cosk}\_2(N(C))$ is an isomorphism of simplicial sets.

_proof:_

The canonical map on $n$-simplices $N(C)\_n \to \mathrm{cosk}\_2(N(C))\_n$ is equivalent to the map 
\\[
\Hom(\Delta\[n\], N(C))\to \Hom(\Delta\[n\], \mathrm{cosk}\_2(N(C)))\cong \Hom(\mathrm{sk}\_2\Delta\[n\], N(C))
\\]

$\mathrm{sk}\_2\Delta\[n\]$ contains the $2$-faces, which determines composable edges. Since $\Hom(\Delta\[n\], N(C))$ is isomorphic to the length $n$-composable edges, which are uniquely determined by the sequences of $2$-composable edges, this is an isomorphism.

### Exercise 22

Let $G$ be a group and let $BG$ be the category with one object and $G$ as endomorphisms of that object. Show that $N(BG)$ has only one non-trivial homotopy group, namely $\pi\_1(N(BG))$, and that this group is canonically isomorphic to $G$.

_proof:_

First of all, by Exercise 19, we have $N(BG)\cong \mathrm{cosk}\_2N(BG)$. Then by Exercise 17, we have $\pi\_k(N(BG))=0$ for $k\geq 2$. $N(BG)$ is connected so $\pi\_0(N(BG))=0$.

For $f\in\Hom(S^1, N(BG))$, $f(*)=*$ and $f(e)=g\in G$ for $e$ the unique nondegenerate $1$-simplice, and $f$ is uniquely determined by $g$. Suppose we have a based homotopy $H: \Delta\[1\]^2/\partial \Delta\[1\]\times \Delta\[1\]\to N(BG)$, the only three nondegenerate $1$-simplices, point in the same direction, living along adjacent $2$-faces. Hence they must be equal. In order word, $\pi\_1(N(BG))=\Hom(S^1, N(BG))=G$

### Exercise 24

Consider the map $\[0\] \to \[n\]$ with image {$0$}. Show that this determines a map $0: \[0\] \to\partial \Delta\[n\]$. Calculate the simplicial homotopy sets $\pi\_i(\partial \Delta\[n\])$ for $i \geq 1$ and $n\geq 2$. Deduce that $\partial \Delta\[n\]$ is not a Kan complex.

_proof:_

A map $S^n\to \pi\_i(\partial \Delta\[n\])$ based at $0$, has to factor through $\[0\]$ because the only $n$-simplices with $\partial \Delta\[n\]=0$ is the degenerate one. Therefore $\pi\_i(\partial \Delta\[n\])=0$. If $\partial \Delta\[n\])$ is Kan then this implies $\partial \Delta\[n\])$ is contractible, so $\partial \Delta\[n\])$ is not Kan.

### Exercise 26
 Determine the homotopy category of the following simplicial sets:

We use Lemma 1.2.7 that says if $X\to Y$ induces isomorphism on $\mathrm{sk}\_2X\to \mathrm{sk}\_2Y$, then $hX\to hY$ is an isomorphism.
#### i)
$\partial \Delta\[n\]$
_proof:_

For $n>2$, $\mathrm{sk}\_2 \partial \Delta\[n\]=\mathrm{sk}\_2\Delta\[n\$. Therefore, $h\partial \Delta\[n\]\cong \[n\]$. 

For $n=2$, $\mathrm{sk}\_2 \partial \Delta\[2\]=\partial \Delta\[2\]$. There are three objects, three arrows, two of which are composable, and no $2$-simplices. Therefore, $h\partial \Delta\[2\]$ is the category of three objects, $0$, $1$, and $2$, with arrow $0\to 1$, $0\to 2$, and $1\to 2$, with $0\to 1\to 2\neq 0\to 2$. 

For $n=1$, $\partial \Delta\[1\]$ is the disjoint union of two point, so $h\partial \Delta\[1\] $ is the disjoint category of two object.

#### ii)

$\Lambda^n\_j$ for $n\geq 2$ and $0\leq j \leq n$

_proof:_

It is the category of $n+1$ objects, a $n$-composable sequence of arrows, and an arrow $0\to n$ that is different from $0\to 1\to ...\to \hat {j}\to ...\to n$.


#### iii)

$I^n$

_proof:_

$hI^n\cong \[n\]$.

### Exercise 27

Let $f : X \to Y$ be a map of simplicial sets. Prove or give a counter example to the following statements:

#### i)

If $f$ is a monomorphism, then $hX \to hY$ is fully faithful.

 _counterexamples:_

$\partial \Delta[1]\to \Delta\[1\]$ is mono, but $h\partial \Delta[1]=0\cup 1\to h\Delta\[1\]=\[1\]$ is not full.

Let $X:=\partial \Delta\[2\]/\[1\to 2\]$ and let $Y:=\Delta\[2\]/\[1\to 2\]$, so we identify the edge $1\to 2$. There is a monomorphism $X\to Y$, but $hX$ is the two object category, with two distinct arrows, yet $hY$ has only one arrow, so it is not faithful.

#### ii)

If $f$ is a degree-wise surjection, then $hX \to hY$ is surjective and full, i.e., it induces a
surjection on objects and on hom-sets.

_proof:_

see iii)

#### iii)

If $f$ induces a surjection on $0$- and $1$-simplices, then $hX \to hY$ is surjective and full.

_proof:_

Since $f$ is surjection. It obviously induces a surjection on the objects. Let $e: x\to y$ in $hY$, it corresponds to an arrow $e':x'\to y'$ in $hX$, because $e:x\to y$ corresponds to an edge $e:x\to y$ in $Y$.

### Exercise 33

Let $X$ be a simplicial set and consider the canonical map $X \to N(hX)$.

#### i)

Show that this map factors through the canonical map $X \to \mathrm{cosk}\_2(X)$.

_proof:_

We have that $X\to \mathrm{cosk}\_2(X)$ determines an isomorphism $hX\to h\mathrm{cosk}\_2(X)$. 

#### ii)

Show that the induced map $ \mathrm{cosk}\_2(X) \to N(hX)$ is an isomorphism if $X$ is isomorphic
to the nerve of a category.

_proof:_

If $X=N(C)$, then $N(hX)=X$, and we have that nerve of categories are $2$-coskeletal.

#### iii)
Show that the map $\mathrm{cosk}\_2(X) \to N(hX)$ is in general not an isomorphism. Hint: Find an
$X$ which is $2$-coskeletal, but not the nerve of a category.

_proof:_

Let $X$ be the simplicial set of $2$ copies of $\Delta\[2\]$ glued together along the $0\to 1$ and $1\to 2$. This is obviously not the nerve of category.

For $\Hom(\Delta\[n\], X)\to \Hom(\mathrm{sk}\_2(\Delta\[n\]), X)$, suppose we have $f:\mathrm{sk}\_2(\Delta\[n\])\to X$, $f$ factors through one copy of $\Delta\[2\]$. Therefore, there is a filler by $\Delta\[n\]$, hence $X$ is $2$-coskeletal.

#### iv)

Prove or disprove the following statement: The map $\mathrm{cosk}\_2(X) \to N(hX)$ is an isomorphism if and only if $X$ is isomorphic to the nerve of a category.

_counterexample:_

Let $X$ be the pushout of $\Delta\[3\]\xleftarrow{}\partial \Delta\[3\]\to \Delta\[3\]$. Its $2$-coskeleton is $\Delta\[3\]$, as $\mathrm{sk}\_2 \Delta\[n\]\to X$ lives within $\partial \Delta\[3\]$. We have then $\Delta\[3\]\to N(hX)$ is isomorphism, but $X$ is not a nerve.

### Exercise 34

Let $(V , \otimes, \mathbb{1})$ be a monoidal category. Then the functor $\Hom\_V (\mathbb{1}, −) : V \to Set$ is lax monoidal. Is it monoidal? If not: Can you find a condition on $(V , \otimes, \mathbb{1})$ which ensures that it is?

_counterexample:_

Let $V=Ab$ with the tensor product, $\mathbb{1}=\mathbb{Z}$. We have then $\Hom\_V (\mathbb{1}, −)\cong fgt$, the forgetful functor from abelian groups to sets. We have that $fgt(A\otimes B)\not\cong fgt(A)\times fgt(B)$.

A strong condition on $V$ so the functor is monoidal, if $\otimes$ is the product. 


