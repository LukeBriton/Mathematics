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