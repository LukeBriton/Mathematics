> Der Begriff der Konvergenz erlaubt uns
> - to add together infinite sets of numbers (or vectors)
> - unendlich viele (Rechen-)Operationen durchzuführen
> was die Analysis von der Algebra unterscheidet.

#### Sequences

- sequence/suite/Folge
	$(x_{n}):=\varphi: \mathbb{N} \to X$
	$(x_j)_{j \ge m}:=\psi: m + \mathbb{N} \to X$

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
\mathbb N \arrow[rr, "\varphi"'] \arrow[dr, "s_m(n)=m+n"'] & & X \\  
& m+\mathbb N \arrow[ur, "\psi"'] &
\end{tikzcd}

\begin{tikzcd}
\mathbb N \arrow[rr, "n\mapsto x_{m+n}"'] \arrow[dr, "n\mapsto m+n"'] & & X \\  
& \{m,m+1,m+2,\dots\} \arrow[ur, "j\mapsto x_j"'] &
\end{tikzcd}
\end{document}
```
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd} \mathbb N \arrow[r, "s_m", "\sim"'] & m+\mathbb N \arrow[r, "\psi"] & X \end{tikzcd}
\end{document}
```
- vector space of all number sequences
	$s=s(\mathbb{K})=\mathbb{K}^\mathbb{N}$
- Eigenschaft
	- fast alle: $\exists m\in \mathbb{N}, \forall n \ge m$, $E(x_n)$ wahr ist.
	- unendlich viele: $\exists N\in \mathbb{N}, \text{Anz}(N) = \infty$ und gilt $E(x_n), n\in N$
		- Anzahl
- subsequence/sous-suite/Teilfolge
	Es sei $\varphi = (x_n)\in X^\mathbb{N}$, und $\psi:\mathbb{N}\to \mathbb{N}$ sei strikt wachsend. Dann heißt $\varphi \circ \psi :=(x_{n_k})_{k \in \mathbb{N}} ∈ X^\mathbb{N}$ Teilfolge von $\varphi$, wobei wir $n_k := ψ(k)$ gesetzt haben.

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
- Für $m \in \mathbb{N}^\times$ seien
	$s(\mathbb{K}^m) := \text{Abb}(\mathbb{N}, \mathbb{K}^m) = (\mathbb{K}^m)^{\mathbb{N}}$
	- Abbildung
	$c(\mathbb{K}^m) := \{ (x_n) \in s(\mathbb{K}^m) ; (x_n) \text{ ist konvergent} \} .$
	- $c(\mathbb{K}^m)$ ist ein Untervektorraum von $s(\mathbb{K}^m)$.
	- Die Abbildung $\lim : c(\mathbb{K}^m) \to \mathbb{K}^m, \quad (x_n) \mapsto \lim_{n \to \infty} (x_n)$  ist definiert und linear.
	- Für $(\lambda_n) \in c(\mathbb{K})$ und $(x_n) \in c(\mathbb{K}^m)$ mit $\lambda_n \to \alpha$ und $x_n \to a$ gilt $\lambda_n x_n \to \alpha a$ in $\mathbb{K}^m$.
#### Cluster Points

> [!note] 聚点
>- 任意邻域，总有无穷多项。
>- 任意邻域，任意尾列，总有项。
>- 任意 $ε$ ，任意尾列，总有项在 $ε$-开球里。
>	任意 $ε$-开邻域 ，任意尾列，总有项。

$$
\varphi: \mathbb{N} \longleftrightarrow \mathbb{Q}, x_{n}:=\varphi(n)\implies\forall x\in \mathbb{R}\text{ is a cluster point of }(x_{n}).
$$

#### Convergence of sequences

> [!note] 收敛
>- 任意邻域，几乎所有项。
>- 任意邻域，总有尾列。
>- 任意 $\varepsilon$，总有尾列在 $ε$-开球里。
> 	任意 $ε$-开邻域 ，总有尾列。
	 收敛的条件比聚点更强。

- 收敛$\implies$有界
- 收敛$\implies$有唯一聚点/极限
	有唯一聚点$\cancel{ \implies }$收敛
- 有界+有聚点$\cancel{ \implies }$收敛
	- [real analysis - Show a bound sequence with a cluster point is indeed convergent - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1014909/show-a-bound-sequence-with-a-cluster-point-is-indeed-convergent)
	- [general topology - In what metric spaces does bounded + unique limit point imply convergence of a sequence? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4762540/in-what-metric-spaces-does-bounded-unique-limit-point-imply-convergence-of-a-s)
	- [ca.classical analysis and odes - Sequence that converge if they have an accumulation point - MathOverflow](https://mathoverflow.net/questions/24508/sequence-that-converge-if-they-have-an-accumulation-point)
	- [Simple examples of proper metric spaces? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/792253/simple-examples-of-proper-metric-spaces)

- 收敛$\implies$子列收敛于聚点
- 是聚点 $\Longleftrightarrow$ 有子列收敛焉
	$$
	n_0 := 0, \quad n_k := \min\{m \in \mathbb{N} ; m > n_{k-1}, x_m \in \mathbb{B}(a, 1/k)\}, \quad k \in \mathbb{N}^\times.
	$$
	Nun schließen wir aus dem Wohlordnungsprinzip, daß $n_k$ für jedes $k ∈ \mathbb{N}^×$ wohldefiniert ist.
	
- 比较审敛
	Es seien $(x_n)$, $(y_n)$ konvergente Folgen in $\mathbb{R}$. Ferner gelte $x_n \le y_n$ für unendlich viele $n \in \mathbb{N}$. Dann folgt:
	$$
	\lim x_n \le \lim y_n .
	$$
	- aus $x_n < y_n$ folgt nicht $\lim x_n < \lim y_n$.
- 夹逼定理
	Es seien $(x_n)$, $(y_n)$ und $(z_n)$ reelle Zahlenfolgen mit $x_n \le y_n \le z_n$ für fast alle $n \in \mathbb{N}$, und es gelte
	$$\lim x_n = \lim z_n =: a.$$
	Dann konvergiert auch $(y_n)$ gegen $a$.
- 收敛 $\Longleftrightarrow$ 绝对值收敛
- 收敛 $\Longleftrightarrow$ 各分量收敛 （little to be gained）
	- 复数列收敛 $\Longleftrightarrow$ 实部、虚部收敛

- product metric on $X := X_1 \times \cdots \times X_m$, $(X_j, d_j)$, $1 \le j \le m$
	$(x_n) = ((x_n^1, \dots, x_n^m))_{n \in \mathbb{N}}$
	$a := (a^1, \dots, a^m)$
	$\lim x_n \to a \iff \lim x_n^j \to a^j$.
	- a sequence of vectors is convergent iff the sequences of its components are convergent (? by equivalence of metrics)
- Es seien $m \in \mathbb{N}^\times$ und $x_n = (x_n^1, \dots, x_n^m) \in \mathbb{K}^m$ für $n \in \mathbb{N}$. Dann sind äquivalent:
	- (i) Die Folge $(x_n)_{n \in \mathbb{N}}$ konvergiert in $\mathbb{K}^m$ gegen $x = (x^1, \dots, x^m)$.
	- (ii) Für jedes $k \in \{1, \dots, m\}$ konvergiert die Folge $(x_n^k)_{n \in \mathbb{N}}$ in $\mathbb{K}$ gegen $x^k$. (komponentenweise Konvergenz)
	Eine Folge in $\mathbb{K}^m$ konvergiert genau dann, wenn sie komponentenweise konvergiert.


- Bolzano-Weierstraß
	$\mathbb{K}^m$ 上有界 $\implies$ 有收敛子列&聚点

- 收敛 $\implies$ Cauchy列
	完备：Cauchy列 $\implies$ 收敛 

#### Bounded Sets

bounded/beschränkt
- $d$-beschränkt/beschränkt in $X$ (bezüglich der Metrik $d$)
	Eine Teilmenge $Y \subseteq X$, $\exists M > 0, \forall x, y \in Y, d(x, y) \le M$.
	$\text{diam}(Y) := \sup\limits_{x,y \in Y} d(x, y)$
	$d(x,y)$ 上有界，$\sup{d(x,y)}$ 为直径。
- normbeschränkt/beschränkt in $E$
	in dem von der Norm induzierten metrischen Raum beschränkt ist.
	- $X \subseteq E$ ist beschränkt $\iff$ Es ein $r > 0$ gibt mit $X \subseteq r\mathbb{B}$.

- 像集有界，数列有界
- 像集有界，函数有界
	- Supremumsnorm
		Für $u \in E^X$ setzen wir
		$\|u\|_{\infty} := \|u\|_{\infty, X} := \sup\limits_{x \in X} \|u(x)\| \in \mathbb{R}^{+} \cup \{\infty\}.$

有界数列向量空间 
	$\ell_{\infty} := \ell_{\infty}(\mathbb{K}) := B(\mathbb{N}, \mathbb{K})$
	$\|(x_n)\|_{\infty} = \sup_{n \in \mathbb{N}} |x_n|, \quad (x_n) \in \ell_{\infty}$
	- $c_0$ und $c$ sind normierte Vektorräume bezüglich der Supremumsnorm, und $c_0 \subseteq c \subseteq \ell_\infty$ als Vektorräume.
	- $c_0$ ist ein abgeschlossener Untervektorraum von $\ell_\infty$.

有界函数向量空间
	$B(X,E):=(B(X, E), ‖·‖_{∞}):=\{ u ∈ E^X ; u\text{ ist beschränkt} \}$ ist ein Untervektorraum von $E^X$
	- $(E, ‖·‖)$ Banach $\implies$ $B(X,E)$ Banach
	- $B(E, F ) ∩ \text{Hom}(E, F ) = {0}.$

#### Monotone Sequences

- 单调有界，收敛于确界
	Jede wachsende (bzw. fallende) beschränkte Folge $(x_n)$ in $\mathbb{R}$ konvergiert, und es gilt
	$$
	x_n \uparrow \sup\{x_n; n \in \mathbb{N}\} \quad (\text{bzw. } x_n \downarrow \inf\{x_n; n \in \mathbb{N}\})
	$$
- 一些个重要极限（我好嫌计算。。）

#### Infinite Limits

- $\bar{\mathbb{R}}$ 上无合适度量，以ad hoc定义扩展 $\mathbb{R}$。
	- $\bar{\mathbb{R}}$ 上“收敛”包括趋于无穷（converge improperly）。
	- $\mathbb{R}$ 中单调数列在 $\bar{\mathbb{R}}$ 上“收敛”。

- $\bar{\mathbb{R}}$ 中的上下极限（**任意**数列均有）
	- Limes superior (der kleinste Häufungspunkt)
		$$
		\limsup := \overline{\lim}\limits_{n \to \infty} x_n := \lim_{n \to \infty} \left( \sup_{k \ge n} x_k \right) = \inf_{n \in \mathbb{N}} \left( \sup_{k \ge n} x_k \right)
		$$
	- Limes inferior (der größte Häufungspunkt)
		$$
		\liminf := \underline{\lim}\limits_{n \to \infty} x_n := \lim_{n \to \infty} \left( \inf_{k \ge n} x_k \right) = \sup_{n \in \mathbb{N}} \left( \inf_{k \ge n} x_k \right)
		$$
	- $\bar{\mathbb{R}}$ 上收敛 $\Longleftrightarrow$ $\overline{\lim} x_n \le \underline{\lim} x_n$

#### Completeness

Cauchyfolgen
- 任意 $\varepsilon$，总有尾列，任两项距离小于 $\varepsilon$。
- translationsinvariant
	Sind $(x_n)$ eine Cauchyfolge und $a$ ein beliebiger Vektor in $E$, so ist auch die „um $a$ verschobene“ Folge $(x_n + a)$ eine Cauchyfolge.
	- Dies zeigt insbesondere, daß Cauchyfolgen *nicht* mit Umgebungen beschrieben werden können.
	- [Translation invariant metrics and topological groups - Mathematics Stack Exchange](https://math.stackexchange.com/questions/976933/translation-invariant-metrics-and-topological-groups)
- 收敛 $\implies$ Cauchy列
	Cauchy列$\cancel{\implies}$收敛
- Cauchy列 $\implies$ 有界
- Cauchy列有收敛子列 $\implies$ 收敛

completeness/complétude/Vollständigkeit
complete/complet/vollständig
- Cauchy列 $\implies$ （有界 $\implies$ 有收敛子列 $\implies$）收敛 
- Die Vollständigkeit eines normierten Vektorraumes $E$ ist invariant unter Übergang zu äquivalenten Normen
- $\mathbb{K}^m$ ist ein Banachraum.
- Es seien $X$ eine nichtleere Menge und $E = (E, \|\cdot\|)$ ein Banachraum.
	Dann ist auch $B(X, E)$ ein Banachraum.

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