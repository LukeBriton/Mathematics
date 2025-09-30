### 

#### Set Inclusions Between Number Sets

(Analysis I)

$\mathbb{N}\subset \mathbb{Z}\subset (\mathbb{D}\subset) \mathbb{Q}\subset \mathbb{R}\subset \mathbb{C}$ 

![Relations d'inclusion entre les différents ensembles de nombres.|300](https://upload.wikimedia.org/wikipedia/commons/9/9a/NumberSetinR2.svg)


Starting in this section with a simple and ‘natural’ axiom system for the natural numbers, we will construct in later sections the integers, the rational numbers, the real numbers and finally the complex numbers. This *constructive* approach has the advantage over the *axiomatic* formulation of the real numbers of D. Hilbert 1899, that the entire structure of mathematics can be built up from a few foundation stones coming from mathematical logic and axiomatic set theory.

#### Number System Ladder ($\mathbb{N}$ → $\mathbb{C}$)

Semiring $\mathbb{N}$ $\xrightarrow{\text{加法逆元→最小扩环}}$  有幺整数环 $\mathbb{Z}:=\mathbb{N}^2/\sim$ $\xrightarrow{\text{乘法逆元→最小扩域/作为整环的商域}}$ 有理数域 $\mathbb{Q:=(Z\times Z^\times)/\sim}$ $\xrightarrow{\text{完备性}}$ 完备有序域 $\mathbb{R:= (R, +, ·, ≤)}$ $\xrightarrow{x^2=1\text{可解→最小扩域}}$ 复数域 $\mathbb{C} := (\mathbb{R}^2, +, ·)$

#### Natural Numbers $\mathbb{N}$

![[Natural Numbers]]

#### Integers $\mathbb{Z}$

##### Idea

$\mathbb{N} = (\mathbb{N}, +, ·)$ is ‘almost’ a commutative ring with unity. The only property missing is the existence of an additive inverse $-n$ for each $n ∈ \mathbb{N}$.

Suppose that $Z$ is a ring which contains $\mathbb{N}$, and that the ring operations on $Z$ restrict to the usual operations on $\mathbb{N}$. Then for all $(m, n) ∈ \mathbb{N}^2$ the difference $m - n$ is a well defined element of $Z$, and

$$
m − n = m' − n' \Leftrightarrow m + n' = m' + n , (m', n') ∈ \mathbb{N}^2 .
$$

$$
(m - n) + (m' - n') = (m + m') - (n + n')\\
(m - n)] \cdot (m' - n') = (mm' + nn') - (mn' + m'n)
$$

##### 9.1 Theorem

There is a smallest domain with unity, $\mathbb{Z}$, such that $\mathbb{N} ⊆ \mathbb{Z}$ and the ring operations on $\mathbb{Z}$ restrict to the usual operations on $\mathbb{N}$. This ring is unique up to isomorphism and is called the **ring of integers**.

Define an equivalence relation on $\mathbb{N}^2$ by

$$
(m, n) ∼ (m', n') :\Leftrightarrow m + n' = m' + n
$$

and set $\mathbb{Z} := \mathbb{N}^2/∼$. Define addition and multiplication on $\mathbb{Z}$ by

$$
[(m, n)] + [(m', n')] := [(m + m', n + n')]\newline
[(m, n)] \cdot [(m', n')] := [(mm' + nn', mn' + m'n)]
$$

$\mathbb{Z} := (\mathbb{Z}, +, ·)$ is a commutative ring without zero divisors.

Now let $R ⊇ \mathbb{N}$ be some commutative ring with unity and without zero divisors, such that the operations on $R$ restrict to the usual operations on $\mathbb{N}$. Since $\mathbb{Z}$, by construction is clearly minimal, there is a unique injective homomorphism $ϕ : \mathbb{Z} → R$ with $ϕ|\mathbb{N} = \text{(inclusion of }\mathbb{N}\text{ in } R)$. This implies the claimed uniqueness up to isomorphism.

In the following we do not distinguish different isomorphic copies of $\mathbb{Z}$ and speak of **the** (unique) **ring of integers**. (Another approach: Fix once and for all a particular representative of the isomorphism class of $\mathbb{Z}$ and call it **the** ring of integers.) The elements of $\mathbb{Z}$ are the **integers**, and $-\mathbb{N}^× := \{ -n ; n ∈ \mathbb{N}^× \}$ is the set of **negative integers**. Clearly $\mathbb{Z} = \mathbb{N}^× ∪ {0} ∪ (-\mathbb{N}^×) = \mathbb{N} ∪ (-\mathbb{N}^×)$ as disjoint unions.

#### Rational numbers $\mathbb{Q}$

In the ring $\mathbb{Z}$, we can now form arbitrary differences $m - n$, but, in general, the quotient of two integers $m/n$ remains undefined, even if $n \ne 0$. To overcome this ‘defect’ we will construct a field $K$ which contains $\mathbb{Z}$ as a subring. Of course, we choose $K$ ‘as small as possible’.

##### 9.2 Theorem

There is, up to isomorphism, a unique smallest field Q, which contains Z as a subring.

$$
(a, b) ∼ (a', b') :\Leftrightarrow ab' = a'b
$$

and set $\mathbb{Q} := (\mathbb{Z}\times\mathbb{Z}^×/∼)$.

$$
[(a, b)] + [(a', b')] := [(ab' + a'b, bb')]\newline
[(a, b)] \cdot [(a', b')] := [(aa', bb')]
$$

With these operations $\mathbb{Q} := (\mathbb{Q}, +, ·)$ is a field.

In the construction of $\mathbb{Q}$ as an ‘extension field’ of $\mathbb{Z}$ in Theorem 9.2, no use is made of the fact that the elements of $\mathbb{Z}$ are ‘numbers’. All that was necessary was that $\mathbb{Z}$ be a domain. So this proof shows that any domain $R$ is a subring of a unique (up to isomorphism) minimal field $Q$. This field is called the **quotient field of R**.

#### Real numbers $\mathbb{R}$

We seek an ordered **extension field** of $\mathbb{Q}$ in which the equation $x^2 = a$ is solvable for each $a > 0$.

##### Order Completeness
![[Real Numbers#Order Completeness]]


##### Extended Number Line

$\mathbb{\bar{R}} := \mathbb{R} ∪ \{±∞\}, -\infty < x < \infty, x\in \mathbb{R}$

$\mathbb{\bar{R}}$ is a totally ordered set, but is not a field.

- (i) If $A ⊆ \mathbb{R}$ and $x ∈ \mathbb{R}$, then
	- (α) $x < \sup(A)$ $\Leftrightarrow$ $∃\ a ∈ A$ such that $x < a$.
	- (β) $x > \inf(A)$ $\Leftrightarrow$ $∃\ a ∈ A$ such that $x > a$.
- (ii) Every subset $A$ of $\mathbb{R}$ has a supremum and an infimum in $\mathbb{\bar{R}}$.

$\text{Order Completeness} \implies \text{The Archimedean Property}$

**10.6 Proposition (Archimedes)** $\mathbb{N}$ is not bounded above in $\mathbb{R}$, that is, for each $x ∈ R$ there is some $n ∈ \mathbb{N}$ such that $n > x$.

**10.7 Corollary**

- (i) Let $a ∈ \mathbb{R}$. If $0 ≤ a ≤ 1/n$ for all $n ∈ \mathbb{N}^×$, then $a = 0$.

- (ii) For each $a ∈ \mathbb{R}$ with $a > 0$ there is some $n ∈ \mathbb{N}^×$ such that $1/n < a$.

(i)

$$
\forall n ∈ ℕ^×,\ 0 < a ≤ 1/n \implies \forall n ∈ ℕ^×,\ n\le 1/a
$$

Thus $ℕ$ would be bounded above in $ℝ$, contradiction.

(ii) is an equivalent reformulation of (i).

**The Density of the Rational Numbers in $\mathbb{R}$**

The next proposition shows that $\mathbb{Q}$ is ‘dense’ in $\mathbb{R}$, that is, real numbers can be ‘approximated’ by rational numbes.

$\text{The Archimedean Property} \implies \text{Density of the Rational Numbers in }\mathbb{R}$

**10.6 Proposition (Density)** For all $a, b ∈ \mathbb{R}$ such that $a < b$, there is some $r ∈ \mathbb{Q}$ such that $a < r < b$.

- existence of (unique) $n^\text{th}$ root $\sqrt[n]{a}$ ($n\in \mathbb{N}$)
- $r^\text{th}$ power $a^r=(\sqrt[q]{a})^p$ ($r=\frac{p}{q} \in \mathbb{Q}$)

**The Density of the Irrational Numbers in $\mathbb{R}$**

**10.11 Proposition (Density)** For all $a, b ∈ \mathbb{R}$ such that $a < b$, there is some $\varepsilon ∈ \mathbb{R}\backslash \mathbb{Q}$ such that $a < r < b$.

#### Complex numbers $\mathbb{C}$



#### Représentation des nombres irrationnels

![Représentation des nombres irrationnels.|400](https://upload.wikimedia.org/wikipedia/commons/1/19/Irrationnels.svg)