### Group Action

群作用
$$
G\times X \to X,\quad (g,x)\mapsto g\cdot x
$$
- 左幺元
- 结合律

幺半群作用 $M$ 的左作用
$$
a:M\times X \to X,\quad a(m,x)\mapsto m\cdot x
$$
- 左幺元
- 结合律

实 $n \times n$ 矩阵所成幺半群 $M_n(\mathbb{R})$ 作用于 $\mathbb{R}^n$：视 $\mathbb{R}^n$ 元素为 $n \times 1$ 阶竖直矩阵，则作用 $(A, x) \mapsto A x$ 无非是矩阵乘法。

- 循环群 $\exists g\in G, G = \left \langle \, g \, \right \rangle = \left\{ g^k | \; k \in \mathbb{Z} \right\}$

n阶有限循环群 $\cong$ 整数同余加法群 $\mathbb{Z}/n\mathbb{Z}$

- 群同态 

Let $G=(G,\odot)$ and $G^{\prime}=(G^\prime,\ast)$ be groups. A function $\varphi : G → G^′$ is called  
a (group) homomorphism, if
$$
\varphi(g\odot h) = \varphi(g)* \varphi(h), g,h\in G
$$

- 子群

In the [mathematical](https://en.wikipedia.org/wiki/Mathematics "Mathematics") field of [group theory](https://en.wikipedia.org/wiki/Group_theory "Group theory"), **Lagrange's theorem** states that if H is a subgroup of any [finite group](https://en.wikipedia.org/wiki/Finite_group "Finite group") G, then $| H |$  is a divisor of $| G |$  . That is, the [order](https://en.wikipedia.org/wiki/Order_of_a_group "Order of a group") (number of elements) of every [subgroup](https://en.wikipedia.org/wiki/Subgroup "Subgroup") divides the order of the whole group.

The following variant states that for a subgroup H of a finite group G  , not only is $| G | / | H |$  an integer, but its value is the [index](https://en.wikipedia.org/wiki/Index_of_a_subgroup "Index of a subgroup") $[ G : H ]$ , defined as the number of left [cosets](https://en.wikipedia.org/wiki/Coset "Coset") of $H$ in $G$ .

This variant holds even if G is infinite, provided that | G |  , | H |, and $[ G : H ]$ are interpreted as [cardinal numbers](https://en.wikipedia.org/wiki/Cardinal_number "Cardinal number").

The left [[coset]]s of $H$ in $G$ are the [[equivalence class]]es of a certain [[equivalence relation]] on $G$: specifically, call $x$ and $y$ in $G$ equivalent if there exists $H$ in $H$ such that $x=yh$. 
Therefore, the set of left cosets forms a [[Partition of a set|partition]] of $G$.
Each left coset $aH$ has the same cardinality as $H$ because $x \mapsto ax$ defines a bijection $H \to aH$ (the inverse is $y \mapsto a^{-1}y$).
The number of left cosets is the [[index of a subgroup|index]] $[G : H]$.
By the previous three sentences, 
$\left|G\right| = \left[G : H\right] \cdot \left|H\right|.$

定理的證明利用了[[陪集]]的以下性質：
- 一個子群的所有陪集在集合意義下有相同的大小（ Cardinality ）。
- 一個子群的所有陪集分割——即每個群元素都位在剛好一個（ exactly one ）陪集之中——了整個群。
- 根據集合的特性， $G$ 的大小可以寫成是陪集的大小 $|H|$ 乘上陪集的數量 $[G:H]$。

- 不动点集

- 轨道

- 稳定化子

[abstract algebra - Why are they called orbits? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/516057/why-are-they-called-orbits)

the only reason I find convincing for that name is that in some sense the action of group over a set can be viewed as a dynamical system and thus the name orbit has the usual physical "interpretation" and justification.

[Show every subgroup of D4 can be regarded as an isotropy group for a suitable action of D4 - Mathematics Stack Exchange](https://math.stackexchange.com/questions/76255/show-every-subgroup-of-d4-can-be-regarded-as-an-isotropy-group-for-a-suitable-ac/76423#76423)

[abstract algebra - Intuitive definitions of the Orbit and the Stabilizer - Mathematics Stack Exchange](https://math.stackexchange.com/questions/253179/intuitive-definitions-of-the-orbit-and-the-stabilizer)

Consider a sphere $S⊂\mathbb{R}^3$ and a group $G$ of (all) rotations along the OZ axis (north-south pole, as Earth).

The orbit of $x$ is "everything that can be reached from $x$ by an action of something in $G$."

![orbit](https://i.sstatic.net/C4QEP.png)

$\text{Orb}(x) = \{ y = g_\alpha\cdot x \mid g \in G, \alpha \in [0, 2\pi)\}$

That means the orbit of a point $x$ of the sphere $S$ is a set of all the points that a $G$ (i.e. rotations) can produce from it, in our case a circle, like the dotted one on the picture.

The stabilizer of $x$ is "the set of all elements of $G$ which don't move $x$ when they act on $x$".

$G_{\text{pole}} = G$

$G_{\text{non-pole}} = \{1\}$

stabilizer of $x$ is the biggest subgroup that won't disturb your $x$.

$|G| = |\text{Orb}(x)| × |\text{St}(x)|$