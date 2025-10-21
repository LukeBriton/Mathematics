#### Sequences

- vector space $s=s(\mathbb{K})=\mathbb{K}^\mathbb{N}$
- 收敛列加法、数乘 
	the convergent sequences form a subspace of $s$.
$$
c=c(\mathbb{K}):=\{ (x_{n}) ∈ s ; (x_{n})\text{ converges}\}
$$
	$c$ is a subspace of $s$, and
$$
\lim:c\to \mathbb{K}, (x_{n})\mapsto \lim{x_{n}}
$$
	is linear.
	
- Null Sequence: $\text{ker}(\lim)=c_{0}=c_{0}(\mathbb{K}):=\{ (x_{n}) ∈ s ; (x_{n})\text{ converges with}\lim x_{n}=0\}$
- 零列$\times$有界、收敛列$\times$收敛列
	$c$ is a subalgebra of $s$ and the function $\lim:c\to \mathbb{K}$ is an algebra homomorphism

https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-42/issue-1/Topologies-on-sequences-spaces/pjm/1102968025.pdf

- 非零收敛列倒数

#### Cluster Points

- 任意邻域，无限多项。
- 任意邻域，任意序号，总有项。
- 任意 $\varepsilon$ ，任意序号后，总有项在开球里。

$$
\varphi: \mathbb{N} \longleftrightarrow \mathbb{Q}, x_{n}:=\varphi(n)\implies\forall x\in \mathbb{R}\text{ is a cluster point of }(x_{n}).
$$

#### Convergence of sequences

- 任意邻域，几乎无穷多项。
- 任意邻域，总有尾列。
- 任意 $\varepsilon$，总有尾列在开球里。

- 收敛的条件比聚点更强。

- 收敛$\implies$有界

- 收敛$\implies$有唯一聚点

- 有界+有聚点$\cancel{ \implies }$收敛

[real analysis - Show a bound sequence with a cluster point is indeed convergent - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1014909/show-a-bound-sequence-with-a-cluster-point-is-indeed-convergent)

[general topology - In what metric spaces does bounded + unique limit point imply convergence of a sequence? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4762540/in-what-metric-spaces-does-bounded-unique-limit-point-imply-convergence-of-a-s)

[ca.classical analysis and odes - Sequence that converge if they have an accumulation point - MathOverflow](https://mathoverflow.net/questions/24508/sequence-that-converge-if-they-have-an-accumulation-point)

[Simple examples of proper metric spaces? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/792253/simple-examples-of-proper-metric-spaces)

- 收敛$\implies$子列收敛于聚点

- 是聚点 $\Longleftrightarrow$ 有子列收敛焉

- 比较审敛

- 收敛 $\Longleftrightarrow$ 各分量收敛 （little to be gained）
	- 复数列收敛 $\Longleftrightarrow$ 实部、虚部收敛

- Bolzano-Weierstrass
	有界 $\implies$ 有收敛子列&聚点

- 收敛 $\implies$ Cauchy列
	完备：Cauchy列 $\implies$ 收敛 
#### Bounded Sets

- $d(x,y)$ 上有界，$\sup{d(x,y)}$ 为直径。

- 像集有界，数列有界
	- 有界数列向量空间 $\mathscr{l}_{∞} := \mathscr{l}_{∞}(\mathbb{K}) := B(\mathbb{N}, \mathbb{K})$ 
		supremum norm:  数列范数的上确界

- 在其诱导度量空间中有界，则在赋范空间中有界

- 像集有界，函数有界
	- 有界函数向量空间 $B(X,E):=(B(X, E), ‖·‖_{∞}):=\{ u ∈ E^X ; u\text{ is bounded} \}$
		$X$ 非空集，$(E, ‖·‖)$ 赋范向量空间，则$E^X$中，有界函数集 $B(X,E)$ 构成子空间。
		supremum norm: $‖·‖_{∞}$  函数值范数的上确界
	- $(E, ‖·‖)$ Banach $\implies$ $B(X,E)$ Banach
	- $B(E, F ) ∩ \text{Hom}(E, F ) = {0}.$



#### Topology

- $\mathbb{C} := \mathbb{R} + i\mathbb{R}$ can be identified with the set $\mathbb{R}^2$
	So is $\mathbb{C}^m \longleftrightarrow$ $\mathbb{R}^{2m}$ 典范恒等
	Thus for topological questions, that is, statements about neighborhoods of points, the sets $\mathbb{C}^m$ and $\mathbb{R}^{2m}$ can be identified.
- The notions ‘cluster point’ and ‘convergence’ are topological concepts, that is, they are defined in terms of neighborhoods. Thus they are invariant under changes to equivalent norms.

#### Monotone Sequences

- 单调有界，收敛于确界

- 一些个重要极限（我好嫌计算。。）

#### Infinite Limits

- $\bar{\mathbb{R}}$ 上无合适度量，以ad hoc定义扩展集合。。
	$\bar{\mathbb{R}}$ 上“收敛”包括趋于无穷（converge improperly）。
	$\bar{\mathbb{R}}$ 上单调集合“收敛”

- $\bar{\mathbb{R}}$ 中的上下极限（**任意**数列均有）
	$\limsup:=\overline{\lim\limits_{ n \to \infty }}$ 最大聚点
	$\liminf:=\underline{\lim}\limits_{ n \to \infty }$ 最小聚点

- $\bar{\mathbb{R}}$ 上收敛 $\Longleftrightarrow$ $\limsup\le\liminf$

#### Completeness

- 任意 $\varepsilon$，总有尾列，任两项距离小于 $\varepsilon$。

Cauchy列 平移不变 不能用邻域定义

[Translation invariant metrics and topological groups - Mathematics Stack Exchange](https://math.stackexchange.com/questions/976933/translation-invariant-metrics-and-topological-groups)

- 收敛 $\implies$ Cauchy列
- Cauchy列 $\implies$ 有界
- Cauchy列有收敛子列 $\implies$ 收敛
- 完备：Cauchy列 $\implies$ （有界 $\implies$ 有收敛子列 $\implies$）收敛 

- The completeness of a normed vector space E is invariant under changes to equivalent norm

- $\mathbb{K}^m$ Banach

- $\mathbb{Q}^\mathbb{N}$ 有幺交换环
	- $\bar{a}=(a,a,\dots,a)$，则 $\bar{1}$ 为其幺元
	- $\mathcal{R}:=\{\text{Cauchy sequences}\in \mathbb{Q}^\mathbb{N}\}$ 是其子环 From Exercise I.8.6, we know that $\mathcal{R}$ cannot be a field （？）
	- $\mathbf{c}_{0}:=\{\text{Null sequences}\in \mathbb{Q}^\mathbb{N}\}$ 是 $\mathcal{R}$ 的非平凡真理想
	- $R = \mathcal{R}/\mathbf{c}_{0}$
		$\mathbb{Q}\to R, a\mapsto [\bar{a}]=\bar{a}+\mathbf{c}_{0}$ 入射，$\mathbb{Q}$ 作为 $R$ 的子环
		$\mathcal{P}:=\{\text{strictly positive sequences}\in \mathcal{R}\cup\mathbf{c}_{0}\}$
		- $(R, \le)$ 有序环，在$\mathbb{Q}$上诱导自然序
			$[r]<[s]:\Leftrightarrow s-r\in\mathcal{P}$
		- $R$ 是域
		- $\mathbb{Q}$ 上单调有界序列 $\implies$ Cauchy
		- $R$ 中单调有界序列 $\implies$ 有确界
		- $R$ 是 $\mathbb{Q}$ 的有序域扩张

#### Convergence of Series

级数收敛：部分和序列收敛

- $\sum x_{k}$ 收敛 $\implies$ $(x_{k})$ 零列

- 调和级数发散（非柯西列）

- 几何级数 $|a|?1$

- the linearity of the limit function holds for series
	部分和同样可以视作数列。。

- Cauchy 审敛准则
	部分和序列是Cauchy列

- 非负级数：$∑ x_k < ∞ \Longleftrightarrow ∑ x_k \text{ converges}$

- 交错级数 $± ∑(−1)^kx_{k}$ with $x_{k}\ge{0}$
	- Leibniz 审敛准则
		$(x_{k})$ 非负单减零列 $\implies$ $∑(−1)^kx_{k}$ 收敛
	- 交错调和级数

- 实数的各进制展开

- $\lfloor \cdot \rfloor : \mathbb{R} \to \mathbb{Z}, x\to \lfloor x \rfloor$

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
	\begin{tikzcd}
		\mathsf{\mathbb{R}}
		\arrow[bend left=50, r, "\mathrm{floor\ or\ ceiling}", ""' name=U]
		\arrow[bend right=50, r, "" name=D, "\supset"'] &
		\mathsf{\mathbb{Z}} &
		
	\end{tikzcd}
\end{document}
```

- $g\ge{2}$ 各实数均有 base $g$ expansion
	- This expansion is unique if expansions satisfying $x_{k} = g − 1$ for almost all $k ∈ N$ are excluded. (e.g. $1.94\dot{9}$)
	- $x$ is a rational number if and only if its base $g$ expansion is periodic
	 $x=\lfloor x \rfloor+r,\ r\in[0, 1)$
		Too many technical details...

#### Absolute Convergence

- 绝对收敛 $\implies$ 收敛
- 条件收敛

- 强级数（majorant）审敛准则
	Banach Space 级数有强级数 $\implies$ 绝对收敛

- 根值审敛法
	$α:=\overline{\lim}\sqrt[k]{|x_{k}|}$
	$α<1$, $α>1$
	$α=1$ both
- 比值审敛法
	$\frac{|x_{k+1}|}{|x_{k}|}$

- 指数函数：$\text{exp}:\mathbb{C}\to \mathbb{C}, z\mapsto \sum\limits_{k=0}^\infty \frac{z^k}{k!}$
- 重排
	a convergent series cannot be arbitrarily rearranged without changing its value
	- 重排定理
		绝对收敛 $\implies$ 重排绝对收敛&值相同