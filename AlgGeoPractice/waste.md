### 2.3.22* Dimension of Fibers of a Morphism

Let $f: X\to Y$ be a dominant morphism of integral schemes of finite type over a field $k$

#### a)
Let $Y'$ be a closed irreducible subset of Y, whose generic point $\eta$ is contained in $f(X)$. Let $Z$ be any irreducible component of $f^{-1}(Y')$ such that $\eta\in f(Z)$, show that
\\[ \mathrm{codim}(Z,X)\leq \mathrm{codim}(Y',Y)\\]

_proof:_

We have that for any $p\in Z$
\\[ \mathrm{codim}(Z,X)\leq \dim \Oc\_{X, p}\\]

So let $p \in Z$ such that $f(p)=\eta$, then there is 
\\[
\varphi: \Oc\_{Y,\eta}\to \Oc\_{X, p}
\\]
Since $f$ is dominant, the map above is injective, so 
\\[ \dim(\Oc\_{Y,\eta})\geq \dim(\Oc\_{X,p})\\]

But the latter is just $\mathrm{codim}(Y',Y)$.

#### b) 

Let $e = \dim X - \dim Y$ be the relative dimension of $X$ over $Y$. For any point
$y\in f(X)$, show that every irreducible component of the fibre $X\_y$ has dimension $\leq e$.

_proof:_

Let $Z$ be an irreducible component of $X\_y$, denote the closure $E:=\overline Z$ in $X$, which is an irreducible closed set of $X$. Let $Y':=\overline{y}$, it has generic point $y$, and we have $y\in f(Z)$, then we have by a)

\\[ \mathrm{codim}(E,X)=\dim (X)-\dim (E)\leq \mathrm{codim}(Y',Y)=\dim(Y)-\dim(Y')\\] Rearranging gives us $e\leq \dim (E)-\dim (Y')$. 

Rewrite the inequality with transcendental degree
\\[e\leq \mathrm{tr.d}K(E)/k-\mathrm{tr.d}K(Y')/k\leq  \mathrm{tr.d}K(E)/K(Y')\\]

The latter inequality is of transcendental degree of tower $L/K/k$.

Note that $K(Y')=\kappa(y)$, so $\mathrm{tr.d}K(E)/K(Y')$ is just dimension of $Z$.

#### c)

Show that there is a dense open subset $U\subset X$, such that for any $y\in f(U)$, $\dim U\_y=e$.


### 2.4.10* Chow's Lemma

This result says that proper morphisms are fairly close to projective morphisms. Let $X$ be proper over a noetherian scheme $S$. Then there is a scheme $X'$ and a morphism $g: X' \to X$ such that $X'$ is projective over $S$, and there is an open dense subset $U\subseteq X$ such that $g$ induces an isomorphism of $g^{-1}(U) \to U$. Prove this result in the following steps.

#### a)

Reduce to the case $X$ irreducible.

_proof:_

Proper scheme over noetherian scheme are noetherian as well. So $X$ is covered by finite irreducible.

If the construction is defined for irreducible, we then look at the smallest of all intersection. Continue the construction until the entire $X$ is covered.

#### b)

Show that $X$ can be covered by a finite number of open subsets $U\_i$, $i = 1, . .. ,n$, each of which is quasiprojective over $S$. Let $U\_i\to P\_i$ be an open immersion of $U\_i$ into a scheme $P\_i$ which is projective over $S$.

_proof:_

Let $V\_j=\spec(A\_j)$ be affines open cover of $S$, which can be finite as $S$ is noetherian. Since $X\to S$ is proper, it is finite type, so there are finitely many $U\_{ij}=\spec(B\_{ij})$ such that $B\_{ij}$ are finitely generated $A\_j$-algebra. They will contain the generic point of $X$. 

For $i,j$, let $x\_1,...,x\_m$ be the $A\_j$-generators of $B\_{ij}$,

There is then closed immersion 

\\[
\spec(B\_{ij})\to \spec(A\_j\[x\_1,...,x\_m\])\cong \A^{m}\_{A\_j}
\\]
There is then also an open immersion
\\[
\A^{m}\_{A\_j}\to \Proj^{m}\_{\spec(A\_j)}\to  \Proj^{m}\_S
\\]

There is then a projective $P\_{ij}\to \Proj^{m}\_S\to S$, such that $U\_{ij}\to P\_{ij}$ is open immersion. 

#### c)

Let $U=\cap\_i U\_i$ and consider

\\[
f: U\to X\times\_S P\_{1}\times\_S...\times\_S P\_{n}
\\]
Let $X'$ be the closed subscheme induced on $\overline{f(U)}$. There are maps $g:X'\to X$ and $h:X'\to  P\_{1}\times\_S...\times\_S P\_{n}$ from the projections. Show that $h$ is closed immersion, so $X'$ is projective over $S$.

_proof:_

Choose let $V\_i\subseteq P\_i$ be the closure of the image of $U$, the preimage in $Z$ of $V\_i$ forms a closed cover of $Z$, so $Z\to   P\_{1}\times\_S...\times\_S P\_{n}$ is a closed set. Moreover, since $p^{-1}(V\_i)$ has the closed subscheme structure, $Z$ is a closed immersion.

#### d)

Show that $g^{-1} (U) \to U$ is an isomorphism, thus completing the proof.

_proof:_

There is one side inverse, from the inclusion $U\to X'\subseteq X\times\_SP$. We know that $U\to P\_i$ are open immersion.  
