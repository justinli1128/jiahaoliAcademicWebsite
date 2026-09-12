---
layout: default
title: Practices in _Algebraic Geometry_ by R. Hartshorne (updating)
---
(Updating. v.3)
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

## 2.2: Schemes
## 2.3: First Properties of Schemes
## 2.4: Separated and Proper Morphisms
## 2.5: Sheaves of Modules
## 2.6: Divisors
## 2.7: Projective Morphisms
## 2.8: Differentials
## 2.9: Formal Schemes

# Chapter 3: Cohomology

