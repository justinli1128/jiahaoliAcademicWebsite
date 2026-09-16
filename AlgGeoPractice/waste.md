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
