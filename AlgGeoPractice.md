---
layout: default
title: Practices in _Algebraic Geometry_ by R. Hartshorne (updating)
---

# Chapter 2: Schemes
## 2.1: Sheaves
### 2.1.1 
Let $A$ be an abelian group, and define the constant presheaf associated to $A$ on the topological space $X$ to be the presheaf $U \mapsto  A$ for all $U \neq \emptyset$, with restriction maps the identity. Show that the constant sheaf $\mathcal{A}$ defined in the text is the sheaf associated to this presheaf.

_proof:_ 

There exists $\phi: const_A\to \mathcal{A}$, by defining $a\in A\mapsto (f:U\to A, u\mapsto a)$ the constant map at $a$. We want to show that this is an isomorphism on the stalk for every $p\in X$.

   We know that for every $x\in U$, there is a connected $x\in V\subseteq U$, therefore, the restriction of the colimit $\mathrm{colim}\_{p\in U}F\cong \mathrm{colim}\_{p\in V}F$ for all connected $V$. Apply this to $\phi$, we have that this is the identity on $A$, which is the stalk for both sheaf and presheaf.

### 2.1.3
#### a)
   Show that $\varphi: \mathcal{F}\to \mathcal{G}$ is surjective iff the following holds: for every open set $U \subseteq  X$, and for every $s\in \mathcal{G}(U)$, there is a covering $\{U_i\}$ of $U$, and there are elements $t_i \in \mathcal{F}(U_i)$, such that $\varphi(t_i)=s|_{U_i}$.
   
_proof:_
    
($\impliedby$) This shows that $\varphi$ is surjective on the stalk, so $\varphi$ is surjective.

($\implies$) we have that $\varphi$ is surjective on the stalk. Let $s\in \mathcal{G}(U)$, then for every $P \in U$, $s|_P\in \mathcal{G}\_P$ has preimages $t|\_P\in \mathcal{F}\_P$. There is then an open set $U_i \subseteq U$ such that $\varphi(t|\_{U_i})=s|\_{U_i}$. Do this with all $P$.

#### b)

 Give an example of a surjective morphism of sheaves $\varphi: \mathcal{F}\to \mathcal{G}$ and an open set $U$ such that $\varphi|_U: F(U)\to G(U)$ is not surjective.

 _example:_

Let $X=\mathbb{C}$, let $F=O$ be the space of holomorphic functions and let $G=O^*$ be the space of nonvanishing holomorphic functions, $\varphi(f)=\exp(f)$. 

We see that the stalks $O_P \to O^\*_P$ is surjective, as for every nonvanishing $g\in {O^\*}\_P$, there is a small open disc $U$ such that $g(U)\subset Dom \ \ln$, the holomorphic domain of $\ln$. So this is surjective on stalk, hence surjective.

However, on $U=\mathbb{C}-{0}$, $g(z)=z$ is nonvanishing yet $\ln (z)$ is not holomorphic. 

## 2.2: Schemes
## 2.3: First Properties of Schemes
## 2.4: Separated and Proper Morphisms
## 2.5: Sheaves of Modules
## 2.6: Divisors
## 2.7: Projective Morphisms
## 2.8: Differentials
## 2.9: Formal Schemes

# Chapter 3: Cohomology

