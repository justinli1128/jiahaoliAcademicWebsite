---
layout: default
title: Practices in of Part 1 of _Lecture Notes on Motivic Cohomology_ by C. Mazza, V. Voevodsky, and C. Weibel (updating)
---
(v.1.1.1)

[Part 1: Presheaves with Transfers]

[Lecture 1: The category of finite correspondences](#lecture-1)

## Lecture 1

### Notes

Some notes on the correspondences:

Fix a base scheme $S=\spec (k)$, an elementary correspondence from $X$ to $Y$ over $S$, for smooth separated connected $S$-schemes $X$ and $Y$, is a closed integral subscheme of $X\times \_S Y$ that is finite and surjective over $X$. A correspondence is a finite integral linear combination of elementary correspondences (for unconnected ones, we take the linear combination over each irreducible component).

Given morphism $f:X\to Y$ over $S$, define $\Gamma\_f$ the graph, the pullback of $f\times id: X\times\_S Y\to Y\times\_S Y$ along the relative diagonal $\Delta\_{Y/S}$. Since $Y$ is $S$-separated, $\Gamma\_f$ is a closed immersion. There is isomorphism $X\to \Gamma\_f$ determine by the projection. So it is integral, finite and surjective over $X$.  

Given two closed subschemes $W, V\subseteq X$, we define the intersection product
\\[
W\cdot V:=\sum\_{i}i(Z\_i, W, V)Z\_i
\\] for each irreducible component of $W\cap V$, here $i(Z\_i, W, V)$ is the intersection multiplicity at $Z\_i$.

For $W$ and $V$ elementary correspondence from $X$ to $Y$, we have that $W\cap V$ is proper, so the multiplicity is computed as $length\_{\Oc\_{X,\eta\_i}}(\Oc\_{X,\eta\_i}/(I\_{W,\eta\_i}+I\_{V,\eta\_i}))$.

Let $f:X\to Y$ be a morphism, let $W$ be an closed irreducible set that is finite along $p$, then $V:=f(W)$ is closed and irreducible, and $\[K(W):K(V)\]=d$ is finite. The pushforward of $W$ is then $d\cdot V$.

Suppose we have elementary correspondence $W:X\to Y$ and $V:Y\to Z$, we define the composition, $V\circ W$ as follow: we first look at $(X\times V)\cdot (W\times Z)$, and we pushforward the combination to $X\times Z$ along projection of $X\times Y\times Z\to X\times Z$.

Let $f:X\to Y$ and $g: Y\to Z$ are morphisms between connected smooth separated schemes, the intersection product of the graphs $(X\times \Gamma\_g)\cdot (\Gamma\_f\times Z)$ is a multiple of the irreducible sets, $(x, f(x), g\circ f(x))$. Using Lemma 42.62.5 of Stack Project, we see that the intersection product is just $(X\times \Gamma\_g)\cap (\Gamma\_f\times Z)$. Since the projection onto $X\times Z$ is just $\Gamma\_{g\circ f}\cong X$, and $(X\times \Gamma\_g)\cap (\Gamma\_f\times Z)\cong X$, so the multiplicity is just $1$. Hence
\\[
\Gamma\_g\circ \Gamma\_f=\Gamma\_{g\circ f}
\\]

### Exercise 1.10
If $S = \spec k$ then $Cor\_k(S,X)$ is the group of zero-cycles in $X$. If $W$ is a finite correspondence from $\A^1$ to $X$, and $s,t : \spec(k) \to \A^1$ are $k$-points, show that the zero-cycles $W \circ \Gamma\_s$ and $W \circ \Gamma\_t$ are rationally equivalent.

_proof:_

First of all, $s$ and $t$ are rationally equivalent in $\A^1$, because $\[s\]-\[t\]$ is the divisor of the regular function $f$ with zero at $s$ of order $1$ and a pole at $t$ with order $1$.

We assume $W$ is the generator of $Cor$, the general case follows easily. We have that $W \subseteq \A^1\times\_k X$ is by definition finite and surjective over $\A^1$. Hence it has dimension $1$. 

For the points, $s$ and $t$ on $\A^1$, $W \circ \Gamma\_s$ and $W \circ \Gamma\_t$ are just pullback of $W$ along respectively $s\times X$ and $t\times X$, denote $W\_s$ and $W\_t$ resp. The projection 

\\[
p:W\to \A^1
\\]
The $p^{\sharp}: K(\A^1)\to K(W)$ takes $f$ to $p^{\sharp}f$, and $W\_s$ and $W\_t$ are rationally equivalent on $W$ through $p^{\sharp}f$. Now if we project onto $X\cong S\times X$, this determines the rational equivalence of $W\_s$ and $W\_t$ by Theorem 1.4 of W. Fulton, as projection onto $X$ is proper and inclusion of $W$ is proper, and pushforward of proper morphism preserves rational equivalence.

### Exercise 1.11

#### a)
Let $x$ be a closed point on $X$, considered as a correspondence from $S = \spec(k)$ to $X$ . Show that the composition of correspondence $S \to X \to S$ is multiplication by the degree $\[\kappa(x) : k\]$, and that $X \to S \to X$ is given by $X \times x \subseteq X \times X$.

_proof:_

 The intersection product of the correspondences $T\subseteq S\times X\times S\cong X$ is just the point $x$, therefore, the pushforward onto $S\times S$, just completely determined by the degree $\[\kappa(x):k\]$.

 The intersection product of $X \to S \to X$ in $X\times S\times X\cong X\times X$ is precisely $X\times x$ because $X\to S$ is just $ X\subseteq X\times S\cong X$ itself. 


#### b)
Let $L/k$ be a finite Galois extension with Galois group $G$ and $T = \spec(L)$. Prove that $Cor\_k(T,T) \cong \mathbb{Z}\[G\]$ and that $T \to S \to T$ is $\sum\_{g\in G}(g)$. Then show that $Cor\_k(S,Y)\cong Cor\_k(T,Y)^G$ for every $Y$.

_proof:_

The scheme $T\times\_S T$ is just $\spec(L\otimes \_k L)$, we have that $L\otimes\_k L\cong \prod\_{g\in G}L$. Hence the irreducible components are determined by $L$ labeled by $g\in G$. This shows the first part.

$T \to S \to T$ is the entire $T\times T$, which has $\|G\|$ many irreducible components, hence the pushforward onto $T\times T$ is $\sum\_{g\in G}(g)$.

We have the map $f:Cor\_k(S,Y)\to Cor\_k(T,Y)$ determined by precomposition with $T\to S$. We see that for any $g\in G$, the correspondence $T\xrightarrow{g} T\to S$ is determined by the graph of the underlying morphism, which is the same for any $g$. Hence the image of $f$ is a subgroup of the $G$-invariant $Cor\_k(T,Y)$. 

Suppose $T\to Y$ is $G$-invariant, then $T\to Y$ and $T\to S\to T \to Y$ are the same, as $T\to S\to T$ is $\sum\_{g\in G} (g)$. Therefore, $T\to Y$ lies in the image of $T\to S$. 

### Exercise 1.12
If $k \subset F$ is a field extension, there is an additive functor $Cor\_k \to Cor\_F$ sending $X$ to $X\_F$. If $F$ is finite and separable over $k$, there is an additive functor $Cor\_F \to Cor\_k$ sending $U$ to $U$. These are adjoint: if $U$ is smooth over $F$ and $X$ is smooth over $k$, there is a canonical identification: $Cor\_F(U,X\_F) =Cor\_k(U,X)$.

_proof:_

