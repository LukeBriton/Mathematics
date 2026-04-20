We have the following chain of strict inclusions for functions over a closed and bounded non-trivial interval of the real line: 
- Continuously differentiable $⊂$ Lipschitz continuous $⊂$ $α$-Hölder continuous
where $0 < α ≤ 1$. We also have
- Lipschitz continuous $⊂$ absolutely continuous $⊂$ uniformly continuous $⊂$ continuous.

#### norm & metric

[vector spaces - Difference between metric and norm made concrete: The case of Euclid - Mathematics Stack Exchange](https://math.stackexchange.com/questions/38634/difference-between-metric-and-norm-made-concrete-the-case-of-euclid)

[general topology - Metric spaces and normed vector spaces - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1607957/metric-spaces-and-normed-vector-spaces)

#### Continuity

- More precisely, a function is continuous if arbitrarily small changes in its value can be assured by restricting to sufficiently small changes of its argument.
- En première approche, une fonction f est **continue** si, à des variations infinitésimales de l'[antécédent](https://fr.wikipedia.org/wiki/Ant%C3%A9c%C3%A9dent_\(math%C3%A9matiques\) "Antécédent (mathématiques)") x, correspondent des variations infinitésimales de l'[image](https://fr.wikipedia.org/wiki/Image_\(math%C3%A9matiques\) "Image (mathématiques)") _f_(_x_).

> [!note] 连续
>continuity/continuité/Stetigkeit
>Es sei $f:X\to Y$ zwischen den $(X, d_X)$ und $(Y, d_Y)$,
>$f$ ist stetig in $x_0\in X$:
>- 函数值的任意邻域，总包含自变量某个邻域的像。
>	$\forall V\ni f(x_0)$, $\exists U\ni x_0$, s.t. $f(U)\subseteq V$
>	- $\forall \varepsilon>0$, $\exists \delta>0$, s.t. $f\big(B_X(x_0,\delta)\big)\subseteq B_Y\big(f(x_0),\varepsilon\big).$
>- 列连续 Folgenstetigkeit
>	- Folgenkriterium
>	für jede Folge $(x_k)$ in $X$ mit $\lim x_k = x$ gilt: $\lim f(x_k) = f(x)$.
>		- „stetige Funktionen mit Grenzwertbildungen verträglich sind“
>		  $\lim f(x_k) = f(\lim x_k)$
>		  für jede konvergente Folge $(x_k)$ in $X$. Es sei $f: X \to Y$ stetige zwischen metrischen Räumen.
>- $f = (f_1, \dots, f_m) : X \to \mathbb{K}^m$ 各分量连续
>	$f(x_n) \to f(x) \iff f_k(x_n) \xrightarrow[n \to \infty]{} f_k(x), \quad k = 1, \dots, m.$
>	- $f : X \to \mathbb{C}$ 实部、虚部连续
>- （实变函数）左、右连续
>
>$f$ ist stetig:
>- $f^{-1}:\mathcal{T}_Y\to\mathcal{T}_X$
>	- 开集的前像为开
>	- 闭集的前像为闭
>	反之不亦然：
>		- $A=\{(x, y)\in \mathbb{R}^2| xy=1\}$ 闭，$\text{pr}_1(\cdot)$ 连续，但 $\text{pr}_1(A)$ 开。
>		- $y=x^2, x\in(-1,1), y\in[0,1)$   

- 若把它误读成“包含**所有**邻域的像”，就变成“局部常值”，太强。
	$\exists U\ni x_0$, $\forall V\ni f(x_0)$, s.t. $f(U)\subseteq V$
	then $f(U)\subseteq \bigcap_{V\ni f(x_0)} V$
	- In metric (indeed $T_1$) spaces, $\bigcap_{V\ni f(x_0)} V=\{f(x_0)\}$.
	  So $f(U)\subseteq \{f(x_0)\}$
	- Une **fonction localement constante** est une fonction définie sur un espace topologique, telle qu'en chaque point il existe un voisinage sur lequel la fonction est constante.

[Open and closed maps - Wikipedia](https://en.wikipedia.org/wiki/Open_and_closed_maps)
- "Strongly open map" if whenever $U$ is an open subset of the domain $X$, then $f(U)$ is an open subset of $f$'s codomain $Y$.
	$\forall U\ni x_0$, $\exists V\ni f(x_0)$, s.t. $V\subseteq f(U)$
https://dummit.cos.northeastern.edu/teaching_fa22_4555/complexanalysis_5_local_behavior_of_holomorphic_functions_v1.00.pdf
- More explicitly, nonconstant holomorphic functions are "locally onto": if $f (z_0) = w_0$, then near $z_0$, $f$ takes all values sufficiently near $w_0$, in the sense that for any $\epsilon > 0$ there exists an $r > 0$ such that for any $w$ with $|w − w_0| < r$, there exists some $z$ with $|z − z_0| < \epsilon$ with $f (z) = w$.
	$\forall U\ni x_0$, $\exists V\ni f(x_0)$, s.t. $V\subseteq f(U)$
- $f$ 在 $x_0$ 处把每个邻域映成 $f(x_0)$ 的一个邻域
	$\forall \delta>0$, $\exists \varepsilon>0$, s.t. $B_Y\big(f(x_0),\varepsilon\big)\subseteq f\big(B_X(x_0,\delta)\big).$

- $f(x_{0})$ 附近的值，总能被足够接近 $x_{0}$ 的点取到
	$\forall V\ni f(x_0)$, $\exists U\ni x_0$, s.t. $V\subseteq f(U)$
	- 例如 $f(x)=x^2$ 在 $x_0=0$ 连续，但 $f(U)$ 不可能覆盖 $0$ 的任何对称邻域（会缺少负数）

- Abrundungsfunktion, auch Gaußklammer ($[x]$)
	$\lfloor \cdot \rfloor : \mathbb{R} \to \mathbb{R}$, $x \mapsto \lfloor x \rfloor:=\max\{k\in \mathbb{Z}; k\leq x\}$
	ist stetig in $x_0 \in \mathbb{R} \setminus \mathbb{Z}$ und unstetig in $x_0 \in \mathbb{Z}$.
- Dirichletfunktion
	$$
	f(x) := \begin{cases} 1, & x \in \mathbb{Q}, \\ 0, & x \in \mathbb{R} \setminus \mathbb{Q}, \end{cases}
	$$
	ist nirgends stetig, d.h. in jedem Punkt unstetig.
- Lipschitz-stetig & Lipschitz-Konstante $α>0$
	$d(f(x), f(y)) \le \alpha d(x, y), \quad x, y \in X.$
- die kanonischen Projektionen
	Es seien $E_1, \dots, E_m$ normierte Vektorräume.
	Dann ist $E := E_1 \times \dots \times E_m$ bezüglich der Produktnorm $\|\cdot\|_{\infty}$ ein normierter Vektorraum.
	$\mathrm{pr}_k: E \to E_k, \quad x = (x_1, \dots, x_m) \mapsto x_k, \quad 1 \le k \le m,$
	- Jede $\mathrm{pr}_k$ ist Lipschitz-stetig.
	- $\mathrm{pr}_k: \mathbb{K}^m \to \mathbb{K}$
	- $z \mapsto \mathrm{Re}(z)$, $z \mapsto \mathrm{Im}(z)$
- Abstandsfunktion
	Abstand von $x$ zu $M$
	$d(\cdot, M):X\to \mathbb{R}, x\mapsto d(x,M):=\inf_{m∈M} d(x,m)$
	- Lipschitz-stetig
- Isometrie
	$d(f(x), f(x')) = d(x, x')$ für $x, x' \in X$ gilt
	- „die Abstände erhält“
	- In general not bijective 
	  [group theory - Prove that an isometry is a bijection - Mathematics Stack Exchange](https://math.stackexchange.com/questions/498985/prove-that-an-isometry-is-a-bijection)
	  [metric spaces - If $f: M\to M$ an isometry, is $f$ bijective? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/340326/if-f-m-to-m-an-isometry-is-f-bijective)
	- Sind $E$ und $F$ normierte Vektorräume und ist $T: E \to F$ linear,
		so ist $T$ genau dann eine Isometrie, wenn gilt $\|Tx\| = \|x\|, \quad x \in E.$
		- isometrischer Isomorphismus
			$T$ ist außerdem surjektiv
			- $T^{-1}: F \to E$ ist ebenfalls isometrisch.
- Vektorraum der stetigen Abbildungen $C(X, F)\subseteq F^X$
	Es seien $X$ ein metrischer Raum, $F$ ein normierter Vektorraum.
	$f : \text{dom}(f) \subseteq X \to F$, $g : \text{dom}(g) \subseteq X \to F$
		seien stetig in $x_0 \in \text{dom}(f) \cap \text{dom}(g)$.
	- die Summe von $f$ und $g$
		$\text{dom}(f + g) := \text{dom}(f) \cap \text{dom}(g)$
		$f + g : \text{dom}(f + g) \to F,$ $x \mapsto f(x) + g(x)$
	- das $\lambda$-fache von $f$ und $g$
		$\lambda f : \text{dom}(f) \to F,$ $x \mapsto \lambda f(x)$
	- $f + g$ und $\lambda f$ sind stetig in $x_0$.
	Gilt $F = \mathbb{K}$
	- $\text{dom}(f \cdot g) := \text{dom}(f) \cap \text{dom}(g)$
		$f \cdot g : \text{dom}(f \cdot g) \to \mathbb{K}, \quad x \mapsto f(x) \cdot g(x)$ ist stetig in $x_0$.
	Gelten $F = \mathbb{K}$ und $g(x_0) \neq 0$
	- $\text{dom}(f/g) := \text{dom}(f) \cap \{ x \in \text{dom}(g) ; g(x) \neq 0 \}$
		$f/g : \text{dom}(f/g) \to \mathbb{K}, \quad x \mapsto f(x)/g(x)$ ist stetig in $x_0$.
	- 有理函数 连续
	- $\mathbb{K}^n$ 上多项式 连续

- Stetigkeit von Kompositionen
	Es seien $X$, $Y$ und $Z$ metrische Räume.
	Ferner sei $f: X \to Y$ stetig in $x \in X$, und $g: Y \to Z$ sei stetig in $f(x) \in Y$.
	- Dann ist die Komposition $g \circ f: X \to Z$ stetig in $x$.
	- Die Umkehrung ist falsch, d.h., aus der Stetigkeit von $g \circ f$ folgt i. allg. nicht, daß $f$ oder $g$ stetig ist.
- Es sei $f: X \to E$ stetig in $x_0$.
	- Dann ist die Norm von $f$,
	  $\|f\|: X \to \mathbb{R}, \quad x \mapsto \|f(x)\|$ stetig in $x_0$.
	- Die Exponentialfunktion $\exp: \mathbb{C} \to \mathbb{C}$ ist stetig.

- Einseitige Stetigkeit 单边连续 （限于 $\mathbb{R}$ 上序结构）
	$f(x_{0})$ 的邻域，总包含 $x_{0}$ 的某个左/右 $δ$-邻域
	- 左/右连续 $\Longleftrightarrow$ 小于/大于其的序列收敛

- Show that any linear function from $\mathbb{K}^n$ to $\mathbb{K}^m$ is Lipschitz continuous

#### Compactness

$X:=(X,d)$ 中
- 覆盖：能盖住所给集合的一族集合
- 开覆盖：各集均开
- 紧：任意开覆盖，有有限开覆盖子集。
	任意开覆盖，有有限子覆盖。

### Exercise

#### 12: Show that any linear function from $\mathbb{K}^n$ to $\mathbb{K}^m$ is Lipschitz continuous.

Train of thought of mine:

Since implicitly it assumes both vector spaces to be finite-dimensional, it's "natural" to have a basis (standard/natural/canonical basis perhaps), though I'm not very clear if there is a natural choice (maybe in the sense of categorical naturaelity?), and seems it depends on (or is equivalent to?) Axiom of Choice.

Anyway, we can have one (quite standard) basis like $\mathbf{e_1} = (1, ..., 0)^T$, $\mathbf{e_2} = (0, 1, ..., 0)^T$, ..., etc. in a vector space (though someone told me it's only meaningful in an inner product space, for me it's like "all bases are created equal" when only considering linearity). Then we have some isomorphism between matrix representation $\mathrm{M}$ and the linear function $f$, and it maps basis $\{\mathbf{e}_{j}\}_{j\le n}$ to $\{\epsilon_{i}\}_{i\le m}$ (both defined with Kronecker delta) through $\epsilon_{i}=\text{a linear combination of  }\{\mathbf{e}_{j}\}$, maybe we can write it as $\epsilon_{i} = f_{i}({\{\mathbf{e}_{j}\}})$. Since all linear functions are done with the given basis, one can just ignore scalars temporarily...

Then, I have a feeling, for $f = (f_1, f_2, ..., f_m)$ is continuous when it's component-wise continuous (though I'm not quite clear about its proof), why don't we prove its Lipschitz continuity in a similar way?

That is, we need to prove there is some Lipschitz constant α, s.t.
$$
\begin{align*}
& d(f_{1}(\mathbf{x}), f_{1}(\mathbf{y}))\le αd(\mathbf{x},\mathbf{y})\\
& \mathbf{x} = (x_{1}, x_{2}, \dots, x_{n})^T\\
& \mathbf{y} = (y_{1}, y_{2}, \dots, y_{n})^T\\
\end{align*}
$$
How to define the metric... <= induce it from a norm ($\mathbb{K}^n$ and $\mathbb{K}^m$ are normed)

"Unless otherwise stated, we consider $\mathbb{K}^m$ to be endowed with the Euclidean inner product (·|·) and the induced Euclidean norm"

$$
\begin{align*}
d(\mathbf{x},\mathbf{y}) &= ‖\mathbf{x}-\mathbf{y}‖\\
&= ‖(x_{1}-y_{1}, x_{2}-y_{2}, \dots, x_{n}-y_{n})^T‖ \\
d(f_{1}(\mathbf{x}), f_{1}(\mathbf{y})) &= ‖f_{1}(\mathbf{x})-f_{1}(\mathbf{y})‖ \\
&= ‖f_{1}(\mathbf{x} - \mathbf{y})‖\\
& = ‖f_{1}((x_{1}-y_{1}, x_{2}-y_{2}, \dots, x_{n}-y_{n})^T) ‖\\
& = ‖(x_{1}-y_{1})M_{11}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{12}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{1n}\mathbf{e}_{n} ‖\\
& = ‖((x_{1}-y_{1})M_{11}, (x_{2}-y_{2})M_{12}, \dots, (x_{n}-y_{n})M_{1n})^T‖\\
\text{Without loss of generality, let }& M_{11}\text{ be}\max \{M_{1j}\},\ j\le m,\ \text{then we shall have}\\
d(f_{1}(\mathbf{x}), f_{1}(\mathbf{y})) &\le ‖((x_{1}-y_{1})M_{11}, (x_{2}-y_{2})M_{11}, \dots, (x_{n}-y_{n})M_{11})^T‖ \\
&= M_{11}‖(x_{1}-y_{1}, x_{2}-y_{2}, \dots, x_{n}-y_{n})^T‖\\
&= M_{11}d(\mathbf{x},\mathbf{y})
\end{align*}
$$
For all $f_{i}$s, $d(f_{i}(\mathbf{x}), f_{i}(\mathbf{y}))\le\max\{M_{i1}\}d(\mathbf{x},\mathbf{y})$, $i\le m$.

$$
\begin{align*}
d(f(\mathbf{x}), f(\mathbf{y})) &= ‖f(\mathbf{x}) - f(\mathbf{y})‖ \\
&= ‖f(\mathbf{x} - \mathbf{y})‖\\
&= ‖f_{1}(\mathbf{x} - \mathbf{y}) + f_{2}(\mathbf{x} - \mathbf{y}) + \dots + f_{m}(\mathbf{x} - \mathbf{y})‖\\
& = ‖(x_{1}-y_{1})M_{11}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{12}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{1n}\mathbf{e}_{n}\\
&\quad+(x_{1}-y_{1})M_{21}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{22}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{2n}\mathbf{e}_{n}\\
&\quad+(x_{1}-y_{1})M_{m1}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{m2}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{mn}\mathbf{e}_{n}‖\\
&\le ‖(x_{1}-y_{1})M_{11}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{12}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{1n}\mathbf{e}_{n}‖\\
&\quad+‖(x_{1}-y_{1})M_{21}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{22}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{2n}\mathbf{e}_{n}‖\\
&\quad+‖(x_{1}-y_{1})M_{m1}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{m2}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{mn}\mathbf{e}_{n}‖\\
&\le M_{11}d(\mathbf{x},\mathbf{y}) + M_{21}d(\mathbf{x},\mathbf{y}) +\dots+ M_{m1}d(\mathbf{x},\mathbf{y})\\
&\le \max\{M_{i1}\}d(\mathbf{x},\mathbf{y})
\end{align*}
$$


$id = \mathbf{e} \otimes \mathbf{v}$

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
	V \arrow[r, "f"] \arrow[d, "\mathbf{e}^j"'] & W \arrow[d, "\mathbf{\epsilon}_i"] \\
	\mathbb{R}^n \arrow[r, "T"']                & \mathbb{R}^m                      
\end{tikzcd}
\end{document}
```
$$
\begin{align*}
T&=\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n} A_{j}^i\mathbf{e}^j\otimes\mathbf{\epsilon}_i, \mathbf{e}^j\text{为对偶基}\\
T(v)&=\sum\limits_{1\leq i\leq m, 1\leq j\leq n} A_{j}^i\mathbf{e}^j(v)\mathbf{\epsilon}_i\\
&=\sum\limits_{i,j} A_{j}^iv_{j}\mathbf{\epsilon}_i\\
\end{align*}
$$
