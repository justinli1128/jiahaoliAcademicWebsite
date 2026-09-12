---
layout: default
title: Practices in _Algebraic Geometry_ by R. Hartshorne (updating)
---
(Updating. v.4)
[Chapter 2: Schemes](# Chapter 2: Schemes)
[2.1: Sheaves](# 2.1 Sheaves)
[2.2: Schemes](# 2.2 Schemes)
[2.3: First Properties of Schemes](# 2.3: First Properties of Schemes) 

# Chapter 2: Schemes
## 2.1: Sheaves
### 2.1.1 
Let $A$ be an abelian group, and define the constant presheaf associated to $A$ on the topological space $X$ to be the presheaf $U \mapsto  A$ for all $U \neq \emptyset$, with restriction maps the identity. Show that the constant sheaf $\mathcal{A}$ defined in the text is the sheaf associated to this presheaf.

_proof:_ 

There exists $\phi: const_A\to \mathcal{A}$, by defining $a\in A\mapsto (f:U\to A, u\mapsto a)$ the constant map at $a$. We want to show that this is an isomorphism on the stalk for every $p\in X$.

   We know that for every $x\in U$, there is a connected $x\in V\subseteq U$, therefore, the restriction of the colimit $\mathrm{colim}\_{p\in U}F\cong \mathrm{colim}\_{p\in V}F$ for all connected $V$. Apply this to $\phi$, we have that this is the identity on $A$, which is the stalk for both sheaf and presheaf.

### 2.1.3
#### a)
   Show that $\varphi: \mathcal{F}\to \mathcal{G}$ is surjective iff the following holds: for every open set $U \subseteq  X$, and for every $s\in \mathcal{G}(U)$, there is a covering $\{U\_i\}$ of $U$, and there are elements $t\_i \in \mathcal{F}(U\_i)$, such that $\varphi(t\_i)=s|\_{U\_i}$.
   
_proof:_
    
($\impliedby$) This shows that $\varphi$ is surjective on the stalk, so $\varphi$ is surjective.

($\implies$) we have that $\varphi$ is surjective on the stalk. Let $s\in \mathcal{G}(U)$, then for every $P \in U$, $s\|\_P\in \mathcal{G}\_P$ has preimages $t\|\_P\in \mathcal{F}\_P$. There is then an open set $U\_i \subseteq U$ such that $\varphi(t\|\_{U\_i})=s\|\_{U\_i}$. Do this with all $P$.

#### b)

 Give an example of a surjective morphism of sheaves $\varphi: \mathcal{F}\to \mathcal{G}$ and an open set $U$ such that $\varphi\|\_U: \mathcal{F}(U)\to \mathcal{G}(U)$ is not surjective.

 _example:_

Let $X=\mathbb{C}$, let $\mathcal{F=O}$ be the space of holomorphic functions and let $\mathcal{G=O}^{\*}$ be the space of nonvanishing holomorphic functions, $\varphi(f)=\exp(f)$. 

We see that the stalks $\mathcal{O}\_P \to \mathcal{O}^{\*}\_P$ is surjective, as for every nonvanishing $g\in {\mathcal{O}^{\*}}\_P$, there is a small open disc $U$ such that $g(U)\subset Dom \ \ln$, the holomorphic domain of $\ln$. So this is surjective on stalk, hence surjective.

However, on $U=\mathbb{C}-{0}$, $g(z)=z$ is nonvanishing yet $\ln (z)$ is not holomorphic. 

### 2.1.15
Let $\mathcal{F}$ and $\mathcal{G}$ be sheaves of abelian groups over $X$. For every $U\subseteq X$ show that the set $\Hom(\F\|\_U,\G\|\_U)$ of morphisms of the restricted sheaves has a natural structure of abelian group. Show that the presheaf $U\mapsto \Hom(\F\|\_U,\G\|\_U)$ is a sheaf. This is the Hom sheaf $\HomSh(\F, \G)$

_proof:_

For every $U \subseteq X$, define addition on $\psi, \phi\in\Hom(\F\|\_U,\G\|\_U)$ to be $(\psi+\phi)(V):=\psi(V)+\phi(V)$. Since the restriction maps are abelian group morphism, this is well defined. 

Given $U$ and $V$ open, and $\phi\|\_U\in \Hom(\F\|\_U,\G\|\_U)$ and $\phi\|\_V\in \Hom(\F\|\_V,\G\|\_V)$, such that $\phi\|\_{U}\|\_V=\phi\|\_V\|\_U$. We define $\phi\in \Hom(\F\|\_{U\cup V},\G\|\_{U\cup V})$ to be for $W\subseteq U\cup V$ as following
        \\[\phi(W): \F(W)\to \G(W)\\ a\mapsto \phi\|\_{U\cap W}(a) \cup \phi\|\_{V\cap W}(a)\\]
        
Here $\phi\|\_{U\cap W}(a) \cup \phi\|\_{V\cap W}(a)$ is the section glued from $\phi\|\_{U\cap W}(a)\in \G(U\cap W)$ and $\phi\|\_{V\cap W}(a)\in \G(V\cap W)$, which is doable because $\phi\|\_U\|\_V=\phi\|\_V\|\_U$.

Since restriction and gluing commutes, this defines us a morphism of sheaf $\phi: \F(U\cup V)\to \G(U\cup V)$. It is easy to see that the gluing of patches of morphism gives the original morphism.
    
### 2.1.21 Examples of Sheaves on Varieties
 Let $X$ be some variety over $k$ closed, $\Oc\_X$ is the sheaf of regular functions 
 
#### a)
 
 Let $Y$ be a closed subset of $X$. For each open set $U \subseteq X$, let $I\_Y(U)$ be the ideal in the ring $\Oc\_X(U)$ consisting of those regular functions which vanish on $Y$. Show $I\_Y$ is a sheaf, the ideal sheaf

_proof:_

Suppose $f\|\_U\in I\_Y(U)$ and $f\|\_V\in I\_Y(V)$ that agrees on $U\cap V$, let $f\in \Oc\_X(U\cup V)$ be the glued section, since $f(Y\cap U)=0$ and $f(Y\cap V)=0$, then $f(Y\cap (U\cup V))=0$, so $f\in I\_Y(U\cup V)$. The uniqueness follows easily.

#### b)

If $Y$ is a subvariety, then the quotient sheaf $\Oc\_X/I\_Y$ is isomorphic to $i\_*\Oc\_Y$, where $i: Y\to X$ is the inclusion.

_proof:_

For $U\subseteq X$, $i\_{\*}\Oc\_Y(U)=\Oc\_Y(i^{-1}(U))=\Oc\_{Y}(Y\cap U)$. 

There is map
        \\[
            \varphi: \Oc\_X\to i\_{\*}\Oc\_Y
        \\] induced from precomposition of the inclusion, we see that $f\in \ker \varphi(U)$ iff $f$ vanishes on $Y\cap U$, so $f\in I\_Y$. Since kernels are determined on the opensets, we have $\varphi$ determines the isomorphism we claimed.

#### c)

Let $X=\Proj^1$ and let $Y=\{P,Q\}$ for $P\neq  Q\in X$. There is then $\F=i\_{\*}\Oc\_P\oplus i\_{\*}\Oc\_Q$ and 
    \\[
        0\to I\_Y\to \Oc\_X\to \F\to 0
    \\] is exact. Show, however, the section map $\Gamma(X, \Oc\_X)\to\Gamma(X, \F)$ is not surjective. (Leaves room for derived functors)

_proof:_

$\Gamma(X, \Oc\_X)\cong k$, the constant functions. Yet $\Gamma(X, \F)\cong\Oc\_P\oplus \Oc\_Q$, clearly not surjective.
    
#### d)

Let $X=\Proj^1$ and let $\G$ be the constant sheaf associated to the function field $K(X)$. Show that there is an injection $\Oc\_X\to \G$. Show that the quotient sheaf $\G/ \Oc\_X$ is isomorphic to the direct sum of sheaves $\bigoplus\_{P\in X}i\_P(I\_P)$ where $I\_P:=K(X)/\Oc\_P$ and $i\_P$ defines the skyscraper at $P$.  

_proof:_

Define $\varphi: \Oc\_X\to \G$ on $U$ to be 
        \\[
            \varphi\|\_U: \Oc\_X(U)\to \G(U)
            \\ f\mapsto const\_f
    \\] The constant function at $f$. This is obviously a sheaf morphism and injective. 

There is also $\psi:\G\to \bigoplus\_{P\in X}i\_P(I\_P)$ defined on connected $U$ $\psi(U)$ as $f\in K(X)\mapsto \sum\_{P\in U} f \mod{\Oc\_P}$. This makes sense because $f\mod \Oc\_P=0$ iff $f\in \Oc\_P$ a regular function at $P$, so $f$ is nonzero on $I\_P$ iff it has a pole at $P$. But there are only finitely many poles to a rational function on $\Proj^1$, hence this makes sense.
    On the stalk, this is $f\in K(X)\mapsto f\mod \Oc\_P$. So it is surjective. There is sequence 
    \\[ 0\to \Oc\_X\to \G\to \bigoplus\_{P\in X}i\_P(I\_P)\to 0\\]

The $\ker \psi\_P$ is the just $\Oc\_P$, so the sequence is exact on stalks. Hence the sequence is exact.


## 2.2: Schemes
## 2.3: First Properties of Schemes
## 2.4: Separated and Proper Morphisms
## 2.5: Sheaves of Modules
## 2.6: Divisors
## 2.7: Projective Morphisms
## 2.8: Differentials
## 2.9: Formal Schemes

# Chapter 3: Cohomology

