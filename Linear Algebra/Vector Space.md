
# Vector Space

## Algebraic View

（代数学方法 卷一：基础架构）

![[Algebraic Structures#Algebraic Structure Ladder (Set → Field)]]

Additive Group $\xrightarrow{\text{（环）R的纯量乘法（分配律、相容性、幺元）}}$ Left/Right $R$-module $M$ $\xrightarrow{\text{除环D}}$ $D$-Vector Space $\xrightarrow{\text{域K}}$ $K$-Vector Space, linear maps between each pair are $K$-Module Homomorphisms

相容性缺失所成的反例见：[Does a vector space need the compatibility of scalar multiplication with field multiplication axiom?](https://www.reddit.com/r/askmath/comments/1b718py/does_a_vector_space_need_the_compatibility_of/)

此处“数乘”为
$$
\displaylines{
(\cdot,\cdot):\mathbb{C}\times\mathbb{C}^2\rightarrow\mathbb{C}^2,\\
(a+bi, (c,d))\mapsto(ac,ad)
}
$$

1. 从形式观点看，模是带有一族乘法算子的加法群。

2. 任意环对自身的左乘法构成左 $R$-模，对右乘法构成右 $R$-模。

3. 交换环 $R$ 上的模不分左右，可以简称为 $R$-模。

4. 设 $D$ 为除环，我们称右 $D$-模为 $D$-向量空间。其子模，商模等也称为子空间，商空间。定义中选取左模或右模其实无关宏旨，当 $D$ 为域时更可以不论左右。

## Analytic View

（Analysis I & 香蕉空间）

![[Algebraic Structures#Vector Space Ladder (Ab → Hilb)]]

尽管形式上如此堆叠，实际诱导先后为 $\text{Inner product}\implies \text{Norm}\implies \text{Metric}$

## Categorical View

- 选定一个域 𝕜, 令 $\mathsf{Vect}(\Bbbk)$ 为 𝕜 上所有向量空间构成的范畴, 态射为线性映射.
	
	类此定义有限维向量空间范畴 $\text{Vect}_f(\Bbbk)$, 它是 $\mathsf{Vect}(\Bbbk)$ 的全子范畴.

- 对于任意 $\Bbbk$-向量空间 $V$, 定义其对偶空间
$$
V^\vee := \text{Hom}_\Bbbk(V, \Bbbk) = \{ \Bbbk-\text{线性映射}\; V \to \Bbbk \}.
$$
	任一线性映射 $f: V_1 \to V_2$ 诱导对偶空间的反向映射
$$
\begin{align*}
	f^\vee: V_2^\vee & \longrightarrow V_1^\vee, \\
	[\lambda: V_2 \to \Bbbk] & \longmapsto \lambda \circ f.
\end{align*}
$$

	易见 $D: V \to V^\vee$, $f \mapsto f^\vee$ 定义了函子 $D: \mathsf{Vect}(\Bbbk)^\text{op} \to \mathsf{Vect}(\Bbbk)$, 可以验证 $D$ 是忠实的. 根据注记 \ref{rem:op-functor}, 我们有合成函子 $D D^\text{op}: \mathsf{Vect}(\Bbbk) \to \mathsf{Vect}(\Bbbk)$.
			
	将 $D$ 限制于有限维向量空间, 便得到函子 $D: \mathsf{Vect}_f(\Bbbk)^\text{op} \to \mathsf{Vect}_f(\Bbbk)$ 和 $D D^\text{op}: \mathsf{Vect}_f(\Bbbk) \to \mathsf{Vect}_f(\Bbbk)$. 分别称为对偶和双对偶函子.

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
	\begin{tikzcd}


		V_1 \arrow[rd, "\lambda\circ f"] \arrow[rr, "f"] &            & V_2 \arrow[ld, "\lambda"] \\
		                                                 & \Bbbk &                          

	\end{tikzcd}

\end{document}
```

考虑群范畴 $\mathsf{Grp}$. 对于任一个群 $G$, 总是可以忘掉 $G$ 的群结构而视之为集合, 群同态当然也可以视为集合间的映射, 此程序给出\emph{忘却函子} $\mathsf{Grp} \to \mathsf{Set}$. 准此要领可对其他结构定义忘却函子, 例如 $\mathsf{Top} \to \mathsf{Set}$ (忘掉空间的拓扑结构), $\mathsf{Vect}(\Bbbk) \to \mathsf{Ab}$ (忘掉 $\Bbbk$-向量空间 $V$ 的纯量乘法, 只看它的加法群 $(V, +)$, 这里 $\Bbbk$ 是任意域) 等等, 不一一列举. 这类函子显然忠实而非全.

对于任意向量空间 $V$ 皆有求值映射

$$
\begin{align*}
	\text{ev}: V & \longrightarrow DD^\text{op} V = (V^\vee)^\vee \\
	v & \longmapsto [\lambda \mapsto \lambda(v)].
\end{align*}
$$

对于任意线性映射 $f : V → W$ , 从 $f^∨$ 的定义不难检查以下图表

```tikz
\usepackage{tikz-cd}

\begin{document}
	\begin{tikzcd}

		V \arrow[r, "\mathrm{ev}"] \arrow[d, "f"'] & DD^\mathrm{op} V \arrow[d, "{DD^\mathrm{op} f}"] \\
		W \arrow[r, "\mathrm{ev}"'] & DD^\mathrm{op} W
	\end{tikzcd}

\end{document}
```

```tikz
\usepackage{tikz-cd}

\begin{document}
	\begin{tikzcd}

		V \arrow[r, "\mathrm{ev}"] \arrow[d, "f"'] & V^{**} \arrow[d, "{f^{**}}"] \\
		W \arrow[r, "\mathrm{ev}"'] & W^{**}
	\end{tikzcd}

\end{document}
```

是交换的, 于是有 $ev : id → DD^{op}$. 容易看出 $ev : V → DD^{op}V$ 总是单射, 事实上可以  
证明 ev 是双射当且仅当 $V$ 有限维. 一切限制到全子范畴 $\mathsf{Vect}_{f}(\Bbbk)$ 上, 遂有同构
$$
\text{ev}: \text{id}_{\mathsf{Vect}_f(\Bbbk)} \stackrel{\sim}{\rightarrow} D D^\text{op}.
$$
同一式子在相反范畴中诠释，便是
$$
\text{id}_{\mathsf{Vect}_f(\Bbbk)^\text{op}} \stackrel{\sim}{\rightarrow} D^\text{op} D.
$$


```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
	\begin{tikzcd}
		\mathsf{Vect}_{\Bbbk}
		\arrow[bend left=50, r, "\mathrm{id}", ""' name=U]
		\arrow[bend right=50, r, "" name=D, "(-)^{**}"'] &
		\mathsf{Vect}_{\Bbbk} &
		\arrow[Rightarrow, to path=(U) -- (D) \tikztonodes, "\mathrm{ev}"] 
	\end{tikzcd}
\end{document}
```

故函子 $D: \mathsf{Vect}_f(\Bbbk)^\text{op} \to \mathsf{Vect}_f(\Bbbk)$ 是范畴间的等价, 而 $D^\text{op}: \mathsf{Vect}_f(\Bbbk) \to \mathsf{Vect}_f(\Bbbk)^\text{op}$ 则是它的拟逆.


选定域 $\Bbbk$, 定义范畴 $\mathsf{Mat}$ 如下: 其对象是 $\mathbb{Z}_{\geq 0}$, 对任意对象 $n, m \in \mathbb{Z}_{\geq 0}$, 定义 $\text{Hom}(n, m) := M_{m \times n}(\Bbbk)$ 为域 $\Bbbk$ 上的全体 $m \times n$ 矩阵 $A = (a_{ij})_{\substack{1 \leq i \leq m \\ 1 \leq j \leq n}}$ 所成集合. 约定 $M_{0 \times n}(\Bbbk) = M_{m \times 0}(\Bbbk) := \{0\}$. 态射的合成定义为寻常的矩阵乘法
$$
	\begin{align*}
		\text{Hom}(n, m) \times \text{Hom}(m, k) & \longrightarrow \text{Hom}(n, k) \\
		(A, B) & \longmapsto BA .
	\end{align*}

$$

定义函子 $F: \mathsf{Mat} \to \mathsf{Vect}_f(\Bbbk)$ 如下: 置 $F(n) = \Bbbk^{\oplus n} := M_{n \times 1}(\Bbbk)$, 而对 $A \in \text{Hom}(n, m)$, 线性映射 $FA: \Bbbk^{\oplus n} \to \Bbbk^{\oplus m}$ 是矩阵乘法 $v \mapsto Av$. 我们断言 $F$ 是范畴等价.

这一切只是虚张声势的线性代数. 首先留意到 $F: \text{Hom}(n, m) \to \text{Hom}_\Bbbk(\Bbbk^{\oplus n}, \Bbbk^{\oplus m})$ 是双射, 这无非是线性映射的矩阵表达. 再者, 从 $V \simeq \Bbbk^{\oplus \dim V}$ ($V$ 是 $\Bbbk$-向量空间) 可知 $F$ 是全忠实本质满的, 由定理 \ref{prop:functor-equiv-criterion} 可知它是范畴等价.

域 $\Bbbk$ 上的向量空间范畴 $\mathsf{Vect}(\Bbbk)$: 零空间是零对象, 零映射是零态射.

选定域 $\Bbbk$, 定义函子 $V: \mathsf{Set} \to \mathsf{Vect}(\Bbbk)$ 如下: 对于集合 $X$, 命 $V(X) := \bigoplus_{x \in X} \Bbbk x$ 为以 $X$ 为基的 $\Bbbk$-向量空间. 任意映射 $f: X \to Y$ 皆诱导出线性映射 $V(f): V(X) \to V(Y)$, 它由在基上的限制 $f$ 所刻画. 令 $U: \mathsf{Vect}(\Bbbk) \to \mathsf{Set}$ 为忘却函子, 则 $x \mapsto x \in V(X)$ 给出态射 $\iota: X \to UV(X)$. 尽管有些拗口, 不妨设想 $V(X)$ 是 $X$ 上的“自由向量空间”.

为阐明 $V(X)$ 的泛性质, 定义范畴 $(X / U)$ 使得其对象形如 $(W, i: X \to U(W))$, 其中 $W \in \text{Ob}\mathsf{Vect}(\Bbbk)$ 而 $X \xrightarrow{i} U(W)$ 是 $\mathsf{Set}$ 中的态射, 态射定为使下图交换的线性映射 $h: W_1 \to W_2$:

```tikz
\usepackage{tikz-cd}

\begin{document}
	\begin{tikzcd}

		{} & X \arrow[ld, "i_1"'] \arrow[rd, "i_2"] & \\
		U(W_1) \arrow[rr, "U(h)"'] & & U(W_2).

	\end{tikzcd}

\end{document}
```

我们断言 $(V(X), \iota)$ 是 $(X / U)$ 中的始对象. 这说的无非是对任意 $(W, i) \in \text{Ob}(X / U)$, 存在唯一的 $h: V(X) \to W$ 使图表

```tikz
\usepackage{tikz-cd}

\begin{document}
	\begin{tikzcd}

		{} & X \arrow[ld, "\iota"'] \arrow[rd, "i"] & \\
		U(V(X)) \arrow[rr, "U(h)"'] & & U(W)

	\end{tikzcd}

\end{document}
```

交换. 由于 $X$ 是 $V(X)$ 的基, 这般 $h$ 是唯一确定了的.

```tikz
\usepackage{tikz-cd}
\begin{document}
	\begin{tikzcd}
	  & X \arrow[ld, "\iota_X"'] \arrow[rd, "\Phi(h)"] & \\
	  U(V(X)) \arrow[rr, "U(k)"'] & & U(W)
	\end{tikzcd}
	
	\begin{tikzcd}
	  & X \arrow[ld, "\iota_X"'] \arrow[rd, "\Phi(h)"] & \\
	  U(V(X)) \arrow[rr, "U(h)"'] & & U(W)
	\end{tikzcd}

\end{document}
```

上图涉及 $h$ 的条件称为 $V(X)$ 满足的泛性质. 根据命题 \ref{prop:initial-obj-uniqueness}, 我们说泛性质刻画了 $V(X)$ 连同 $\iota: X \to UV(X)$, 至多差一个唯一的同构. 之后我们还会遇到更精密的“自由对象”的构造, 如自由群.

## Geometrical View

classical continuous geometries

Here we merely list, for future reference, several very classical geometries whose transformation groups are “continuous” rather than finite or discrete. We will not make the intuitively clear notion of continuous transformation group precise (this would involve defining the so-called topological groups or even Lie groups)

Finite-dimensional vector spaces

$$
(\mathbb{V}^n : \text{GL}(n))
$$

n-dimensional orthonormal vector space

$$
(\mathbb{V}^n : \text{O}(n))
$$

Affine spaces are, informally speaking, finite-dimensional vector spaces “without a fixed origin”. This means that their transformation groups $\text{Aff}(n)$ contain, besides $\text{GL}(n)$, all parallel translations of the space (i.e., transformations of the space obtained by adding a fixed vector to all its elements).

$$
(\mathbb{V}^n : \text{Aff}(n))\quad\text{or}\quad(\mathbb{V}^n : \text{Aff}(n))
$$
Euclidean spaces
$$
(\mathbb{R}^n : \text{Sym}(\mathbb{R}^n))
$$

[[Euclidean Geometry]]

## Inclusive Relations Between Spaces

$\{ \textrm{inner product vector spaces} \} \subsetneq \{ \textrm{normed vector spaces} \} \subsetneq \{ \textrm{metric spaces} \} \subsetneq \{ \textrm{topological spaces} \}.$
- Any metric space is a Hausdorff space.

"topology on $X$ induced from the metric $d$"

"metric on $E$ induced from the norm $‖·‖$"

"norm induced from the scalar product $(·|·)$"



Euclidean inner product: $(x|y) := \sum^{m}_{j=1} x_j \bar{y}_j$

Hilbert norm: "norm $‖x‖ := \sqrt{(x|x)}$ on $E$ induced from the scalar product $(·|·)$"

- (Jordan-von Neumann theorem) keys are parallelogram law and polarization identity.

Euclidean norm: "norm $|x| := \sqrt{(x|x)} = \sqrt{\sum^{m}_{j=1}|x_{j}|^2}$ on $E$ induced from the Euclidean inner product $(·|·)$"

metric induced from the norm: $d(x, y)=‖x − y‖$


拓扑空间

![[Normed Vector Space]]

![[Hilbert Space]]

[Inner product space](https://en.wikipedia.org/wiki/Inner_product_space)

The article on [Hilbert spaces](https://en.wikipedia.org/wiki/Hilbert_spaces "Hilbert spaces") has several examples of inner product spaces, wherein the metric induced by the inner product yields a [complete metric space](https://en.wikipedia.org/wiki/Complete_metric_space "Complete metric space"). An example of an inner product space which induces an incomplete metric is the space $C([a, b])$, of continuous complex valued functions $f$ and <math>g</math> on the interval $[a, b]$. The inner product is
$$
\langle f, g \rangle = \int_a^b f(t) \overline{g(t)} \, \mathrm{d}t.
$$
This space is not complete; consider for example, for the interval $[−1, 1]$ the sequence of continuous "step" functions, $\{ f_k \}_k,$ defined by:
$$
f_k(t) = \begin{cases} 0 & t \in [-1, 0] \\ 1 & t \in \left[\tfrac{1}{k}, 1\right] \\ kt & t \in \left(0, \tfrac{1}{k}\right) \end{cases}
$$
This sequence is a [Cauchy sequence](https://en.wikipedia.org/wiki/Cauchy_sequence "Cauchy sequence") for the norm induced by the preceding inner product, which does not converge to a _continuous_ function.

![[Banach Space]]

![[Metric Space]]