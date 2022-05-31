![[Pasted image 20220509083937.png]]

![[Pasted image 20220509102246.png]]

We first define two ordered sets $A$ and $B$, and two order reversing maps $\gamma$ and $\phi$, where $\gamma$ goes from $A$ to $B$ and $\phi$ goes from $B$ to $A$.

The pair $(\gamma,\phi)$ is a Galois pair if $a\le a^{\gamma\phi}$ for each element $a\in A$ and $b\le b^{\phi\gamma}$ for every element $b\in B$.

![[Pasted image 20220509104028.png]]

An element $a$ in $A$ is called galois with respect to the pair $(\gamma,\phi)$ if $a=a^{\gamma\phi}$. Obviously the same is true for the other set (though you would switch the order of $\gamma$ and $\phi$)

![[Pasted image 20220510094445.png]]

Let $\mathcal{S}$ denote the set of all subfields $S$ of $R$ s.t. $R$ is finitely generated and galois over $S$, and let $\mathcal{G}$ denote the set of all finite subgroups of $Aut(R)$.

We define $\gamma$ to be a bijective order-reversing map from $\mathcal S$ to $\mathcal G$, where $S^\gamma=Aut_S(R)$ for every element $S$ in $\mathcal S$

We also see that the map $\phi$, where $G^\phi=Fix_R(G)$ for every element $G$ in $\mathcal G$, is also a bijective order-reversing map from $\mathcal G$ to $\mathcal S$

Then $\gamma$ and $\phi$ are inverses of each other

We also see that if we have two elements each from $\mathcal S$ and $\mathcal G$, say $T$ and $U$ are elements from $\mathcal S$ and $K$ and $H$ are elements from $\mathcal G$, s.t. $T\subseteq U$ and $T^\gamma=K$ and $U^\gamma=H$.

Then we have that $|\frac{K}{H}|=\dim_T(U)$

![[Pasted image 20220510094451.png]]

The minimal polynomial of $t$ over $S$ is a single polynomial of lowest degree with coefficients from $S$, where $t$ is a root.

$S[X]$ must be a principal ideal domain.

![[Pasted image 20220510094544.png]]

For a field $T$ and a subfield S, if $T$ is finitely generated over $S$ it means that we can take some finite subset $B$ of $T$, where all elements in $T$ can be represented as a combination of elements from $S$ and $B$.

Take $\mathbb{Q}[i]$ and $\mathbb{Q}$ for example, in this case our $B$ would be $\{1,i\}$, it's clear to see that all elements in $\mathbb{Q}[i]$ can be represented as some combination of elements from $\mathbb{Q}$ and $B$

For a field $T$ to be algebraic over the subfield $S$, it means that all elements $t$ in $T$ are algebraic over $S$

For an element $t$ in $T$ to be algebraic over $S$, it means that $S$ contains elements $s_0,...,s_n$ s.t.

$s_nt^n+s_{n-1}t^{n-1}+...+s_1t+s_0=0$

A field $T$ is normal over a subfield $S$ if for every element $t$ in $T$, the minimal polynomial $\min_S(t)$ splits over $T$

A field $T$ is separable over a subfield $S$ if every element of $T$ is separable over $S$, for an element $t$ in $T$ to be separable over $S$, we mean that for a non-constant polynomial, each of its prime divisors over $S$ is multiplicity-free.

For a field $T$ to be galois over $S$, it means that

![[Pasted image 20220510094555.png]]

I think the purpose of the lectures is best summed up in theorem 10.1.

The little paragraph before prefaces that the proof of theorem 10.1 requires our knowledge from Corollary 5.4, Lemma 5.7, Lemma 7.6, Theorem 8.2, Corollary 8.3, and Theorem 9.8.

Theorem 10.1 equates to us a commutative field T being algebraic and galois over a subfield of T called S

It states that T being normal and separable over S is also the same.

And finally, that T is a splitting field over S of a set of separable polynomials over S

From theorem 10.1 (with a little work) follows Corollary 10.2 and 10.3

It feels a little bit like realizing that the derivative and integral are inverses of each other, at least to me. I had a great experience with that realization.

![[Pasted image 20220509104951.png]]

(i) 3

(ii) 4

(iii) Fields have exactly two ideals.

(iv)

(v) Transcendental

(vi) Yes

(vii) Yes