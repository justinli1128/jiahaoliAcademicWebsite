---
layout: default
title: Practices in Chapter 2 of _Algebraic Geometry_ by R. Hartshorne (updating)
---
(v.1.1.4)

[Chapter 2: Schemes](#Chapter 2: Schemes)

[2.1: Sheaves](#21-sheaves)


[2.2: Schemes](#22-schemes)

[2.3: First Properties of Schemes](#23-first-properties-of-schemes)

[2.4: Separated and Proper Morphisms](#24-separated-and-proper-morphisms)

[2.5: Sheaves of Modules](#25-sheaves-of-Modules)


[2.6: Divisors](#26-divisors)

[2.7: Projective Morphisms](#27-projective-morphisms)

[2.8: Differentials](#28-differentials)

[2.9: Formal Schemes](#29-formal-schemes)


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
### 2.2.1
Let $A$ be a ring, let $X = \spec A$, let $f \in A$ and let$ D(f) \subseteq  X$ be the open complement of $V( (f))$. Show that the locally ringed space$ (D(f), \Oc\_X\|\_{D(f)}) $ is isomorphic to $\spec (A)\_{(f)}$ .

_proof:_

First $D(f)$ is the set of prime ideals not containing $(f)$. 

There is inclusion of algebra $i:A\to A\_f$. We have for $p\in \spec (A\_f)$, $i^{-1}(p)$ is prime, and it does not contain $f$, since $f$ is an unit in $A\_f$. So we have a continuous map 
    \\[
       i:\spec A\_f\to D(f)
    \\]

We can also define inverse map that takes $p\mapsto pA\_f$, since $A\_f/pA\_f\cong A/p$ so this is prime. And continuous since if we have $g/f^n\in A\_f$ and $V(g/f^n)\subseteq \spec (A\_f)$ is closed, then the preimage would be $V(g)$.

Not hard to see that $\spec(A\_f)\cong D(f)$ under the maps we defined. There is then morphism
    \\[
        \varphi:\Oc\_{X}\|\_{D(f)}\to i\_{\*}\Oc\_{\spec(A\_f)}
    \\] And it is isomorphic on the stalk.

### 2.2.2
Let $(X,\Oc\_X)$ be a scheme, and let $U \subseteq X $be any open subset. Show that $(U, \Oc\_X\|\_U)$ is a scheme. We call this the induced scheme structure on the open set $U$, and we refer to $(U, \Oc\_X\|\_U)$ as an open subscheme of $X$.

_proof:_

Suppose we have $p \in U \subseteq X$, there is an affine open $\spec(A)$ containing $p$ in $X$. Choose $f\in A$ so that $x\in D(f)\subseteq U\cap \spec(A)$, which always exist since $U\cap \spec(A)$ is open in $\spec(A)$. Therefore, we have an affine neighbourhood of $p$ in $U$, that is $D(f)$. Do 
this with all $p\in U$.

### 2.2.3 Reduced Schemes
$(X, \Oc\_X)$ is reduced if for every $U\subseteq X$, $\Oc\_X(U)$ has no nilpotents. 

#### a)

Show that this is equivalent to every stalk has no nilpotents

_proof:_

$\implies$ Let $a\in \Oc\_{X,p}$, we know $a=\[f, U\]$ for some $U$ and some $f\in \Oc\_X(U)$ and $(g,V)\in \[f,U\]$ iff $g\|\_{U\cap V}=f\|\_{U\cap V}$. 

Suppose $a$ is nilpotent, there is $a^n=0$ for some $n$. So $f^n\|\_{U\cap V}=0$ for some neighbourhood $V$ of $x$. $U\cap V$ is open, so $f$ cant be nilpotent, a contradiction.

$\impliedby$ Let $f\in \Oc\_X(U)$, we know that $f^n\|\_p=(f\|\_p)^n$, since $(f\|\_p)^n\neq0$, $f^n\neq 0$.

#### b)

For scheme $(X,\Oc\_X)$ define $X\_{red}:=(X, \Oc\_X^{red})$ to be the locally ring spaced where $\Oc\_X^{red}(U)$ is the reduction of $\Oc\_X(U)$ (quotient of ideal of nilpotnets). Show that $X\_{red}$ is a scheme and there is a morphism $i:X\_{red}\to X$ that is a homeomorphism on the topological space.

_proof:_

We show first $\spec(B)\_{red}\cong\spec(B^{red})$.

There is a map $\psi:\spec(B^{red})\to \spec(B)$ from the quotient $q:B\to B^{red}$. Since $0\in p$ for every $p\in \spec(B)$, nilpotents $I\subseteq p$ for every $p$. So the map is a bijection. It is continuous because if we have closed set $V(f)\subseteq \spec(B^{red})$. We have then $\psi(V(f))$ is the set of $q^{-1}(p)$ for $f\in p$. As it turns out, $\psi(V(f))=V(f+I)$, since if $f+I\subseteq p'$, then $f\in q(p)$, and $q^{-1}q(p)=p$.

Since the localization alway from some set commute with quotient, we see that $\spec(B^{red})\cong \spec(B)\_{red}$.

The rest is then trivial, finding a cover $\spec(A\_i)$ of $X$, we can easily show that $\spec(A\_i^{red})$ covers $X_{red}$

#### c)
Shows that $f:X\to Y$ for $X$ reduced factors uniquely through $Y\_{red}\to Y$

_proof:_

The underlying continuous map is easily determined uniquely.

The map $\varphi: \Oc\_Y\to f\_{\*}\Oc\_X$, is a sheaf map over $Y$. We know that ring maps takes nilpotents to nilpotents, so $\varphi$ factors through $\Oc\_Y^{red}=i\_{\*}\Oc\_{Y\_{red}}$ uniquely.

### 2.2.4 Adjunction of $\spec(-):\Ring^{op}\to \Sch: \Gamma$

For $f:X\to \spec(A)$, there is $f^{\sharp}: \Oc\_{\spec(A)}\to f\_{\*}\Oc\_X$, taking the top section we have 
\\[
    \alpha: \Hom\_{\Sch}(X,\spec(A))\to \Hom\_{\Ring}(A, \Gamma(X, \Oc\_X))
\\] Show that this is an isomorphism.

_proof:_

We start by construction a function $\beta$ of the other direction.

For a map $f^{\sharp}: A\to \Gamma(X, \Oc\_X)$, for every $p\in X$, there is a map 
    \\[ f^{\sharp}\_p: A\to \Gamma(X, \Oc\_X)\to \Oc\_{X,p}/m\_{p}\\], 

here $m\_{p}$ is the maximal ideal of $\Oc\_{X,p}$

The kernel of this map is prime, since the codomain is a field. So we have a function $g:X\to \spec(A)$ that takes $p$ to $\ker f^{\sharp}\_p$. Is it continuous?

For $r\in A$, $D(r)$ is the set of prime ideals not containing $r$, $g(p)\in D(r)$, if $\ker f^{\sharp}\_p$ not contains $r$. So $f^{\sharp}\_p(f)\notin m\_p$. Since $X$ is a scheme, $p$ is contained in some affine open $\spec(A)$, $f^{\sharp}\_p(r)\notin m\_p$ is equivalent to $f^{\sharp}(r)\mod p\neq 0$, or $f^{\sharp} (r)\notin p$ over $\spec(A)$. Internal to $\spec(A)$, we have $g^{-1}(D(r))\cap\spec(A)=D\_{\spec(A)}(f^{\sharp}(r))$. So we have that $g$ is continuous. We see that $g^{-1}(D(r))$ is the nonvanishing open set of $f^{\sharp}(r)$ in $X$ (make sense if we think $f^{\sharp}$ as precomposition.)

We define $g^{\sharp}: \Oc\_{\spec(A)}\to g\_{\*}\Oc\_X$ that takes $r'/r^n\in A\_{r}$ to $f^{\sharp}(r')/f^{\sharp}(r)^n\in\Oc\_X(U)$, here $U$ is the nonvanishing open set of $f^{\sharp}(r)$ so it makes sense. We denote the construction $\beta(f^{\sharp})$.

Obviously $\alpha\circ \beta=id$. We show that this is true in the other direction.

Assume for now $X=\spec(B)$.  A map $f: \spec(B) \to \spec(A)$, is induced by its top section $f^{\sharp}:A\to B$, from $(f^{\sharp})^{-1}$ on the primes ideals. This is equivalent to the kernel of the map 
    \begin{align*}
        A\to B\to B\_{(p)}\to B\_{(p)}/m\_p
    \end{align*} As preimage of $m_p$ in $B$ is $p$.

So for affine case, the continuous map we constructed agrees. Now for a general scheme $X$, there is an affine cover $\spec(A\_i)$. Since stalk is determined locally, we easily deduce that the continuous map $\beta\circ \alpha(f)$ agrees with that of $f$.

The case of sheaf map can also be deduced from the affine case.

For $f:\spec(B)\to \spec(A)$ associated to ring map $\varphi:A\to B$, $f^{\sharp}: \Oc\_\spec(A)\to f\_{\*}\Oc\_{\spec(B)}$ on standard opens $D(r)$ of $\spec(A)$ is just 

\\[ A\_r \to B_{\varphi(r)}\\]

Where $r'/r^n$ are map to $\varphi(r')/\varphi(r)^n$, the map we have constructed. 

The general scheme case follows.

### 2.2.9

If $X$ is a topological space, and $Z $ an irreducible closed subset of $X$, a generic point for $Z$ is a point $\xi$ such that $Z=\overline{ \{\xi\}}$. If $X$ is a scheme, show that every (nonempty) irreducible closed subset has a unique generic point. 

_proof:_

First of all, schemes are $T_0$. It suffices to show this for affines. For $p\neq q\in \spec(A)$, there is $f\in p$ and not in $q$. So $q\in D(f)$ and $p\notin D(f)$.

Let $\spec(A)$ be an affine open of $Z$. There is an ideal $I=\sqrt 0$ such that $V(I)=\spec(A)$. Since $\spec(A)$ is irreducible, $I$ is prime, since for $f, g\in A$ such that $fg\in I$, we have 
\\[ V(I)\subseteq V(fg)=V(f)\cup V(g)\\]
So $f\in I$ or $g\in I$. 

Therefore, $I$ is a generic point of $\spec(A)$. Since $Z$ is irreducible and $\spec(A)$ is open in $Z$, so $I$ is then a generic point of $Z$.

If there are two generic point $\xi$ and $\xi'$, we have $\xi\in \overline{\{\xi'\}}$ and $\xi'\in \overline{\{\xi\}}$. So any open neighbourhood of one contains the other. Since schemes are $T_0$, this implies $\xi=\xi'$.

### 2.2.17 Criterion for Affineness

#### a)

Let$ f: X\to Y$ be a morphism of schemes, and suppose that $Y$ can be covered by open subsets $U\_i$ such that for each $i$, the induced map $f^{-1}(U\_i)\to U\_i$ isomorphism. Then $f$ is an isomorphism. 

_proof:_

We have that $f$ is a homeomorphism on the underlying space. Since $f\_i^{\sharp}: \Oc\_Y\|\_{U\_i}\to f\_{\*}\Oc\_X\|\_{f^{-1}U\_i}$ is an isomorphism of sheaves and we have that any open sets $V$ in $Y$ are unions of opens of $U\_i$ similarly $f^{-1}(V)$ would be the union of those opens of $f^{-1}(U\_i)$. The gluing property tells us that the overall sheaves are isomorphic.

#### b)

A scheme $X$ is affine if and only if there is a finite set of elements $f\_i \in \Gamma(X, \Oc\_X)$ such that the open subsets $X\_{f\_i}$ are affine and $f\_i$ generate $1\in A$.

_proof:_

($\implies$) If $X$ is affine, since $X$ is quasicompact, then there are finite $f_i$ that generate $i$, and $X_{f_i}=D(f_i)$.

($\impliedby$) Denote $A=\Gamma(X,\Oc\_X)$, we want to show $X\cong \spec(A)$. There is a map $\varphi: X\to \spec(A)$ that is induced from the identity in $\beta:\Hom\_{\Ring}(A,\Gamma(X,\Oc\_X))\to \Hom\_{\Sch}(X, \spec(A))$.

We first show that $X\_{f\_i}\cong D(f\_i)$, which is natural as $X\_{f\_i}$ are affine, so top section $\Gamma(X\_{f\_i}, \Oc\_{X\_{f\_i}})\cong A\_{f\_i}$ determines $X\_{f\_i}$ entirely. 

Since $f\_i$ generate $1$, then $D(f\_i)$ covers $A\_{f\_i}$, and $\varphi^{-1}(D(f\_i))=X\_{f\_i}\to D(f\_i)$ are isomorphisms. By the previous exercise, we have $X\cong \spec(A)$.

## 2.3: First Properties of Schemes

### 2.3.6

Let $X$ be an integral scheme. Show that the local ring $\Oc\_{\xi}$ of the generic point $\xi$ of $X$ is a field. It is called the function field of $X$ and is denoted by $K(X)$. Show also that if $U = \spec (A)$ is any open affine subset of $X$, then $K(X) $is isomorphic to the quotient field of $A$. 

_proof:_

If $X$ is an integral scheme, take an affine cover $\spec(A\_i)$ of $X$. Since for every open $U$, $\Oc\_X(U)$ is integral domain, $A\_i$ are integral domain. The unique generic point of $X$ is the generic point $(0)$ of $\spec(A\_i)$. Since stalk are locally determined, we have $\Oc\_{X,(0)}=Q(A\_i)$. Here $Q(A\_i)$ is the quotient field of $A\_i$ for some $i$.    

### 2.3.9 Product of Schemes

#### a)

Let $k$ be a field, $\A^1\_k:=\spec(k\[x\])$, show that $\A^1\_k\times\_{\spec(k)}\A^1\_k\cong \A^2\_k$ and show that the underlying point set of the product is not the product of the underlying point sets of the factors (even if $k$ is algebraically closed). 

_proof:_

First of all, $\A^1\_k\times\_{\spec(k)}\A^1\_k\cong \spec(k\[x\]\otimes\_kk\[y\])\cong \spec(k\[x,y\])=\A^2\_k$.

Since we claim that for even closed $k$, this is not the product set. So let $k=\mathbb{C}$. There are points $\{p \in \mathbb{C}\}$ and generic point $\xi$ for the underlying set of $\A^1\_k$. The product is $(p,q)\in \C^2$, $(\xi, q)$, $(p,\xi)$, and $(\xi,\xi)$. But $\A^2\_k$ has $(p,q)$ and only one generic point $\eta$.

#### b)

Describe $\spec(k(s))\times\_{\spec(k)}\spec(k(t))$.

_description:_

$\spec(k(s))\times\_{\spec(k)}\spec(k(t))=\spec(k(s)\otimes\_kk(t))$. This is not a field, since $s\otimes 1-1\otimes t$ is not invertible. It is in general not a one point space. It is a integral scheme.

### 2.3.13 Properties of Morphisms of Finite Type

#### a)

A closed immersion is a morphism of finite type. 

_proof:_

Let $f:Y \to X$ be closed, choose affine cover $\spec(A\_i)$ of $X$. Since closed immersion is stable under pullback, we have $f^{-1}(\spec(A\_i))$ is a closed immersion of $\spec(A\_i)$. Hence there is ideal $I$ of $A\_i$ such that $f^{-1}(\spec(A\_i))\cong \spec(A\_i/I)$. $A\_i/I$ is finitely generated $A\_i$-algebra. Hence $f$ is of finite type.

#### b)

A quasi-compact open immersion is of finite type.

_proof:_

We simply identify an open immersion with an open set $U$ of $X$ that is a scheme. Quasicompact implies for all open affine $\spec(A)$ of $X$, $U\cap \spec(A)$ are quasicompact.

$U\cap \spec(A)$ is quasicompact implies that we just need to find an affine cover of , $U\cap \spec(A)$ so it is induced from a finitely generated $A$-algebra. We can cover $U$ by something of the form $D(f\_i)$ of $\spec(A)$, and $A\to A\_{f\_i}$ is finitely generated.

#### c)

A composition of two morphisms of finite type is of finite type. 

_proof:_

If $C$ is a finitely generated $B$-algebra, and $B$ is finitely generated $A$-algebra, then $C$ is $A$-finitely generated. Finiteness of cover is simple.

#### d)

Morphisms of finite type are stable under base extension. 

_proof:_

Let $f:Y\to X$ be finite, and $g:X'\to X$ be any map. For open affine $\spec(B)$ of $X'$, let $\spec(A\_i)$ be some affine cover of $g(\spec(B))$. It suffices to assume that $\spec(B)$ is contained entirely in one of $A$. We have that $f^{-1}(\spec(A))$ are covered by finitely many fin.gen. $A$-algebra $R$. The preimage of $\spec(B)$ in $Y\times_XX'$ then is covered by $R\otimes_{A} B$, which is $B$ fin.gen.

#### e)

If $X$ and $Y $ are schemes of finite type over $S$, then $ X \times\_S Y$ is of finite type over $S$.

_proof:_

For affine $\spec(A)$ in $S$, there are $\spec(B\_i)$ and $\spec(C\_j)$ in the $X$ and $Y$ resp. and the preimage in $X\times\_S Y$ is then $\spec(B\_i\otimes\_A C\_j)$. All are fin.gen. $A$-alg and there are finitely many of them.

### 2.3.20 Dimensions

Let $X$ be an integral scheme of finite type over a field $k$ (not necessarily
algebraically closed).

#### a)

For any closed point $P\in X$, $\dim(X)=\dim(\Oc\_{X,p})$ , where for rings, we always mean the Krull dimension.

_proof:_


#### b)

Let $K(X)$ be the function field of $X$, then $\dim(X) =\mathrm{tr.d} K(X)/k$
(transcendental degree over $k$)

_proof:_


#### c)

If $Y$ is a closed subset of $X$, then $\mathrm{codim}(Y,X) = \inf\{\dim \Oc_{X,p}\| \ p \in Y\}$.

_proof:_

#### d)

If $Y$ is a closed subset of $X$, then $\dim (Y) + \mathrm{codim}(Y,X) = \dim (X)$

_proof:_

#### e)

If $U$ is a nonempty open subset of $X$, then $\dim (U) = \dim (X)$.

_proof:_

#### f)

If $k\subseteq k'$ is a field extension, then every irreducible component of $X'= X \times\_k k'$ has dimension $= \dim X$.

_proof:_

### 2.3.22* Dimension of the Fibres of a Morphism.

Let $f:X\to Y$ be a dominant morphism (dense image) of integral schemes of finite type over a field $k$. 

#### a)
Let $Y'$ be a closed irreducible subset of Y, whose generic point $\eta$ is contained in $f(X)$. Let $Z$ be any irreducible component of $f^{-1}(Y')$ such that $\eta\in f(Z)$, show that
\\[ \mathrm{codim}(Z,X)\leq \mathrm{codim}(Y',Y)\\]

_proof:_


## 2.4: Separated and Proper Morphisms
## 2.5: Sheaves of Modules
## 2.6: Divisors
## 2.7: Projective Morphisms
## 2.8: Differentials
## 2.9: Formal Schemes
