
![[Pasted image 20220309142743.png]]
## Question 1

A group refers to a set of numbers and an operation on that set of numbers, either addition or multiplication.

The criteria for a set of numbers to be a group on addition or multiplication is:

1. Associativity
2. Neutral element
3. Inverse for all values

---

Let's take addition as our operation:

Associativity for addition means that $a+(b+c)=(a+b)+c$ for $a,b,c\in S$ where $S$ is our set of numbers.

There must be an element $n\in S$ s.t. $a+n=a$ for any element $a\in S$. $n$ is called the neutral element

For all values $a$, there must be a value $b$ s.t. $a+b=n$ where $n$ is the neutral element.

---

Now for multiplication:

Associativity for addition means that $a(bc)=(ab)c$ for $a,b,c\in S$ where $S$ is our set of numbers.

There must be an element $n\in S$ s.t. $an=a$ for any element $a\in S$. $n$ is called the neutral element

For all values $a$, there must be a value $b$ s.t. $ab=n$ where $n$ is the neutral element.

## Question 2

A commutative ring has 4 requirements

1. Group under addition
2. Monoid under multiplication
3. Multiplication is commutative
4. Distributivity

As we've defined a group under addition in question 1, it remains to explain what a monoid under multiplication is.

A monoid under multiplication has two requirements

1. Associativity
2. Neutral element

Associativity here means that for any three elements $a,b,c\in S$ where $S$ is our set of numbers, $a(bc)=(ab)c$

Neutral element is the same, where there is an element $a,n\in S$ s.t. $an=a$

For multiplication to be commutative, you check that if you have $a,b\in S$, $ab=ba$

Finally, distributivity simply means that $a(b+c)=ab+ac$ for any $a,b,c\in S$

If all of these criteria are satisfied, then you have a commutative ring

## Question 3

A field is a set $S$ that is a group under both addition and multiplication, with the exception of $0$ for the multiplicative group as $0$ has no inverse.

## Question 4

Let $Y$ and $Z$ be ordered sets.

We say that a map $\gamma$ from $Y$ to $Z$ is order reversing if $\gamma(n)\le\gamma(m)$ and $m\le n$

Define two maps:

$\gamma:Y\rightarrow Z$

$\phi: Z\rightarrow Y$

Say that $\gamma$ and $\phi$ are both order reversing maps.

Then the pair $(\gamma,\phi)$ is a Galois pair if:

$y\le\phi(\gamma(y)),y\in Y$ and $z\le\gamma(\phi(z)),z\in Z$

As an example, I'll be using exercise 1 of the homework:

$X:=\{1,2,3\}$

Subsets $U$ of $X$:

$\{1\},\{2\},\{3\},\{1,2\},\{1,3\},\{2,3\},\{1,2,3\}$

$\gamma(U)$ is the set of all permutations $\pi$ of $X$, where $u^\pi=u$ for every element $u$ in $U$

$\gamma(\emptyset)=X$

$\gamma(\{1,2\},\{2,3\},\{1,3\},\{1,2,3\})=\{id_X\}$

$\gamma(\{1\},\{2\},\{3\})=H,D,K$ (respectively)

It's trivial to see that $\gamma$ is order reversing

$\phi(H)$ is the set of all elements $x\in X$ satisfying $x^\pi=x$ for each element $\pi\in H$

$\phi(\{id_X\})=\{1,2,3\}$

$\phi(H)=\{1\}$

$\phi(D)=\{2\}$

$\phi(K)=\{3\}$

$\phi(N)=\{1,2,3\}$

$\phi(X)=\emptyset$

Again, trivial to see that $\phi$ is order reversing

$(id_X)^{\phi\gamma}=1$

$H^{\phi\gamma}=H$

$K^{\phi\gamma}=K$

$D^{\phi\gamma}=D$

$N^{\phi\gamma}=X$

$X^{\phi\gamma}=X$

$\emptyset^{\gamma\phi}=\emptyset$

$\{1\}^{\gamma\phi}=\{1\}$

$\{2\}^{\gamma\phi}=\{2\}$

$\{3\}^{\gamma\phi}=\{3\}$

$\{1,2\}^{\gamma\phi}=\{1,2,3\}$

$\{2,3\}^{\gamma\phi}=\{1,2,3\}$

$\{1,3\}^{\gamma\phi}=\{1,2,3\}$

$\{1,2,3\}^{\gamma\phi}=\{1,2,3\}$

Then $(\gamma,\phi)$ is a Galois pair

## Question 5

If we have a commutative ring $R$ and a subring $S$, $R$ is integral over $S$ when every element in $R$ is integral on $S$.

For an element $r\in R$ to be integral on $S$, it must satisfy some monic polynomial:

$r^n+s_{n-1}r^{n-1}+...+s_1r+s_0=0$

Where $s_0,s_1,...s_{n-1}\in S$

## Question 6

The multiplicative inverse of $1+i$ is $\frac{1-i}{2}$ as $(1+i)(\frac{1-i}{2})=1$

## Question 7

The complex roots of $x^2+x+1=0$ are $\zeta$ and $\zeta^2$

Where $\zeta=-\frac{1}{2}+\frac{\sqrt{-3}}{2}$

## Question 8

The complex roots of $x^4+2=0$ are $\sqrt[4]{-2},-\sqrt[4]{-2}$

## Question 9

An irreducible element of a commutative ring is an element that satisfies two criteria:

1. It is not 0, and not a unit of the ring
2. If the element is a product of two other elements in the ring, then at least one of the factors is a unit of the ring

## Question 10

![[Pasted image 20220309151710.png]]

$\mathbb{Q}[\zeta]$ has a dimension of $2$, while $\mathbb{Q}[\sqrt[3]{2}]$ has a dimension of $3$

This is because a basis for $\mathbb{Q}[\zeta]$ is $1+\zeta$, whereas a basis for $\mathbb{Q}[\sqrt[3]{2}]$ is $1+\sqrt[3]{2}+\sqrt[3]{2}^2$

It's stated that the intersection of two subfields of $\mathbb{C}$ is also a subfield of $\mathbb{C}$.

Lemma 4.2 states that $\dim_S(U)=\dim_S(T)\dim_T(U)$ where $S$ and $T$ are subrings of $U$ with $S\subseteq T$

If we look at the basis for $\mathbb{Q}[\zeta]$ and $\mathbb{Q}[\sqrt[3]{2}]$, the only value they have in common is $1$, which is a basis for $\mathbb{Q}$

We can also say that $\mathbb{Q}[\zeta]$ contains no irrational numbers, and so a number of the form $a+b\sqrt[3]{2}+c\sqrt[3]{2}^2$ is only in $\mathbb{Q}[\zeta]$ if $b=c=0$


