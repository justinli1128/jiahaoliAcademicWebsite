---
layout: default
title: Practices in of Part 1 of _Lecture Notes on Motivic Cohomology_ by C. Mazza, V. Voevodsky, and C. Weibel (updating)
---
(v.1.1.1)

[Part 1: Presheaves with Transfers]

[Lecture 1: The category of finite correspondences](#lecture-1)

## Lecture 1

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

