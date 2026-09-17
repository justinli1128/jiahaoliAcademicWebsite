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

Note that $\mathcal{N}il\F\_j=0$, so it is a $X\_{red}$-module, and $H^{i}(X,F\_j)\cong H^{i}(X\_{red},\F\_j)$, since they have the same underlying space.

There is then a long exact sequence

\\[
...\to H^i(X, \mathcal{N}il^{n+1} \F)\to H^i(X, \mathcal{N}il^{n} \F)\to H^{i}(X\_{red},\mathcal{N}il\F\_j)
\to H^{i+1}(X, \mathcal{N}il^{n+1} \F)\to ...\\]

Since $X$ is noetherian, $\mathcal{N}il^{n}=0$ for big enough $n$, and since $X\_{red}$ is affine, higher cohomology vanishes. Therefore, we can deduce that

$H^i(X, \mathcal{N}il^{n} \F)=0$ for all $n$. Let $n=0$ for our case.

### 3.3.2

Let $X$ be a reduced noetherian scheme. Show that $X$ is affine if and only if each irreducible component is affine.

_proof:_

($\implies$) If $X$ is affine, then we have that each irreducible component must be affine.

($\impliedby$) Let $X=X\_1\cup X\_2\cup...\cup X\_n$ be irreducible decomposition. By assumption, $X\_i$ are affine $\spec(A\_i)$.

We show the statement inductively on $n$. 

For $n=2$, $X=X\_1\cup X\_2$. Since $X\_1\cap X\_2$ is an irreducible of affines, it is itself affine. For any quasicoherent $\F$, there is exact sequence
\\[
0\to \F\to i\_1^{\*}\F\oplus i\_2^{\*}\F\to i\_{12}^{\*}\F\to 0
\\] There is then a long exact sequence

\\[...\to H^i(X, \F)\to H^i(X\_1,\F)\oplus H^i(X\_2,\F)\to H^i(X\_1\cap X\_2,\F)\to H^{i+1}(X, \F)\to ...\\]
Since $X\_i$ and $X\_1\cap X\_2$ are all affine and noetherian, $H^i=0$. Therefore, $H^i(X,\F)=0$ for $i>0$. So affine.

Let $X=X\_1\cup...\cup X\_{n-1}\cup X\_n$, since $X\_1\cup...\cup X\_{n-1}$ is affine, and $(X\_1\cup...\cup X\_{n-1})\cap X\_n$ is irreducible of affine, so affine as well, our argument follows.

### 3.3.3
Let $A$ be a noetherian ring, and let $a$ be an ideal of $A$.

#### a)

Show that $\Gamma\_a(-)$ is a left exact functor from the category of $A$-modules
to itself. We denote its right derived functors, calculated in $\mathrm{Mod}(A)$ by $H^i\_a(-)$

_proof:_

By definition $\Gamma\_a(M)=\{m\in M: \text{there is } n, a^nm=0 \}$. For $f: M\to N$, then we have that if $m\in M$ such that $a^nm=0$ for some $n$, then $a^nf(m)=f(a^nm)=0$.

Given exact sequence
\\[
0\to M'\xrightarrow{f} M \xrightarrow{g} M"
\\]

Injectivity is trivial. If $m\in \ker g$, then there is an $m' \in M'$ such that $f(m')=m$. Since $a^nm=0$, then $f(a^nm')=0$. But $f$ is injective, so $a^nm'=0$.

#### b)
Now let $X = \spec(A)$, $Y = V(a)$. Show that for any $A$-module $M$, $H^i_a(M)\cong H^i\_Y(X, \tilde{M})$

_proof:_

Since $A$ is noetherian, we can find an injective resolution $M\to I\_{\bullet}$, which determines a flasque resolution $\tilde{M}\to \tilde{I\_{\bullet}}$. Therefore, as long as we show that $\Gamma\_a(N)\cong \Gamma\_Y(X, \tilde{N})$, then the statement follows. Note that there is isomorphism $N\cong \Gamma(X, \tilde{N})$, we just need to show that a section is annihilated by power of $a$ iff $s$ is supported on $V(a)$.

Since $A$ is noetherian, $a$ is finitely generated $(f\_1,...,f\_n)$, so $V(a)=V(f\_1)\cap ...\cap V(f\_n)$. 

Suppose, $s\in \Gamma\_Y(X, \tilde{N})$, then $s\|\_{D(f\_i)}=0$ for all $i$. Then by Lemma 1.5.3a), $f\_i^{n\_i}s=0\in \Gamma(X, \tilde{N})$. Therefore, $s\in \Gamma\_a(N)$.

On the other hand, if $s\in\Gamma\_a(N)$, then $s\|\_{D(f\_i)}=b/f\_{i}^n$ for some $b \in N$. But $f\_{i}^n s=0$ so $s\in \Gamma\_Y(X, \tilde{N})$. 

#### c)

For any $i$, show that $\Gamma\_a(H^i\_a(M))=H^i\_a(M)$.

_proof:_

Let $M\to I\_{\bullet}$ be an injective resolution. Apply $\Gamma\_a(-)$ we have cochain complex
\\[
0\to  \Gamma\_a(I\_1)\to \Gamma\_a(I\_2)\to...
\\]

Since every element in the cochain complex are annihilated by powers of $a$, then the cohomology are annihilated as well.

### 3.3.4 Cohomological Interpretation of Depth.
If $A$ is a ring, $a$ an ideal, and $M$ an $A$- module, then $depth\_a M$ is the maximum length of an $M$ -regular sequence $x\_1, ... ,x\_n$ with all $x\_i\in a$.

#### a)
Assume that $A$ is noetherian. Show that if $depth\_a M \geq 1$, then $\Gamma\_a(M)=0$, and the converse is true if $M$ is finitely generated. 

_proof:_

Since $depth\_a M\geq 1$, there exists $x\in a$ such that $x$ is not a zero divisor. If $m\in\Gamma\_a(M)$, then there is $n$ such that $a^nm=0$. But then $x^nm \in a^nm$ which is not zero for any $n$ unless $m=0$.

On the other hand, suppose $\Gamma\_a(M)=0$ and $M$ is finitedly generated.

If $depth\_a M=0$, then for every $x\in a$, there is $m\in M$ such that $xm=0$. In other words, all $x\in a$ are zero divisors. 

For noetherian ring $A$, we have that the zero divisors are $\cup_{p \in \mathrm{Ass}\_A(M)}p$, here $\mathrm{Ass}\_A(M)$ is the set of associated prime ideals of $M$. That is $\mathrm{Ann}\_A(m)$ for some $m$ that is maximal.

Since $A$ is noetherian, $ \mathrm{Ass}\_A(M)$ is finite. We have $a\subseteq \cup_{p \in \mathrm{Ass}\_A(M)}p$, so by prime avoidance, $a\subseteq p=\mathrm{Ann}\_A(m)$ for some $m\in M$.

Therefore, $am=0$ so $m\in\Gamma\_a (M)$, a contradiction.

#### b)

Show inductively, for $M$ finitely generated, that for any $n \geq 0$, the following conditions are equivalent:

i) $depth\_a M\geq n$
ii) $H^i\_a(M)=0$ for $i <n$

_proof:_

For $n=1$, this is a). 

Suppose this is true for $n-1$. 
($\implies$) Let $M$ be a module of $depth\_a M\geq n$, so there is a $x\_1,...,x\_n\in a$ that is a $M$-regular sequence, so $x\_2,...,x\_n$ is a $M/x\_1$-regular sequence, and $depth \_a M/x\_1\geq n-1$. Therefore, $H^i\_a( M/x\_1)=0$ for $i <n-1$

We have that 
\\[
0\to M\xrightarrow{x\_1}M \to M/x\_1\to 0
\\] is short exact, since $x\_1$ is not a zero divisor. 

There is then long exact sequence
\\[
0\to H^{n-1}\_a(M)\xrightarrow{x\_1}H^{n-1}\_a(M)\to H^{n-1}\_a(M/x\_1)
\\] So $x\_1$ is not a zero divisor in $H^{n-1}\_a(M)$. 

Therefore $depth\_a H^{n-1}\_a(M)\geq 1$, hence $\Gamma\_a(H^{n-1}\_a(M))=0$ by a). However, from Ex 3.3.3c), $\Gamma\_a(H^{n-1}\_a(M))=H^{n-1}\_a(M)$, so $H^{n-1}\_a(M)=0$. 

($\impliedby$)
Once again, induction on $n$. Suppose true for $n-1$.
If $H^i\_a(M)=0$ for $i <n$. We know that $M$ has at least depth $n-1$. So there is a $M$-regular sequence $x\_1,...,x\_{n-1}\in a$. Then $M/(x\_1)$ has depth $\geq n-2$. If $H^{n-2}\_a(M/(x\_1))=0$, then we have that $M/(x\_1)$ has depth $\geq n-1$, and $M$ has depth $\geq n$.

We have that $H^{n-1}\_a(M)=0$ and $H^{n-2}\_a(M)=0$, so there is 
\\[
H^{n-2}\_a(M)=0\to H^{n-2}\_a(M/(x\_1))\to H^{n-1}\_a(M)=0
\\] exact. This shows our argument.


### 3.3.6

Let $X$ be a noetherian scheme.

#### a)

Show that the sheaf $\G$ constructed in the proof of (3.6) is an injective object in the category $\mathrm{Qcoh}(X)$ of quasi-coherent sheaves on $X$. Thus $\mathrm{Qcoh}(X)$ has enough injectives.

_proof:_

Let's recall the construction of $\G$. 

Let $\F$ be a quasicoherent $X$-module$. Find a (finite, since $X$ is noetherian) affine cover $U\_i=\spec(A\_i)$ of $X$ such that $\F\|\_{U\_i}=\tilde{M\_i}$ for some $A\_i$-module $M\_i$. This always exists by construction. Find an injective $A\_i$-module $I\_i$ and embedding $M\_i\to I\_i$ for each $i$. There is then a sheaf map $\F\|\_{U\_i}\to \tilde{I\_i}$. Define $\G:=\bigoplus\_i f\_{\*}\tilde{I\_i}$ (or simply the product as $i$ is finite). There is an morphsm $\F\to \G$, which is clearly an injection.

The key is to show that $\Hom\_{\Oc\_X}(-, \G)$ is exact. First of all, we have that 
\\[\Hom\_{\Oc\_X}(-, \G)=\Hom\_{\Oc\_X}(-, \bigoplus\_i f\_{\*}\tilde{I\_i})
\cong \bigoplus\_i \Hom\_{\Oc\_X}(-, f\_{\*}\tilde{I\_i})\cong\bigoplus\_i \Hom\_{\Oc\_{U\_i}}(f^{\*}(-), \tilde{I\_i})
\\]

Since $f:U\_i\to X$ is an open immersion, $f^{-1}\mathcal{N}\cong \mathcal{N}\|\_{U\_i}$. Therefore, $f^{-1}$  is exact. Moreover, since $f^{-1}\Oc\_{X}\cong \Oc\_{U\_i}$ and $f^*=\Oc\_{U\_i}\otimes\_{f^{-1}\Oc\_{X}}f^{-1}$, so $f^{\*}$ is also exact.

Since $U\_i$ are affine, and ${I\_i}$ is an injective $A\_i$-module, $\Hom\_{\Oc\_{U\_i}}(-, \tilde{I\_i})$ is exact. 

Now, $\Hom\_{\Oc\_{U\_i}}(f^{\*}(-), \tilde{I\_i})$ is the composition of exact functors, so it is exact as well. Lastly, $\Hom\_{\Oc\_X}(-, \G)$ is the product of exact functors, it is itself exact.

Therefore, $\G$ is injective.

#### b)*

Show that any injective object of $\mathrm{Qcoh}(X)$ is flasque. 

_proof:_

We first show that for any open subset $i:U\to X$, if $\F$ is injective over $X$ then $\F\|\_{U}$ is injective $\Oc\_U$.  Suppose we have $\G\to \G'$ injection over $U$, and a map $\G\to \F\|\_{U}$, we wish to extend to a $\G'\to\F\|\_{U}$.

Suppose $\G$ and $\G'$ are coherent, then by Ex 2.5.15, there exists coherent module and injection $\G\_X\to \G'\_X$ that restrict to $\G\to \G'$, and there is a map $\G\_X\to \F$ that restrict to $\G\to \F\|\_{U}$. Thus a lift exists. 

By Ex 2.5.15e), any quasicoherent modules are union of coherent modules, so we are good. 

Let $\F\in \mathrm{Qcoh}(X)$ be an injective module. Choose an affine cover $U\_i=\spec(A\_i)$ such that $\F\|\_{U\_i}=\tilde{I\_i}$. We have that $I\_i$ must be injective from the above. Then by Lemma 3.3.3, the map between any injective module $I$ to its localization over a noetherian ring is surjective. Hence, $\F$ is flasque.

#### c)

Conclude that one can compute cohomology as the derived functors of $\Gamma(X, -)$ considered as a functor from $\mathrm{Qcoh}(X)$ to $\mathrm{Ab}$.

_proof:_

Ah Doiii.

## 3.4: \text{\v{C}}ech Cohomology

### 3.4.1

Let $f:X \to Y$ be an affine morphism of noetherian separated schemes. Show that for any quasi-coherent sheaf $\F$ on $X$, there are natural isomorphisms for all $i\geq 0$
\\[
H^{i}(X, \F)\cong H^{i}(Y, f\_{\*}\F)
\\]
_proof:_

Since $Y$ is noetherian and separated, theorem 3.4.5 says that for an ordered open cover $\mathfrak{U}$, we have 

\\[
\v{H}^i(\mathfrak{U}, \G)\xrightarrow{\cong} H^i(Y, \G)
\\] The same would follow for $X$.

Choose an ordered affine cover $\mathfrak{U}$ of $Y$, then $f^{-1}(\mathfrak{U})$ is then an affine cover of $X$, as $f$ is affine.

The \text{\v{C}}ech cochain of $f\_{\*}$ over $\mathfrak{U}$ is 
\\[
\v{C}^n(\mathfrak{U}, f\_{\*}\F)=\prod\_{i\_0\leq i\_1\leq ...\leq i\_n}f\_{\*}\F(U\_{i\_0,i\_1,...,i\_n})
\cong \prod\_{i\_0\leq i\_1\leq ...\leq i\_n}\F(f^{-}(U\_{i\_0,i\_1,...,i\_n}))
=\v{C}^n(f^{-1}\mathfrak{U}, \F)
\\]
Therefore, the cohomology are the same.

### 3.4.2

Prove Chevalley's theorem: Let $f : X \to Y $ be a finite surjective morphism of noetherian separated schemes, with $X$ affine. Then $Y$ is affine

#### a)

## 3.5: The Cohomology of Projective Space
## 3.6: Ext Groups and Sheaves
## 3.7: The Serre Duality Theorem
## 3.8: Higher Direct Images of Sheaves
## 3.9: Flat Morphisms
## 3.10: Smooth Morphisms
## 3.11: The Theorem on Formal Functions
## 3.12: The Semicontinuity Theorem
