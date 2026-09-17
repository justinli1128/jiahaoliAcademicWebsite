---
layout: default
title: Practices in Chapter 2 of _Algebraic Geometry_ by R. Hartshorne (updating)
---
(v.1.1.1)

[Chapter 3: Cohomology](#chapter-3-cohomology)

[3.1: Derived Functors](#31-derived-functors)

[3.2: Cohomology of Sheaves](#32-cohomology-of-sheaves)

[3.3: Cohomology of a Noetherian Affine Scheme](#33-cohomology-of-a-noetherian-affine-scheme)

[3.4: Cech Cohomology](#34-cech-cohomology)

[3.5: The Cohomology of Projective Space](#35-the-cohomology-of-projective-space)

[3.6: Ext Groups and Sheaves](#36-ext-groups-and-sheaves)

[3.7: The Serre Duality Theorem](#37-the-serre-duality-theorem)

[3.8: Higher Direct Images of Sheaves](#38-higher-direct-images-of-sheaves)

[3.9: Flat Morphisms](#39-flat-morphisms)

[3.10: Smooth Morphisms](#310-smooth-morphisms)

[3.11: The Theorem on Formal Functions](#311-the-theorem-on-formal-functions)

[3.12: The Semicontinuity Theorem](#312-the-semicontinuity-theorem)

# Chapter 3: Cohomology

## 3.1: Derived Functors
There are no exercises for this sections. Although I think there should be. Weibel's, Maclane's, and Rotman's books all have excellent exercises on derived functors, there are also some in Vakil's book as well (Maybe I'll make a list of them). 
## 3.2: Cohomology of Sheaves

### 3.2.1

#### a)

Let $X = \A^1$ be the affine line over an infinite field $k$. Let $P,Q$ be distinct closed points of $X$, and let $U = X - P,Q$. Show that $H^1(X,\mathbb{Z}_U)\neq 0$.

_proof:_

Here $\mathbb{Z}\_U:=i\_!\mathbb{Z}$ the extension by zero of the constant sheaf outside of $U$. There is exact sequence

\\[
0\to \mathbb{Z}\_U\to \mathbb{Z}\to i\_P(\mathbb{Z})\oplus i\_Q(\mathbb{Z})\to 0
\\]

Here $i\_P(A)$ stand for the skycraper of $A$ at $P$.

We take the cohomology to get exact sequence.

\\[
0\to H^0(X,\mathbb{Z}\_U)\to \mathbb{Z}\xrightarrow{q} H^0(X,i\_P(\mathbb{Z})\oplus i\_Q(\mathbb{Z}))=\mathbb{Z}\oplus \mathbb{Z}\to H^1(X,\mathbb{Z}\_U)\to 0
\\] 
The map $q$ takes $s\mapsto (s\|\_P, s\|\_Q)$, which is definitely not surjective.

#### b)*

More generally, let $i:Y \to X:=\A^n\_k$ be the union of $n+1$ suitably placed hyperplanes, and let $U = X - Y$. Show that $H^1(X,\mathbb{Z}\_U) \neq 0$. 

_proof:_

Once again, there exists exact sequence
\\[
0\to \mathbb{Z}\_U\to \mathbb{Z}\to \mathbb{Z}\_Y=i\_*\mathbb{Z}\to 0\\]

And there is exact sequence,

\\[ 0\to H^0(X,\mathbb{Z}\_U)\to \mathbb{Z}\xrightarrow{q} H^0(X, \mathbb{Z}\_Y)=H^0(Y, \mathbb{Z})\to H^1(X,\mathbb{Z}\_U)\to 0\\]

For $Y$ with $d$ connected components, $H^0(Y, \mathbb{Z})\cong \mathbb{Z}^d$. Choose $d\geq 2$, the case would follow.

### 3.2.2

Let $X = \Proj^1$ be the projective line over an algebraically closed field $k$. Show that the exact sequence 
\\[0\to \Oc \to \mathcal{K}\to  \mathcal{K}/\Oc \to 0
\\] of (II, Ex. 1.21d) is a flasque resolution of $\mathcal{O}$, here $\mathcal{K}$ is the constant sheaf of the function field $K(X)$. Conclude that $H^i(X, \Oc)=0$ for $i>0$.

_proof:_

Let $U$ be an open set of $X$, we have that $X$ is irreducible, then $U$ must be irreducible, and hence connected. Therefore, $\mathcal{K}(U)=K(X)$ for all opens, and therefore it is flasque. 

By Ex.2.1.21e), $\mathcal{K/O}\cong \sum\_{P\in X}i\_P(K(X)/\Oc\_{X,P})$, therefore it is flasque. 

Take the global section gives us an exact sequence
\\[
0\to \Gamma(X, \Oc)=k\to \Gamma(X, \mathcal{K})=K(X)\xrightarrow{g}\Gamma(X, \mathcal{K/O})=\bigoplus_{P\in X}K(X)/\Oc\_{X,P}\to 0
\\]

There is then cochain complex
\\[
0\to K(X)\to \bigoplus_{P\in X}K(X)/\Oc\_{X,P}\to 0 
\\] that calculate $H^i$. This immediately tells us $H^i(X, \Oc)=0$ for $i>1$. For $i=1$, we claim that $K(X)\to\bigoplus_{P\in X}K(X)/\Oc\_{X,P} $ is surjective, but this directly comes from the previous exact sequence.

### 3.2.3 Cohomology with Support

Let $X$ be a topological space, let $Y$ be a closed subset, and let $\F$ be a sheaf of abelian groups. Let $\Gamma\_Y(X, \F)$ denote the group of sections of $\F$ with support in Y. So $s\|\_U=0$ for $U\subseteq X-Y$.

#### a)

Show that $\Gamma\_Y$ is left exact functor $\mathrm{Ab}(X)\to \mathrm{Ab}$ (we denote $H^i\_Y$ the right derived functor of $\Gamma\_Y$

_proof:_

Given $f: \F\to \G$ a sheaf map, let $s\in \F(X)$ such that $s\|\_ {X-Y}=0$, then we have that 
\\[
f(s)\|\_ {X-Y}=f(s\|\_ {X-Y})=f(0)=0\\]
So $\Gamma_Y$ is a functor.

Suppose we have $0\to \F\_1\xrightarrow{f} \F\_2\xrightarrow{g} \F\_3$ exact. Then $f$ is injective and $\ker{g}=\mathrm{im} \ f$.

We know that $\Gamma$ is left exact, so $\Gamma(f)$ is injective and hence $\Gamma\_Y(f)$ is injective.

Suppose $\alpha\in\ker(g)$, there is an unique $s\in \Gamma(X, \F\_1)$ such that 
$f(s)=\alpha$. If $s$ is not compactly supported, and since $f$ is injective and thus, $f\|\_{X-Y}$ is injective. Then $f(s)\|\_{X-Y}\neq0 =\alpha\|\_{X-Y}$. So $s\in \Gamma\_Y(X,\F\_1)$.

#### b)

If $0\to \F'\xrightarrow{f} \F\xrightarrow{g} \F"\to 0$ is exact with $\F'$ flasque, then 
\\[0\to \Gamma\_Y(X, \F')\to \Gamma\_Y(X, \F)\to \Gamma\_Y(X, \F")\to 0
\\] is exact.

_proof:_

From a) we are left with showing $g$ is surjective.

We know from Ex. 2.1.16b) that $g\|\_U$ is surjective for all open $U$. Suppose we have $\alpha \in \Gamma\_Y(X,\F")$ and a $s\in \Gamma(X,\F)$ such that $\Gamma(g)(s)=\alpha$, is it supported on $Y$?

We can take the restriction of the exact sequence onto $U=X-Y$, which gives us an exact sequence
\\[
0\to \F'(U)\xrightarrow{f}\F(U)\xrightarrow{g}\F"(U)
\\]
$\alpha\|\_U=0$ so $s\|\_U\in \ker g$, which by exactness, there is $t\in \F'(U)$ such that $f(t)=s\|\_U$. 

Since $\F'$ is flasque, there is $t'\in \F'(X)$ that lifts $t$.

We then have $s$ and $f(t')$ that both live over the entire $X$ in $\F$. 

Let $u=s-f(t')$, we have that $g(u)=g(s)-g(f(t'))=g(s)=\alpha$, and $u\|\_{U}=s\|\_U-f(t')\|\_U=s\|\_U-f(t)=0$. Hence $u\in \Gamma\_Y(X,\F)$ and $g(u)=\alpha$.

#### c)

Show that if $\F$ is flasque, then $H^i\_Y(X,\F)=0$ for all $i>0$

_proof:_

Let $0\to \F\to \F\to 0$ be the exact sequence associated with the identity of $\F$. This is then a flasque resolution. Take $\Gamma\_Y$, we then have 
\\[
0\to \Gamma\_Y(X, \F)\to \Gamma\_Y(X, \F)\to 0
\\] is exact. Hence $H^i\_Y=0$ for $i>0$.

#### d)

If $\F$ is flasque, show that the sequence 
\\[
0\to \Gamma\_Y(X, \F)\xrightarrow{i} \Gamma(X, \F)\xrightarrow{res} \Gamma(X-Y, \F)\to 0\\]

is exact.

_proof:_

Since $i$ is inclusion, it is injective. Since $\F$ is flasque, $res$ is surjective. So we just need $c= \mathrm{im} \ i$

If $s\in \mathrm{im}\ i$, then $res(s)=0$ by definition. If $s\in \ker res$, then $s$ is supported on $Y$, hence $s\in \mathrm{im} \ i$.

#### e)

Let $U=X-Y$, show that for any $\F$ there is exact sequence
\\[
0\to H^0\_Y(X, \F)\to H^0(X, \F)\to H^0(U, \F)\to H^1\_Y(X, \F)\to H^1(X, \F)\to H^1(U, \F)\to ...\\]

_proof:_

Let $\F\to \G\_{\bullet}$ be some flasque resolution, $i\_{\*}\F\to i\_{\*}\G\_{\bullet}$ is then a flasque resolution of $i\_{\*}\F$. 

There is then exact

\\[ 0\to \Gamma\_{Y}(X,  \G\_{\bullet})\to \Gamma(X,  \G\_{\bullet})\to \Gamma(X, i\_{\*}\G\_{\bullet})= \Gamma(U, \G\_{\bullet})\to 0\\]

Which determines exactly the long exact sequence we want.

#### f) Excision

Let $V$ be an open subset of $X$ containing $Y$. Then there are natural functorial isomorphisms, for all $i$ and $\F$,

\\[
H^i\_Y(X, \F)\cong H^i\_Y(V, \F\|\_V)
\\]

_proof:_

For any flasque resolution $\F\to \G\_{\bullet}$, there is flasque resolution $i\_{\*}\F\to i\_{\*}\G\_{\bullet}$. 

There is then natural isomorphism of cochain complex $\Gamma\_Y(X, \G\_{\bullet})\to \Gamma\_Y(V, \G\_{\bullet})$ as $Y\subset V$. This then induces isomorphism on the cohomology.

### 3.2.4 Mayer-Vietoris Sequence

 Let $Y\_1, Y\_2$ be two closed subsets of $X$. Then there is a long exact sequence of cohomology with supports

\\[
...\to H^i\_{Y\_1\cap Y\_2}(X, \F)\to H^i\_{Y\_1}(X, \F)\oplus H^i\_{Y\_2}(X, \F)
\to H^i\_{Y\_1\cup Y\_2}(X, \F)\to H^{i+1}\_{Y\_1\cap Y\_2}(X, \F)\to  ...\\]

_proof:_

Let $\F\to \G\_{\bullet}$ be a flasque resolution. 

For each $i$, there is sequence
\\[
0\to \Gamma\_{Y\_1\cap Y\_2}(X, \G\_i)\xrightarrow{i\_1\oplus i\_2}\Gamma\_{Y\_1}(X, \G\_i)\oplus\Gamma\_{Y\_2}(X, \G\_i)\xrightarrow{(s,t)\mapsto s-t} \Gamma\_{Y\_1\cup Y\_2}(X, \G\_i)\to 0
\\]

We want to show that this is exact. 

$i\_1\oplus i\_2$ is injective by construction. 

For $\alpha\in \Gamma\_{Y\_1\cup Y\_2}(X, \G\_i)$, we have $\alpha\|\_{X-Y\_2}$ and $-\alpha\|\_{X-Y\_1}$. For each $j=1,2$, there is a $s\_j\in \Gamma(X, \G\_i)$ supported on $Y\_j$ that is a lift of local sections defined, similar to that in Ex.3.2.3b). So $\alpha=s\_i-s\_j$.

Now for the middle. Obviously $\mathrm{im}\  i\_1\oplus i\_2 \subseteq \ker g$, since $s-s=0$. If $(s,t)\in \ker g$, then $s-t=0$ everywhere, Yet $(s-t)\|\_{X-Y\_1}=-t\|\_{X-Y\_1}$ and $(s-t)\|\_{X-Y\_2}=s\|\_{X-Y\_2}$. So $s$ and $t$ are supported on $Y\_1\cap Y\_2$. 

We are done.


## 3.3: Cohomology of a Noetherian Affine Scheme

### 3.3.1 

Let $X$ be a noetherian scheme. Show that $X$ is affine if and only if $X\_{red}$ is affine.

_proof:_

If $X$ is affine, then $X\_{red}$ is obvious affine. 

Now if $X\_{red}$ is affine. Denote $i: X\_{red}\to X$. Let $\mathcal{N}il$ be the sheaf of nilpotents of $X$. Given a $\F$ quasicoherent over $X$, there is then a filtration $\mathcal{N}il^n \F\subseteq \F$. Denote $\F\_j:=\mathcal{N}il^n \F/\mathcal{N}il^{n+1} \F$. This is then quasicoherent as well. 

Note that $\mathcal{N}il\F\_j=0$, so it is a $X\_{red}$-module, and $H^{i}(X,\mathcal{N}il\F\_j)\cong H^{i}(X\_{red},\mathcal{N}il\F\_j)$, since they have the same underlying space.

There is then a long exact sequence

\\[
...\to H^i(X, \mathcal{N}il^{n+1} \F)\to H^i(X, \mathcal{N}il^{n} \F)\to H^{i}(X\_{red},\mathcal{N}il\F\_j)
\to H^{i+1}(X, \mathcal{N}il^{n+1} \F)\to ...\\]

Since $X$ is noetherian, $\mathcal{N}il^{n}=0$ for big enough $n$, and since $X\_{red}$ is affine, higher cohomology vanishes. Therefore, we can deduce that

$H^i(X, \mathcal{N}il^{n} \F)=0$ for all $n$. Let $n=0$ for our case.

## 3.4: Cech Cohomology
## 3.5: The Cohomology of Projective Space
## 3.6: Ext Groups and Sheaves
## 3.7: The Serre Duality Theorem
## 3.8: Higher Direct Images of Sheaves
## 3.9: Flat Morphisms
## 3.10: Smooth Morphisms
## 3.11: The Theorem on Formal Functions
## 3.12: The Semicontinuity Theorem
